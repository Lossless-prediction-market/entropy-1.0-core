# Morpho Blue Integration Guide — LossLess Labs

## 1. Why Morpho Blue
Morpho Blue gives isolated market design, allowing per-pool risk isolation. This maps well to prediction pools where each market should have bounded, independent exposure.

## 2. Architecture Mapping
- Pool contract owns yield position.
- Yield adapter supplies/withdraws using standardized interface.
- Adapter maintains market params per pool.

## 3. Aave → Morpho Conceptual Rewrite
### Old pattern
- `deposit` into Aave LendingPool.
- Hold/track via aToken balance semantics.

### New pattern
- `supply` into Morpho with market params.
- Track value through share accounting.
- `withdraw` by amount or share at settlement.

## 4. NAV Calculation
- Internal NAV = principal + realized/realizable yield from adapter.
- Per-side token values update at settlement with winner-side yield allocation.

## 5. Fallback Strategy
If Morpho adapter fails capacity/routing checks, fallback to Aave adapter when enabled by governance. All fallback events should emit explicit routing logs.

## 6. Testing Plan
- Unit test adapter math and rounding.
- Integration test round lock/settle across mock Morpho.
- Invariant test principal safety across random sequences.
- Differential test against legacy Entropyfi expected outcomes for round accounting.

## 7. Recommendation
Launch with Morpho Blue primary path and a constrained fallback route. Keep adapter interfaces stable so new yield venues can be added without rewriting pool core.
