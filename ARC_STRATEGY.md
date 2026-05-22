# LossLess Labs — Arc Strategy

## 1. Chain Choice
Arc is selected for predictable fee UX (USDC-native gas), sub-second finality, and strong stablecoin infrastructure alignment.

## 2. Yield Architecture
- Primary: Morpho Blue per-pool isolated markets.
- Fallback: Aave adapter.
- Adapter pattern ensures pools are agnostic to underlying money market.

## 3. Oracle Strategy
- Primary settlement oracle: Chainlink Data Streams.
- Secondary: Pyth.
- Fallback quorum path: RedStone/Stork.
- Settle only when readings converge within configured tolerance.

## 4. Pool Lifecycle on Arc
1. Accept deposits and mint side tokens.
2. Lock and route funds to yield adapter.
3. Read settlement price at round end.
4. Withdraw yield-bearing assets.
5. Return principal, distribute yield to winners, route protocol fee to treasury.

## 5. Risk Controls
- Per-pool caps.
- Max round duration constraints.
- Emergency pause and withdrawal path.
- Oracle stale-data guards.

## 6. Revenue on Arc
- Yield fee routing to treasury.
- Optional market creation fees.
- Sponsor premium modules.
- Treasury idle-balance yield management.

## 7. Migration Philosophy
Do not port old contracts line-by-line. Preserve mechanism; rebuild integrations and safety controls for Arc-era requirements.
