# Nulloss Markets

A lossless prediction market protocol deploying on Arc.

Users deposit USDC to predict asset price movements. Their principal is never at risk. The interest generated on deposits during each prediction round becomes the prize pool. Correct predictions receive a share of it. Incorrect predictions reclaim their full deposit.

Loss is null. Hence the name.

---

## The Problem With Prediction Markets Today

Prediction markets are among the most intellectually honest financial instruments ever designed. They aggregate dispersed information, surface real-time consensus on uncertain outcomes, and have repeatedly outperformed expert forecasts across elections, macroeconomic events, and policy decisions.

Yet they have consistently failed to scale.

The reason is structural. In a traditional prediction market, incorrect participants forfeit capital. This creates a hard psychological ceiling on participation. Users who lose money stop engaging. Casual participants, the people whose aggregated views make price discovery meaningful, exit after their first bad round. What remains is a thin market of committed speculators rather than the broad participation the mechanism requires to function well.

Nulloss removes that ceiling.

---

## The Lossless Mechanic

Every deposit in a Nulloss prediction pool is supplied to Morpho Blue on Arc, where it generates interest during the prediction round. At settlement, the oracle reads the final price. Correct predictions receive a proportional share of the interest pool. Incorrect predictions receive their full deposit back.

```
User deposits 1,000 USDC  →  Predicts Long or Short
                ↓
      Supplied to Morpho Blue (interest accrues)
                ↓
      Oracle settles at round expiry
                ↓
  If correct:   1,000 USDC + share of interest pool
  If incorrect: 1,000 USDC (full deposit returned)
```

The principal is structurally protected by the architecture of the protocol. Not by a guarantee. Not by insurance. By design.

This mechanic removes the primary barrier to prediction market participation. Users who are wrong are not penalized. They simply did not win this round. They stay. They participate again. The market deepens.

---

## Why Arc

Nulloss deploys on Arc. The infrastructure fit is direct.

**USDC as native gas.** Every interaction on Nulloss is denominated in USDC. Deposits, withdrawals, interest claims, and gas fees are all paid in the same asset. Users do not need to acquire or manage a separate volatile gas token. This removes a layer of friction that no general-purpose chain has been able to eliminate.

**Sub-second deterministic finality.** Arc's Malachite BFT consensus finalizes transactions in under one second with certainty. For a prediction market, this means settlement is instant and unambiguous. No probabilistic waiting period. No reorg risk. No settlement ambiguity.

**Stablecoin-native multi-currency support.** Arc's StableFX infrastructure enables USDC and EURC pools on the same settlement layer. Nulloss can serve participants in different currency contexts without bridges or wrapped assets.

**Compliance-ready architecture.** Arc's opt-in compliance tools enable Nulloss to offer institutional pool tiers with appropriate access controls. This product tier requires infrastructure that general-purpose chains were not designed to support.

**Morpho Blue on Arc.** Morpho is a confirmed Arc ecosystem partner. Nulloss uses Morpho Blue's isolated market design. One Morpho market per prediction pool. Interest positions are completely isolated across pools.

---

## Protocol Architecture

### Pool Lifecycle

Each Nulloss prediction pool runs through three phases:

**Open phase:** Users deposit USDC and select their prediction (Long or Short). All deposits are immediately supplied to the pool's dedicated Morpho Blue market and begin accruing interest. Users can swap sides or exit during this phase.

**Locked phase:** The deposit window closes. Capital remains in Morpho Blue accruing interest. Users can still exit but cannot change their prediction.

**Settlement:** The oracle reads the asset price. Correct predictions are determined. Accrued interest is distributed proportionally among correct participants. All users, correct and incorrect alike, withdraw their full principal.

### Pool Tokens

Each pool issues three ERC-20 tokens representing positions:

- **Long Token (lg-):** Minted when a user predicts the price will close above target
- **Short Token (st-):** Minted when a user predicts the price will close below target
- **Sponsor Token (sp-):** Minted when a sponsor deposits liquidity to increase pool depth

