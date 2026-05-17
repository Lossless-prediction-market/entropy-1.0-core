# Deployed Contracts

## Network Availability

Entropyfi is deployed on three networks:

- **Polygon (Matic) Mainnet** — Production
- **Polygon (Mumbai) Testnet** — Testing
- **Ethereum Kovan Testnet** — Testing (legacy)

## Polygon Mainnet Contracts

### Core Protocol

| Contract | Address |
|---|---|
| Entropy V1 Factory | 0xeff87121ab94457789495918eef5a5904eb04419 |

### Prediction Market Pools

#### BTC Pairs
| Asset Pair | Contract Address |
|---|---|
| BTC-USDT | 0x637958F16fd1c79695206a9af8bEe7c0aC242B6E |
| BTC-USDC | 0x22Faf1F97DeA1b4BCf87A2DAa6Ab0e56659E5F03 |
| BTC-DAI | 0xe5545b8009E6CfaeBb9C2A14d3D0a674d87edF1B |

#### TSLA Pairs
| Asset Pair | Contract Address |
|---|---|
| TSLA-USDT | 0xa8653EA964441EBc93c901D7B2429A87B4871B87 |
| TSLA-USDC | 0x0147F0915D3115e47686BE0571795e2f7fD27F77 |
| TSLA-DAI | 0x3eab615FB407f47D1C4A3340D131917Bc8a49da0 |

#### OHM Pairs
| Asset Pair | Contract Address |
|---|---|
| OHM-USDT | 0xFeD532aE45BE055ACB999491fA2e622C81dA0495 |
| OHM-USDC | 0x02424F62c6e16A8aE84777ea096ed7Fa9F25fC68 |
| OHM-DAI | 0x047e3D496ce636c05DBc6A877749Ed98193D090e |

### Farming Contracts

| Contract | Address |
|---|---|
| Sponsor Farm | 0xb956B861BD97bf5195Eb4AA09d5c5EAD1B2e4514 |
| LP Farm | 0x7ace9872ee80145ad7b4d93cf8D84D664c450Ea5 |

### ERP Token

| Network | Address |
|---|---|
| Polygon | 0x28accA4ed2F6186c3D93e20e29e6e6a9Af656341 |
| Ethereum | 0x0a0e3bfD5a8cE610E735D4469Bc1b3b130402267 |

### Principal Tokens (Stablecoins)

| Token | Address | Decimals |
|---|---|---|
| USDT | 0xc2132d05d31c914a87c6611c10748aeb04b58e8f | 6 |
| USDC | 0x2791bca1f2de4661ed88a30c99a7a9449aa84174 | 6 |
| DAI | 0x8f3cf7ad23cd3cadbd9735aff958023239c6a063 | 18 |

---

## Polygon Mumbai Testnet Contracts

### Core Protocol

| Contract | Address |
|---|---|
| Entropy V1 Factory | 0x0b272a52E64542C7B2bfe001fFe6EaD1Ae24c4B8 |

### BTC Pairs (Mumbai)

| Asset Pair | Contract Address |
|---|---|
| BTC-USDT | 0x3a123D3AA9cBd4F6e04A444595911055945Ab7F8 |
| BTC-USDC | 0xE90648A054D6008633a6f6f61b9DcB734E2A76B9 |
| BTC-DAI | 0xf64A88fF8e7420cd755dc7554e42a7B1BfBDeaCd |

### Farming Contracts (Mumbai)

| Contract | Address |
|---|---|
| Sponsor Farm | 0x35983140e2477F797343f376B59689B94da1a87D |
| LP Farm | 0x655fD28E66b64a7649d046343aa7d475ade9B3e7 |

### Principal Tokens (Mumbai)

| Token | Address | Decimals |
|---|---|---|
| USDT | 0xBD21A10F619BE90d6066c941b04e340841F1F989 | 6 |
| USDC | 0x2058A9D7613eEE744279e3856Ef0eAda5FCbaA7e | 6 |
| DAI | 0x001B3B4d0F3714Ca98ba10F6042DaEbF0B1B7b6F | 18 |

---

## Ethereum Kovan Testnet Contracts

### Core Protocol

| Contract | Address |
|---|---|
| Entropy V1 Factory | 0x9c955d3deb8696F1753388068dC9480B1441F0ea |

### BTC Pairs (Kovan)

| Asset Pair | Contract Address |
|---|---|
| BTC-USDT | 0xc0b12d35B26450e45DcBd35D5f9bec81C771Ab08 |
| BTC-USDC | 0xA021911835198CA418568467c7b9888C7A1CC088 |
| BTC-DAI | 0xf62e1729a44F74Cc76Eb59E1c138525CEDfC9C34 |

### Gas Pairs (Kovan)

| Asset Pair | Contract Address |
|---|---|
| ETH-GAS-USDT | 0xD94cB7131e6cB9255d73E1d51777bc67831625fe |
| ETH-GAS-USDC | 0x171B27611C1Da847b3B11C5c5f65F76466875b53 |
| ETH-GAS-DAI | 0x53f641aC198D6c676Af7a8b9395BB693d36E061C |

### Farming Contracts (Kovan)

