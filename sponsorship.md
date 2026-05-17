# Sponsorship

## Overview

Sponsors boost the yield available to players by depositing stablecoins into pools. In return, sponsors receive ERP governance tokens as rewards.

## Why Sponsor?

Sponsors create a positive feedback loop:

```
More Sponsors → Higher APY for Players → More Valuable Governance Token → More Sponsors
```

Benefits for sponsors:
- Earn ERP governance tokens
- Contribute to protocol growth
- Receive proportional rewards from sponsor fees

## How Sponsorship Works

### Step 1: Sponsor a Pool

1. Navigate to the sponsorship interface
2. Click the **Deposit** button
3. Select the pool you want to sponsor
4. Enter the amount of stablecoins (typically USDT) to deposit

**Important:** Deposit stablecoins, not principal assets.

### Step 2: Receive Sponsor Tokens

When you deposit, you receive **sponsor tokens** in a 1:1 ratio.

Example:
- You deposit 5,000 USDT
- You receive 5,000 Sponsor Tokens
- These sponsor tokens are proof of your deposit

### Step 3: Stake Sponsor Tokens

1. Using the stake button on the right side of the sponsorship interface
2. Click **Stake**
3. Your sponsor tokens are staked in the farming contract
4. You begin earning ERP tokens

### Step 4: Claim Your ERP Rewards

ERP tokens are distributed continuously to sponsors based on their share of total sponsor deposits.

Your ERP share calculation:

```
Your ERP Reward = (Your Sponsor Tokens / Total Sponsor Tokens) × ERP Rewards Distributed
```

## Exiting as a Sponsor

### To Redeem Your Sponsor Tokens:

1. Go to the sponsorship interface
2. Click **Exit Farm** button on the right side
3. Follow Step 1 & Step 2 in the UI
4. Your sponsor tokens are burned
5. You receive your USDT back

Your remaining staked sponsor tokens will continue earning ERP until you exit.

## How Sponsors' Yield Feeds Players

All sponsor deposits are supplied to Aave alongside player deposits.

**Pool Composition:**
```
Player Deposits (50%) + Sponsor Deposits (50%) = Full Pool Supplied to Aave

Example:
- 50 players deposit 1,000 USDC = 50,000 USDC
- 10 sponsors deposit 50,000 USDC = 50,000 USDC
- Total pool: 100,000 USDC sent to Aave
- Generated yield: 100,000 × 0.3% = 300 USDC
- Sponsors' yield: 150 USDC sent to winners
- Players' yield: 150 USDC distributed among winners
```

## ERP Token Distribution

Sponsors earn ERP tokens through liquidity mining. The amount earned depends on:

1. **Your proportional share** of total sponsor deposits
2. **The distribution rate** set by the protocol
3. **Duration of staking** (longer staking may earn bonuses)

ERP tokens unlock governance rights and may increase in value as the protocol grows.

## Pool Sponsor Index

Sponsor tokens are tracked by pool. Each pool has its own sponsor token with a specific contract address.

Example sponsor token mapping (Polygon Mainnet):

| Pool | Sponsor Token | Contract Address | Decimals |
|------|---|---|---|
| spBTC-USDT | spBTC-USDT | 0xc6aaf7a2f7d2f08eaa7645cfadb48df1fd657cc4 | 6 |
| spBTC-USDC | spBTC-USDC | 0xb66656036e906e510b243f9e9a66e5599289b9cb | 6 |
| spOHM-USDT | spOHM-USDT | 0x3b8d2f30e081c7c8b9b183229dd6d4c18bfeac65 | 6 |

## Key Points

- **Safe deposits** — Your sponsor capital is always secure
- **Proportional rewards** — You earn ERP based on your share of total sponsors
- **Continuous yield** — ERP rewards accrue continuously, not just at round end
- **Exit anytime** — Redeem sponsor tokens and withdraw USDT without penalties
- **Community aligned** — Sponsors and players benefit together

## Example: Sponsoring a BTC-USDC Pool

**Starting situation:**
- You want to sponsor the BTC-USDC prediction pool
- Current pool size: 100,000 USDC from players
- No existing sponsors
- Sponsor APY: 15% (ERP rewards)

**Your actions:**
1. Deposit 10,000 USDT
2. Receive 10,000 spBTC-USDC sponsor tokens
3. Stake the sponsor tokens
4. Pool now has 100,000 (players) + 10,000 (sponsors) = 110,000 USDC

**What happens next:**
- All 110,000 USDC supplied to Aave
- Over a week, generates ~33 USDC in yield
- 16.5 USDC goes to winners, 16.5 USDC is "sponsor share"
- You earn ERP tokens at ~15% APY on your sponsor tokens
- On 10,000 USDT, that's ~28.85 ERP per week

**After 4 weeks:**
- You've earned ~115 ERP tokens
- Your 10,000 spBTC-USDC tokens remain valid
- You can unstake and exit anytime

## Sponsor-Player Alignment

The protocol is designed so sponsors and players align financially:

- Bigger pools attract more players (higher competition, faster games)
- More sponsors = higher yields for players = more players join
- More players = more exciting markets
- Sponsors earn ERP tokens, which may appreciate

This creates a positive growth cycle for the entire ecosystem.