Tokens are valued at 1:1 with the underlying collateral at deposit. After settlement, the NAV of winning tokens increases proportionally to interest distributed. Tokens can be redeemed at any time for their current underlying value.

This design enables auto-compounding. A winning participant's tokens carry their increased NAV into the next round without requiring a transaction.

### Interest Layer: Morpho Blue

Nulloss uses Morpho Blue as its primary interest source. Morpho Blue is a minimal, immutable lending protocol (650 lines of audited code) that creates isolated markets per asset pair.

Each Nulloss prediction pool corresponds to one Morpho Blue market:

- Loan token: USDC
- Collateral: USDC (pure supply, no borrow exposure)
- Oracle: Chainlink price feed for the market's asset pair
- Supply cap: governance-controlled per pool

Interest accrues continuously as Morpho's share price appreciates. At settlement, the protocol withdraws the full position, calculates net interest as the difference between the withdrawn amount and principal deposited, and distributes accordingly.

Aave serves as a fallback interest source if Morpho supply caps are reached for a given pool.

### Oracle Strategy

Settlement prices are sourced from multiple independent oracle providers, all confirmed on Arc:

- **Primary:** Chainlink Data Streams (pull model, aggregated from multiple sources)
- **Secondary:** Pyth Network (sub-second updates from first-party sources)
- **Fallback:** Stork or RedStone

Settlement uses the median of two independent readings and rejects divergence above a governance-set threshold. This multi-oracle approach reduces the manipulation surface compared to single-oracle designs.

### Protocol Sustainability

Nulloss is designed for long-term operation with a sustainable fee structure:

**Interest fee:** The protocol deducts a governance-controlled percentage of interest distributed to correct participants. This fee does not affect principal and is not visible to incorrect participants, who receive their full deposit regardless.

**Market creation fee:** A flat USDC fee is charged to create a new prediction pool. This controls pool creation quality and funds protocol operations.

**Vault curator participation:** Nulloss operates as a MetaMorpho Vault curator, participating in vault fee distribution across deposits under management.

**Treasury deployment:** Protocol-owned USDC is deployed into Morpho Vaults, where it generates interest that funds ongoing development.

This structure was designed in direct response to the sustainability failure of earlier lossless prediction market protocols, which launched without clear operational funding and did not survive the 2022 bear market.

---

## Institutional Tier: USYC Pools

Arc supports USYC, a yield-bearing stablecoin issued by Circle and backed by short-duration US Treasury securities.

For institutional participants, Nulloss offers USYC-denominated prediction pools. Deposits are held in USYC during the prediction round, accruing Treasury interest throughout. Correct participants receive their USYC back plus a share of the Morpho interest pool. Incorrect participants receive their full USYC deposit back.

USYC pools require institutional KYC via Arc's compliance infrastructure and are subject to Circle's USYC eligibility requirements, including minimum deposit thresholds and non-US institutional classification.

---

## Multi-Currency Support

Arc's StableFX infrastructure enables native onchain FX between stablecoins. Nulloss launches with:

- **USDC pools:** Primary markets for retail and institutional participants
- **EURC pools:** Euro-denominated markets for European participants
- **USYC pools:** Institutional-tier markets (KYC required)

Participants on other chains can bridge USDC to Arc via Circle's CCTP (Cross-Chain Transfer Protocol, Domain 26), enabling access from Ethereum, Base, Polygon, and other CCTP-supported networks.

---

## Governance

$NULL is the Nulloss protocol governance token.

Governance controls:

- Protocol fee percentage (governance-controlled range)
- Approved Morpho vault curators and risk parameters
- Supported collateral assets and oracle configurations
- Protocol upgrade proposals

$NULL emission is milestone-based rather than time-based. No continuous liquidity mining. Governance token utility is anchored to protocol decisions, not speculative mechanics.

---

## Current Status

Nulloss Markets is in active development, targeting deployment on Arc testnet.

