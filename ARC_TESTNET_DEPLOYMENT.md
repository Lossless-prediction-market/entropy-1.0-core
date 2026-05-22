# LossLess Labs — Arc Testnet Deployment Guide

## Network Configuration
- Chain ID: `5042002`
- RPC: `https://rpc.testnet.arc.network`
- WS: `wss://rpc.testnet.arc.network`
- Explorer: `https://testnet.arcscan.app`
- Faucet: `https://faucet.circle.com`

## Phase 0 — Setup
```bash
node --version
git --version
forge --version
```

Foundry `foundry.toml`:
```toml
[rpc_endpoints]
arc_testnet = "https://rpc.testnet.arc.network"
```

## Phase 1 — Contracts
- Compile modernized pool, factory, token, oracle adapter, and yield adapter contracts.
- Configure USDC testnet token and treasury params.

## Phase 2 — Deployment Order
1. Governance token / admin controls.
2. Factory.
3. Yield adapter (Morpho or mock).
4. Oracle adapter.
5. Pool template.
6. Create first pool instance.

Example call (factory pool creation shape will depend on final ABI):
```bash
cast send $FACTORY "createPool(...)" ... --rpc-url https://rpc.testnet.arc.network --private-key $PRIVATE_KEY
```

## Phase 3 — Integration Checks
- Deposit Long/Short.
- Lock round.
- Settle using oracle adapter.
- Validate principal redemption and winner-yield distribution.
- Validate treasury fee receipt.

## Phase 4 — Gas Benchmarking
```bash
cast estimate $POOL "deposit(uint256,uint256)" 1000000 0 --rpc-url https://rpc.testnet.arc.network
```

## Phase 5 — Security Checklist
- Reentrancy guards on mutative paths.
- Oracle staleness checks.
- Fee cap enforcement.
- Principal-protection invariant tests.
- Emergency pause behavior tested.

## Notes
Where live testnet addresses for third-party protocols are missing, mark as `TBD` and use deterministic mocks during integration.
