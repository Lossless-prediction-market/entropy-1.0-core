# Entropyfi (50,50) Overview

## What is Entropyfi (50,50)?

Entropyfi (50,50) brings two innovative products designed specifically for rebase token holders: **Soft Hedge** and **Soft Leverage**.

These products allow OHM holders and other rebase token enthusiasts to manage risk while maximizing returns — all without liquidation risk.

## Design Philosophy: (3,3) Alignment

Entropyfi (50,50) is built for the "(3,3)" DeFi strategy popularized by OlympusDAO:

- **(9,9)** — Full leverage with high reward potential but liquidation risk
- **(3,3)** — Balanced staking with moderate rewards and stability
- **Soft Leverage** — Extra yield with zero liquidation risk
- **Soft Hedge** — Risk management without unwinding positions

## The Two Products

### Soft Hedge

A "cope-free" way to hedge your position against short-term price drops while maintaining long-term holdings.

**Use case:** You're bullish long-term but see near-term headwinds. You want insurance without selling.

**How it works:**
1. Predict the rebase token price will go DOWN
2. If price drops: receive additional rebase rewards from "Leverage" side holders
3. These additional rewards offset your price depreciation
4. If price goes up: you lose only the rebase reward difference (paid to Leverage side)

**Payoff:** Insurance with rebase yield as the "premium"

### Soft Leverage

A "rekt-free" way to boost your rebase rewards without liquidation risk.

**Use case:** You're extremely bullish and want to amplify your rebase rewards, but can't stomach liquidation risk.

**How it works:**
1. Predict the rebase token price will go UP
2. If price goes up: receive boosted rebase rewards + price appreciation gains
3. If price goes down: lose only the rebase reward difference (paid to Hedge side holders)
4. If price stays flat: earn the rebase, avoid the leverage

**Payoff:** 2x-3x rebase reward boost without liquidation cliff

## Visual Comparison: Payoff Matrix

```
Price Goes Up (+10%)
├─ Normal Staking: Standard rebase + 10% price gain = 15% total
├─ Soft Hedge: Standard rebase - reward difference = ~10% total
├─ Soft Leverage: Boosted rebase + reward difference + 10% = 25% total
└─ (9,9) Leverage: Boosted rebase + reward difference + 10% OR liquidated

Price Goes Down (-10%)
├─ Normal Staking: Standard rebase - 10% price loss = -5% total
├─ Soft Hedge: Standard rebase + reward difference - 10% = ~0% total
├─ Soft Leverage: Boosted rebase - reward difference - 10% = -20% total
└─ (9,9) Leverage: Boosted rebase - reward difference - 10% = liquidated
```

## Key Differences: Soft Leverage vs (9,9)

| Feature | Soft Leverage | (9,9) Leverage |
|---|---|---|
| **Liquidation Risk** | Zero | High |
| **Max Loss** | Rebase rewards only | All collateral + liquidation penalty |
| **Unbounded Upside** | Yes | Yes |
| **Borrowing Fees** | Included in rebase | Explicit borrow cost |
| **Simplicity** | Binary prediction | Complex liquidation management |
| **Community Health** | No liquidation cascades | Risk of systemic liquidation |

## The Community Benefit

By using Soft Leverage instead of (9,9) leverage, you:
- Reduce your personal liquidation risk
- Reduce cascading liquidation effects on the community
- Maintain protocol stability
- Support a healthier ecosystem

## Products Included

Entropyfi (50,50) currently supports:

1. **VSQ (VESQ)** — Rebase token on Polygon
   - Live on mainnet
   - 8-hour prediction cycles (matching rebase frequency)

2. **Redacted Cartel** — Ethereum-based rebase project
   - Partnership proposed
   - Coming soon

3. **Additional partners** — More rebase tokens launching

## How (50,50) Is Different From Prediction Markets

**Standard Prediction Markets:**
- Binary outcome (yes/no)
- 50/50 split between sides is coincidental
- Any asset class (stocks, commodities, crypto)
- Settlement price vs initial price

**Entropyfi (50,50):**
- Perfectly balanced mechanics (50% long, 50% short by design)
- Designed for rebase tokens specifically
- Leverages rebase cycles (often 8-hour periods)
- One side wins rebase boost, one side loses it
- Zero-sum game of rebase reward distribution

## Economics of Rebase Rewards

Each rebase cycle, the protocol issues new tokens to stakers. In Entropyfi (50,50):

```
Total Rebase Issued: 100 tokens

Price went UP:
├─ Leverage (YES) side: 100 + bonus (say +30) = 130 tokens
└─ Hedge (NO) side: bonus transferred to Leverage, they get 70 tokens

Price went DOWN:
├─ Leverage (YES) side: 100 - penalty (say -30) = 70 tokens
└─ Hedge (NO) side: penalty transferred to them, they get 130 tokens
```

The total rebase is preserved, just redistributed based on the outcome.

## Getting Started with (50,50)

1. **Have rebase tokens** — e.g., sVSQ, staked VSQ, etc.
2. **Go to the prediction interface** — Select your target token
3. **Choose your side** — Leverage (YES) or Hedge (NO)
4. **Predict price direction** — Simple binary prediction
5. **Deposit** — Your rebase tokens are used as collateral
6. **Wait for settlement** — 8 hours for most cycles
7. **Claim rewards** — Rebase adjusted by outcome
8. **Compound** — Winnings automatically re-enrolled next cycle

## Risks & Considerations

**Soft Leverage risks:**
- Lose rebase reward difference if price goes down
- Missing out on hedge protection
- Volatility amplification during downturns

**Soft Hedge risks:**
- Lose rebase reward difference if price goes up
- Opportunity cost vs holding without hedge
- Small insurance cost (the reward difference)

**Both:**
- Price oracle accuracy (Chainlink Feeds)
- Smart contract security (always audit before use)
- Market illiquidity for small cap tokens

## Advanced Features

- **Swap sides** — Change from Leverage to Hedge during 4-hour deposit window
- **Pause** — Exit position anytime without penalty
- **Auto-compound** — Winners automatically roll into next cycle
- **Set & forget** — Leave your position running for multiple cycles

---

**Next:** [Cope-Free Hedge Guide](./cope-free-hedge.md)