**Completed:**
- Protocol architecture designed
- Interest layer selected (Morpho Blue on Arc)
- Oracle strategy defined (Chainlink + Pyth multi-oracle)
- Smart contract interface specifications drafted
- Reference implementation research complete
- Arc testnet environment configured

**In progress:**
- Smart contract implementation in Solidity 0.8.28
- Morpho Blue interest adapter
- Chainlink and Pyth oracle adapter
- Pool factory and pool template contracts
- Governance token contract

**Planned:**
- Arc testnet deployment
- Full round lifecycle testing
- External security audit
- Arc mainnet deployment
- Frontend application

---

## Technical Stack

| Component | Choice | Rationale |
|---|---|---|
| Chain | Arc (Chain ID: 5042002) | Stablecoin-native, sub-second finality, USDC gas |
| Interest layer | Morpho Blue | Isolated markets per pool, 650-line immutable core |
| Interest fallback | Aave | Secondary source if Morpho supply caps are reached |
| Oracle primary | Chainlink Data Streams | Aggregated, decentralized, confirmed on Arc |
| Oracle secondary | Pyth Network | Sub-second updates, matches Arc finality model |
| Stablecoins | USDC + EURC + USYC | Circle-native, no wrapping required |
| Smart contracts | Solidity 0.8.28 | Modern, built-in overflow protection |
| Framework | Foundry | Standard toolchain for Solidity development |
| Cross-chain | CCTP (Domain 26) | Native USDC bridging across supported networks |

---

## Arc Testnet Configuration

```
Network Name:  Arc Testnet
Chain ID:      5042002
RPC URL:       https://rpc.testnet.arc.network
Explorer:      https://testnet.arcscan.app
Faucet:        https://faucet.circle.com
Gas Token:     USDC
```

**Native Contract Addresses (Arc Testnet):**
```
USDC:     0x3600000000000000000000000000000000000000
EURC:     0x89B50855Aa3bE2F677cD6303Cec089B5F319D72a
USYC:     0xe9185F0c5F296Ed1797AaE4238D26CCaBEadb86C
Permit2:  0x000000000022D473030F116dDEE9F6B43aC78BA3
```

---

## Research Foundation

Nulloss Markets is informed by a thorough analysis of Entropyfi, a lossless prediction market protocol that launched on Polygon in November 2021, raised $1.6M, and shut down in 2022.

Entropyfi demonstrated that the lossless mechanic works at the protocol level. It did not survive long enough to see prediction markets reach mainstream adoption. The protocol lacked a durable operational funding model, launched on infrastructure not designed for stablecoin-native financial applications, and wound down during the 2022 bear market before reaching product-market fit.

Nulloss is designed with those failure points in scope:

- Operational funding built into the protocol from day one
- Deploying on Arc, infrastructure designed specifically for stablecoin-native finance
- Building in 2026, when prediction markets are a demonstrated category with institutional interest
- Morpho Blue instead of Aave, with isolated markets and a smaller audited codebase
- Multi-oracle settlement instead of single-oracle dependence

---

## Links

- **GitHub:** https://github.com/LossLess-Labs/entropy-1.0-core
- **Builder:** [@jadeofwallstreet](https://twitter.com/jadeofwallstreet)
- **Arc Explorer:** https://testnet.arcscan.app

---

*Nulloss Markets is under active development. Smart contracts have not been audited. Do not deploy funds on testnet builds.*

| Token       | Token Address | Decimals
| ----------- | -------------- | -------
| USDT        | [0x13512979ADE267AB5100878E2e0f485B568328a4](https://kovan.etherscan.io/address/0x13512979ADE267AB5100878E2e0f485B568328a4) | 6
| USDC        | [0xe22da380ee6B445bb8273C81944ADEB6E8450422](https://kovan.etherscan.io/address/0xe22da380ee6B445bb8273C81944ADEB6E8450422) | 6
| DAI         | [0xFf795577d9AC8bD7D90Ee22b6C1703490b6512FD](https://kovan.etherscan.io/address/0xFf795577d9AC8bD7D90Ee22b6C1703490b6512FD) | 18
