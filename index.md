---
title: MoniPay Security — Threat Model, Key Storage, RLS Policies, Rate Limits
description: MoniPay's security model — AES-256-GCM key encryption with PIN-derived KDF, deny-all RLS on every database table, signed edge-function requests, HMAC-SHA256 webhooks, rate limits on relay endpoints, soft account deletion, and the Walkaway Test as a non-negotiable design principle.
keywords: monipay security, non custodial wallet security, aes-256-gcm encryption, pbkdf2 key derivation, supabase rls policies, signed edge functions, hmac sha256 webhooks, threat model crypto wallet, walkaway test security, monipay rate limits
canonical: https://docs.monipay.xyz/security/
---

# Security

MoniPay's security model rests on three load-bearing pillars: **local key encryption**, **server-side validation**, and **Walkaway-Test resilience**. Each pillar is designed to remain intact even if the other two are partially compromised.

## Pillar 1 — Local key encryption

- **Algorithm:** AES-256-GCM, with a unique IV per encryption.
- **Key derivation:** PBKDF2 with a high iteration count and a per-user salt — fast enough to be tolerable on every device, slow enough to make offline brute-force impractical.
- **Storage location:** browser `localStorage` (web), Keychain (iOS), KeyStore (Android), secure enclave when the device supports it.
- **Solana keys:** Ed25519 keypairs, `localStorage`-only, **never** written to the database. On import, the decrypted public key must match the address bound to the user's MoniTag; mismatches reject. See [Solana key storage model](/security/solana-key-storage).
- **PIN lockout:** repeated wrong-PIN attempts trigger exponential backoff and eventually a hard lock that requires re-verification.

## Pillar 2 — Server-side validation

### Database (Supabase / Lovable Cloud)

- **Row Level Security:** **deny-all by default**. Every table has explicit `SELECT`, `INSERT`, `UPDATE`, `DELETE` policies. No table is ever readable or writable without an explicit policy that names the access.
- **Roles in a separate `user_roles` table** with a `SECURITY DEFINER` `has_role(user_id, role)` function — no client-side admin checks. Admin checks always happen server-side, against a function that bypasses RLS only inside the function body.
- **Storage buckets** scoped by user-ID path. A user cannot read or write to another user's path even if they hold a valid session token.
- **Rate limits:** `relay-payment` enforces **5 requests / wallet / minute** and **10 requests / IP / minute**. Other sensitive endpoints have per-route limits configured to their abuse profile.
- **Soft account deletion:** `profiles.status = 'deactivated'`. Data is retained for legal and audit compliance. Re-import of a deactivated account is blocked. The DELETE action requires a two-step confirmation to prevent accidental loss.

### Edge functions

- **Signed requests.** The native Flutter app uses a dedicated `signedFetch` HTTP wrapper that signs every request. The web app uses Supabase JWT.
- **HMAC-SHA256 webhook signatures** on every merchant callback. Receivers verify in constant time.
- **Builder-code attribution.** Every MoniPay-routed Base transaction appends the ERC-8021 builder code `bc_qt9yxo1d` as a hex suffix.

### Anti-abuse

- Multi-RPC failover with exponential backoff means a single RPC outage cannot stall the platform.
- Transaction deduplication via unique constraints on `monibot_transactions.tweet_id` and similar — the same social-payment trigger cannot double-pay.
- Reserved-MoniTag enforcement blocks ~150 impersonation-prone usernames at registration time. See [reserved usernames](/monitag/reserved-usernames).

## Pillar 3 — Walkaway-Test resilience

The single principle every product decision is evaluated against: **if MoniPay disappeared tomorrow, your funds would remain spendable from any compatible wallet.** Standard cryptography, standard tokens, exportable keys, no custody, on-chain history. See [the Walkaway Test](/security/walkaway-test) for the full reasoning.

## What MoniPay does *not* do

- **No seed phrases for users to misplace.** The PIN-encrypted key blob plus optional Google Drive AES-GCM backup are the recovery path.
- **No PIN reset.** A PIN reset would require server-held secrets. The Walkaway Test forbids it. Losing your PIN without a backup means losing access — same as every honest self-custody wallet.
- **No custodial fallback.** There is no "we'll move your funds for you" recovery path.
- **No upgradeability proxies in the router contracts.** The contract you read on the explorer is the contract that will execute your payment, forever.

## Security disclosure

Report security issues to **security@monipay.xyz**. Critical issues are acknowledged within 24 hours. We prioritise issues that threaten user funds or compromise the Walkaway Test.

## Read next

- [Solana key storage model](/security/solana-key-storage)
- [The Walkaway Test](/security/walkaway-test)
- [Reserved usernames](/monitag/reserved-usernames)
- [Smart contracts](/contracts/)
