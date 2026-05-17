# Prediction Market

## Overview

The Entropyfi Prediction Market allows you to speculate on asset prices while keeping your principal safe. All deposits are supplied to Aave to generate yield, which is distributed to winners.

## How It Works

### Step 1: Find a Market

Use the filter in the upper right corner to find a market you want to predict on.

Markets are available for:
- Crypto assets (BTC, ETH, etc.)
- Commodities (TSLA, etc.)
- DeFi tokens (OHM, VSQ, etc.)

### Step 2: Place Your Prediction

**Predict Long 🔺** — You think the price will be higher than the target value

**Predict Short 🔻** — You think the price will be lower than the target value

**Example:**
If BTC is currently trading at $40,000 and the target price is $44,772:
- Select "Long" if you think BTC will close above $44,772
- Select "Short" if you think BTC will close below $44,772

### Step 3: Deposit Your Collateral

You can deposit any supported asset:
- USDT
- USDC
- DAI
- ETH

No need to convert — multi-collateral pools handle everything automatically.

**How much?** The more you deposit, the larger your share of the winning yield pool.

### Step 4: Wait for Settlement

Each game has:
- **Join Period** — When users can deposit (usually 4 hours)
- **Cool-down Period** — When the pool is locked and supplied to Aave (usually 4 hours)
- **Settlement** — Chainlink oracle verifies the final price

### Step 5: Claim Your Result

**If you won:** You receive your principal + your proportional share of the yield pool

**If you lost:** You receive 100% of your principal back. No loss.

**Example Payout:**
- Pool deposits: 10,000 USDC
- Yield earned: 100 USDC
- Winners: 5 users
- Your deposit: 1,000 USDC (20% of winners)
- Your payout: 1,000 USDC + (100 × 20%) = 1,020 USDC

## Auto-Compounding (Set & Forget)

Winners are automatically enrolled in the next round with their winnings as the new principal.

For "perma-bull" or "perma-bear" strategies, simply leave your tokens in the pool and let compounding work automatically.

## Swapping Sides

Changed your mind about the price direction?

1. Click **Swap Shares** 🔁
2. Choose your new side (Long ↔ Short)
3. Enter the amount to swap
4. Confirm

Your old tokens are burned and new tokens are minted at the current pool rate.

## Withdrawing

You can withdraw anytime, even during the locked period.

### To Withdraw:

1. Click **View Pool** to go to the pool detail page
2. Enter the Long & Short token amounts you want to withdraw
3. Click **Withdraw**

Your pool tokens will be burned and you'll receive your collateral.

### Choose Your Return Format:

- **Aave aTokens** — Keep earning yield after you leave the game (pause your prediction)
- **Principal Tokens** — Get USDC/USDT/DAI back directly

**Why aTokens?** You save on gas fees and continue earning Aave yield while sitting out a round.

## Yield Calculation

### Interest Generation

During the locked period, all deposits are supplied to Aave:

```
Total Pool Funds → Aave → Generates Interest
```

### Winner Distribution

At settlement, interest is allocated proportionally to all winners:

```
Winner's Share = (Winner's Deposit / Total Winning Deposits) × Total Interest
```

### Pool Token Value Update

After each round, pool token values are updated based on the outcome:

- **If Long wins:** Long token value increases
- **If Short wins:** Short token value increases

Pool tokens can always be redeemed for the underlying collateral at the updated NAV (Net Asset Value).

## Example Game Walkthrough

**Scenario:** BTC-USDT Weekly Prediction

**Setup:**
- Target Price: 44,772 USDT
- Join Period: Monday 12am - 4am UTC
- Locked Period: Monday 4am - Thursday 12pm UTC
- Settlement: Thursday 12pm UTC

**Players:**
- Alice: Deposits 1,000 USDT → Predicts Long → Gets 1,000 lgBTC-USDT tokens
- Bob: Deposits 2,000 USDT → Predicts Long → Gets 2,000 lgBTC-USDT tokens
- Charlie: Deposits 1,000 USDT → Predicts Short → Gets 1,000 stBTC-USDT tokens

**During Locked Period:**
- All deposits (4,000 USDT) supplied to Aave
- Aave generates ~38.46 USDT in interest (assuming 0.3% weekly yield)

**At Settlement:**
- BTC closes at 45,000 USDT (above target)
- Long predictions win
- Charlie (Short) gets 1,000 USDT back (no loss)

**Payouts to Winners:**
- Total winning deposits: 3,000 USDT (Alice + Bob)
- Total interest: 38.46 USDT

Alice's payout:
```
1,000 / 3,000 × 38.46 = 12.82 USDT yield
Total: 1,000 + 12.82 = 1,012.82 USDT
```

Bob's payout:
```
2,000 / 3,000 × 38.46 = 25.64 USDT yield
Total: 2,000 + 25.64 = 2,025.64 USDT
```

Charlie's payout:
```
1,000 USDT (full principal returned)
```

## Key Points

- Your principal is always safe
- Winning is about skill and prediction accuracy
- Losing means zero financial penalty
- Higher deposits = larger share of winning yield
- You can exit anytime without penalties
- Multi-round play compounds returns

## Oracle Integration

Price verification is handled by **Chainlink Price Feeds**, a decentralized oracle network that provides high-quality, tamper-proof price data from multiple aggregators.

The initial target price is queried when the first user joins the game.