| Contract | Address |
|---|---|
| Sponsor Farm | 0x159e02795eaD816cE0792F932BE7B36444F82dC6 |
| LP Farm | None (not deployed on Kovan) |

---

## Game Token Addresses

### Pool Tokens (Long/Short)

Pool tokens represent user positions in prediction markets. Each pool has unique long and short tokens.

**Example: BTC-USDT Pool on Polygon Mainnet**

| Token Type | Token Name | Address | Decimals |
|---|---|---|---|
| Long | lgBTC-USDT | 0xead11797ce0f858bebdcbc01758e5e366619d6e3 | 6 |
| Short | stBTC-USDT | 0xd735edfa617eaf8c102716c0b8cf862a0e880d6f | 6 |

**Example: OHM-USDC Pool on Polygon Mainnet**

| Token Type | Token Name | Address | Decimals |
|---|---|---|---|
| Long | lgOHM-USDC | 0xcb14b880153d7930b0edacaf17a6303eba7c075d | 6 |
| Short | stOHM-USDC | 0x652b01b7d2e876ca5e954076297770419b69f810 | 6 |

### Sponsor Tokens (Pool-Specific)

Sponsor tokens represent your share of sponsor deposits in a pool.

**Example Sponsor Tokens on Polygon Mainnet**

| Pool | Sponsor Token | Address | Decimals |
|---|---|---|---|
| spBTC-USDT | spBTC-USDT | 0x8691332a75d5043405dd1e7885f9af15417c570d | 6 |
| spBTC-USDC | spBTC-USDC | 0x14703d2f6307c2927373fecf70f14943488c89fd | 6 |
| spBTC-DAI | spBTC-DAI | 0xaeb78f8a16bdbda37816cc5be97f9aabf4cdcdac | 18 |
| spTSLA-USDT | spTSLA-USDT | 0x8c6aa86fab7dad13f73e0873a2b496ddadc6361e | 6 |
| spOHM-USDT | spOHM-USDT | 0xc6aaf7a2f7d2f08eaa7645cfadb48df1fd657cc4 | 6 |

---

## Entropyfi (50,50) Contracts

### VSQ (VESQ) Rebase Token (Polygon Mainnet)

| Token Type | Token Name | Address | Decimals |
|---|---|---|---|
| Long/Leverage | LEV-VSQ-V2 | 0xC032Cfa00A35945a3DDb6E2a073cae729056ce74 | 9 |
| Short/Hedge | HGE-VSQ-V2 | 0xe1a2E5C089668BF4932a119c1c299857BDC276bE | 9 |

---

## Liquidity Pools

### Uniswap (Ethereum Mainnet)

| Pair | Address |
|---|---|
| ERP-USDC | On Uniswap |

### Quickswap (Polygon Mainnet)

| Pair | Address |
|---|---|
| ERP-USDC | On Quickswap |

### LP Lock Contracts

| Network | Lock Address | Lock Tx |
|---|---|---|
| Ethereum (Uniswap) | 0xc84eb75bA2c20De72C929CC2Fd73B937F8997919 | [Etherscan](https://etherscan.io/tx/0x0ab68dbb76933adda263a9205ff179ec4bc9a7583ce91a10dfa666dac333295c) |
| Polygon (Quickswap) | 0x02F1410457CEB105Ca8aed71b7654FB05CB61417 | [Polygonscan](https://polygonscan.com/tx/0xbd3b4c63c5236f703f7ef7dd84bdb8a87582e9c9ca6fb6927195aadd0953991e) |

---

## Integration Notes

### Using Pool Contracts

When interacting with pool contracts directly:

1. **Deposit** — Send collateral, receive long/short tokens
2. **Swap** — Burn long tokens, mint short tokens (or vice versa)
3. **Withdraw** — Burn pool tokens, receive collateral

### Using Farming Contracts

1. **Sponsor Farm** — Stake sponsor tokens, earn ERP
2. **LP Farm** — Stake LP tokens, earn ERP

### Oracle Data

All price feeds are sourced from **Chainlink Price Feeds**, which provides decentralized, high-quality price data.

### Settlement Automation

**Chainlink Keepers** automatically trigger:
- Round starts (lock pool, supply to Aave)
- Round ends (calculate winners, update NAV)
- Reward distribution

---

## Verification & Security

All major contracts are verified on Etherscan/Polygonscan. You can view and audit the source code directly:

- **Polygonscan** (Polygon): https://polygonscan.com
- **Etherscan** (Ethereum): https://etherscan.io

Look up any contract address to view verified source code, transactions, and interactions.

---

## Deprecated Contracts

The following contracts are no longer actively used:

- Kovan Testnet (legacy Ethereum testnet)
- Old Liquidity Mining contracts (replaced by Vault Inc)

For new integrations, use Polygon Mainnet or fresh Polygon Mumbai testnet contracts.

---

## Getting Testnet Tokens

To test on Mumbai or Kovan, claim testnet tokens from the appropriate faucet:

- **USDT**: Testnet faucet
- **USDC**: Testnet faucet  
- **DAI**: Testnet faucet

See [Testnet Setup Guide](../getting-started/testnet-tokens.md) for detailed instructions.
