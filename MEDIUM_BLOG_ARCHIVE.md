# Entropyfi Medium Blog Archive

Complete collection of Entropyfi's Medium articles from 2021-2022.

## Table of Contents

1. [Birth of Entropy](#birth-of-entropy) — Aug 30, 2021
2. [Entropyfi Announces Public Mainnet Launch on Polygon](#mainnet-launch) — Nov 3, 2021
3. [Entropyfi Receives Aave Grants](#aave-grants) — Nov 15, 2021
4. [Chainlink Price Feeds & Keepers Integration](#chainlink-integration) — Nov 22, 2021
5. [Official EntropyFi Airdrop](#official-airdrop) — Jan 5, 2022
6. [Chainlink Keepers Engineering](#chainlink-keepers) — Jan 4, 2022
7. [Entropyfi <> VESQ AMA Recap](#vesq-ama) — Jan 20, 2022
8. [Oasis Network Partnership](#oasis-partnership) — Jun 20, 2022

---

## Birth of Entropy {#birth-of-entropy}

**Published:** July 30, 2021  
**Author:** Entropyfi  
**Read time:** 2 min

### Mission Statement

Today is July 30th, 2021. BTC price is $41,509.47

When we ask a question like: "Do you think BTC will reach $42K by the end of the week?"

One might say: "Yes! All the indicators show it's uptrend, there's no reason for the price to drop."

One might say: "No, because my fortune teller told me so."

No matter what speculation or reason is, Entropyfi believes all your price predictions should be turned into actions.

### The Core Problem

It's heartbreaking to us that you have to feel bad **AND** pay after losing a prediction game.

Entropyfi also believes that **no matter what the outcome is, it's just a speculation, even if your prediction is not right, you don't have to lose anything.** It's just a game!

### Why We Built This

Our game is perfect for chart readers and hodlers to generate some income off their prediction skills, all without the risk of liquidation.

Other than posting price prediction on Twitter every 3 hours, we want to be validated when the prediction hits right. It's more about feeling good, and the APY is the gravy.

And yes… That's how Entropy was born.

We are a bunch of peeps that are always down for a good time, competitive, and want to avoid the liquidation risk of trading contracts.

### Game Design

The game logic is super simple:
- If you win the prediction, you win some back
- If you lose the game, you can either withdraw the full amount or keep playing

We also added the compound feature so you don't have to manually input every week unless you would like to change your decision.

### Our Mission

**Our mission is as simple as creating a lossless prediction market for you to predict the price without losing your principal.**

Launching our product any minute now, join the community for updates on launch date and airdrops!

---

## Entropyfi Announces Public Mainnet Launch on Polygon {#mainnet-launch}

**Published:** November 3, 2021  
**Author:** Entropyfi

### The Announcement

Entropyfi, a crowd wisdom machine built on lossless prediction markets in the DeFi space, is thrilled to announce the launch of its much-anticipated mainnet on November 3rd.

With full prediction and sponsorship features on Polygon, users can enjoy fun prediction games with lower transaction costs.

### Background

The mainnet launch comes just a week after Entropyfi raised $1.6 million on DLM (Deversifi launch market) and 2 rounds of ITO on Mask Network.

The mainnet is the culmination of over 6 months of hard work, continuous development, and testing.

### Product Launch

The first product is a self-amplifying prediction game which allows users to amplify their yield in a low risk manner.

Entropyfi offers crypto asset price prediction games and differentiates itself with the lossless function.

**Lossless means it removes the financial disincentive that penalizes users who make wrong predictions.**

Instead, Entropyfi utilizes the yield on deposit pools to reward winners.

### Why This Matters

With a better aligned financial incentive design, Entropyfi is able to scale the prediction market and provide a more reliable and scalable crowd wisdom sourcing machine.

Traditional prediction markets are loss-realized, meaning users will take a loss on their principal if they made the incorrect prediction. The loss-realized characteristics make it difficult for traditional prediction markets to scale, as users who suffered loss might stop engaging with the product.

Entropyfi allows users to engage in prediction market without risking their principal.

### Roadmap

Entropyfi plans to launch on Ethereum and add more prediction/insurance games in the coming months.

For more information, visit https://entropyfi.com/ or follow @Entropyfi on Twitter.

---

## Entropyfi Receives Aave Grants To Build Self-Amplifying Prediction Games {#aave-grants}

**Published:** November 15, 2021  
**Author:** Entropyfi

### Partnership with Aave

EntropyFi is delighted to announce an official collaboration with Aave. As of Q4 2021, Entropyfi has been incorporated into the Aave ecosystem and supported by the **Aave Community Grants Program**.

EntropyFi is thrilled to be part of the crypto revolution to onboard the next 1 billion Web 3.0 users with lossless prediction games.

### Grant Details

The $10K grant will be used to kickstart the development of our second product: **lossless insurance** for those in the crypto community and CeFi seeking to hedge their risks.

EntropyFi will also be expanding our team by hiring smart contract developers and expanding our operations to reach a larger audience.

### Current Status

Currently, EntropyFi has released self-amplifying prediction games on Polygon Mainnet.

Our protocol uses Aave as the official yield generating partner to reward winners who predict pool results correctly.

### Future Plans

EntropyFi is looking forward to collaborating with Aave to grow their pools by:
- Increasing TVL
- Increasing borrow activity
- Increasing unique address interactions

---

## Entropyfi Using Chainlink Price Feeds and Chainlink Keepers {#chainlink-integration}

**Published:** November 22, 2021  
**Author:** Entropyfi

### Oracle Integration

We're excited to announce that Entropyfi is now using **Chainlink Price Feeds** for our Polygon Mainnet launch as our go-to oracle solution for price data within our amplified prediction games.

We're also using **Chainlink Keepers** to automate our smart contract workflow for starting/ending prediction markets and calculating users' profits.

### Why Chainlink?

Entropyfi offers prediction games on crypto-assets, NFTs, DeFi indexes, and other on/off-chain assets which rewards users with amplified yields.

Users have the opportunity to profit from market movements with zero loss to their wager by depositing assets into Entropyfi. Assets are then deposited into yield-generating platforms to generate interest.

Winners of the prediction market will then receive the interest earned by the pool, while all users — regardless if they win or not — will get back their principal.

### The Challenge

A key requirement for Entropyfi is the accurate retrieval of relevant prices at the start and settlement of the prediction round.

Since Entropyfi provides prediction games on both crypto and non-crypto assets, a time-tested oracle solution that can fetch high-quality data from a range of asset types is key to our application.

Each lossless prediction game has:
- Start date
- Contribution cut off date
- Settlement date

The prediction index price (e.g., "Will Bitcoin be higher than $X at the end of next week?") is set at the start of the game.

Users can only contribute funds between the start date and the contribution cutoff date.

At the settlement date, the smart contract needs to be called to calculate the profit for users.

### Solution

Chainlink Price Feeds provide the prices needed to establish an index price at the start date and calculate profits/losses at the settlement date.

Chainlink Keepers automate calls to the smart contracts in order to trigger the contribution period and settlement period.

### Why We Chose Chainlink

Being a lossless prediction game, Entropyfi relies on accurate, up-to-date price feeds to start prediction games and help ensure fair settlement in both a timely and tamper-proof manner.

In addition, Entropyfi will be deployed on multiple scaling solutions as well, so we needed a blockchain-agnostic oracle solution that can accommodate these flexibility requirements.

After researching and comparing multiple oracle solutions, the Entropyfi team chose Chainlink Price Feeds due to:
- Superior data quality
- Robust infrastructure
- Native support for numerous blockchains and L2s

For smart contract automation, we also compared alternative solutions and found Chainlink Keepers to provide very clear documentation and thorough explanation on its pricing structure.

### Benefits

Some of the unique benefits of integrating Chainlink's decentralized services include:

**High-Quality Data** — Chainlink Price Feeds source data from numerous premium data aggregators, leading to price data that's aggregated from multiple sources and backed by a decentralized network of nodes.

---

## Official EntropyFi Airdrop {#official-airdrop}

**Published:** January 5, 2022  
**Author:** Entropyfi  
**Source:** welcometoentropyfi.medium.com

### Welcome to the Airdrop

Welcome to EntropyFi, the first Loss-Less Prediction Market to allow you to supercharge your yield on predictions placed, games played, and more!

To promote the launch of our mainnet and to gain further community feedback on our Prediction Market dApp, we're running an official airdrop campaign.

### Why a New Campaign?

We did a previous airdrop a few days ago, but we assumed anti-spam tools were going to save us from bot attacks via Twitter and Telegram. Unfortunately, they were ineffective.

We decided that any real entries from real people would be completely drowned out, so we created a new campaign with:
- Proper anti-spam measures
- CAPTCHAs
- Dedicated moderators

### How to Participate

First, you must sign into the official contest at the entry link.

#### Free Entry
By just entering the airdrop, you get a free entry.

#### Additional Entries
By providing your Ethereum address, you get a second entry and access to the full list of actions that can earn you more entries.

These additional entries consist of basic participation within the community:
- Playing a game in the dApp
- Joining the official Telegram channel
- Following EntropyFi on Twitter
- And more!

### Questions?

"I entered in the last Airdrop Campaign. Did my entries disappear?"

Yes they are gone, but you will statistically have a better chance to win without thousands of bots watering down your real entries.

### Get Help

We are most active in:
- Telegram
- Discord
- Twitter

Ask us anything about the Official Airdrop or EntropyFi!

---

## Entropyfi Saves Engineering Hours with Chainlink Keepers {#chainlink-keepers}

**Published:** January 4, 2022  
**Author:** Entropyfi

### What is Entropyfi?

Entropyfi is a gamified staking platform that offers competitive, reward-boosted games to users.

**In Entropyfi 1.0**, players stake stablecoins, and the rewards are funded with the yield.

**In Entropyfi 2.0** (launching Q1 2022), players stake $ERP, and the rewards are funded with a protocol-controlled vault.

Entropyfi 2.0 will also release a PRO version for partners and offer a more sustainable, healthy locking mechanism for our partner projects.

### The Problem

Entropyfi is currently offering many gamified yield opportunities to users. These games require periodical triggering of the "start" and "settlement" functions.

A common practice is for developers to setup scripts in the cloud and call the functions. Yet this poses a centralization risk, as an interruption at the cloud service provider could also interrupt the dapp operation.

Entropyfi developers want to streamline and decentralize these operations tasks.

### The Solution: Chainlink Keepers

One of the co-founders of Entropyfi is a longtime admirer of Chainlink services, hence he recommended Chainlink Keepers to the development team.

As the team had previously integrated Chainlink Price Feeds into Entropyfi, the integration of Chainlink Keepers into Entropyfi was a breeze.

### Impact

Integrating with Chainlink Keepers has significantly reduced the repetitive operational work that the Entropyfi team has to do.

**Currently, Entropyfi has 9 live prediction games, with each settling 5 days apart.**

**By integrating Chainlink Keepers, the team was able to save 20 engineering hours per week.**

### Implementation

Chainlink Keepers provide an easy-to-use solution for enabling automated smart contract execution.

Adapting our smart contract and making it Keepers-compatible was easy. Our developers only had to write two wrapper functions:
1. One for checking the execution condition
2. One for executing the function

### Biggest User on Polygon

Entropyfi is currently the biggest user of Chainlink Keepers on Polygon network!

### Support & Partnership

It's been a breeze working with the Chainlink Labs team, who supported us with this integration.

During the initial integration of Keepers, we ran into some issues with setting the proper gas limit for our keeper tasks. The Chainlink Labs team was able to swiftly answer our developers' questions.

We appreciate the high level of support that the Chainlink Labs team has offered.

### Future Vision

Currently, Entropyfi is the biggest user of Chainlink Keepers on the Polygon network.

As we expand to other networks, we hope that Chainlink Keepers will also support these new and upcoming networks, as many other developers could also benefit from a trustable, reliable, and decentralized smart contract operation toolkit.

Entropyfi is building a hyper-competitive platform offering gamified yields.

Entropyfi's vision is to transform the staking into a thrilling experience and to entice long-term hodlers with our unique hodl-to-earn (H2E) mechanism.

---

## Entropyfi <> VESQ AMA Recap {#vesq-ama}

**Published:** January 20, 2022  
**Author:** Entropyfi

### Event

We'd like to say massive thanks to all of you who joined the AMA today at VESQ's Discord channel. We had so much fun!

If you missed this AMA, don't worry — we'll be scheduling more AMAs with different communities and will announce them on our social channels.

### Entropyfi's Vision

Entropyfi is building a hyper-competitive platform offering gamified yields.

Entropyfi's vision is to transform the staking into a thrilling experience and to entice long-term hodlers with our unique **hodl-to-earn (H2E)** mechanism.

### Entropyfi 2.0

With Entropyfi 2.0 launching right around the corner, we invite you to follow us for the latest information.

### Learn More

To learn more about Entropyfi:
- Visit our website
- Visit our Medium
- Visit Entropyfi's Gitbook for developer guide and user guide
- Follow our Twitter
- Join our Telegram and Discord community

---

## Oasis Network Welcomes Entropyfi 2.0 H2E Games {#oasis-partnership}

**Published:** June 20, 2022  
**Author:** Oasis Foundation  
**Reposted:** On Oasis blog

### Partnership Announcement

Oasis Network is excited to announce that **Entropyfi 2.0 H2E (hodl-to-earn) games will be deployed on Emerald**, our EVM compatible ParaTime in February.

As part of Oasis Grant recipient, Entropyfi's multi-chain development, this integration will increase:
- Interoperability for Entropyfi 2.0 H2E games
- The entire DeFi ecosystem as a whole

### About Entropyfi

Entropyfi is building a hyper-competitive platform offering gamified yields.

**Entropyfi's vision:** Transform the staking into a thrilling experience and entice long-term hodlers with their unique **hodl-to-earn (H2E) mechanism**.

### H2E Innovation

**Entropyfi 2.0 is the first protocol to showcase the H2E mechanism**, which allows users to farm and collect stablecoins with governance tokens they have already been hodling.

This represents a major evolution in how yield farming and staking rewards work in DeFi.

### Impact

This deployment on Oasis Emerald represents Entropyfi's commitment to multi-chain growth and brings innovative yield farming mechanics to the Oasis ecosystem.

---

## Key Themes Across All Posts

### 1. Lossless Innovation
Every post emphasizes the core mechanic: **users cannot lose their principal**. This is the defining feature that differentiates Entropyfi from traditional prediction markets.

### 2. Yield-Driven Gaming
The concept of turning yield into rewards for winners is central to the product vision.

### 3. Partnerships
Entropyfi actively partnered with:
- **Aave** — for yield generation
- **Chainlink** — for oracles and automation
- **Oasis** — for multi-chain expansion
- **Mask Network** — for token distribution

### 4. Community-First Approach
Every announcement includes community links and emphasizes engagement through Telegram, Discord, and Twitter.

### 5. Multi-Chain Vision
From the start, Entropyfi planned to expand beyond Polygon to Ethereum, Oasis, and other networks.

### 6. Hodl-to-Earn (H2E) Evolution
Over time, Entropyfi 2.0 evolved toward a "hodl-to-earn" model where users could earn rewards by holding governance tokens ($ERP).

---

## Publishing Timeline

| Date | Article | Key Milestone |
|---|---|---|
| Jul 30, 2021 | Birth of Entropy | Vision articulation |
| Nov 3, 2021 | Mainnet Launch | Polygon live |
| Nov 15, 2021 | Aave Grants | Institutional validation |
| Nov 22, 2021 | Chainlink Integration | Oracle integration |
| Jan 4, 2022 | Chainlink Keepers | Automation, 20 hrs/week saved |
| Jan 5, 2022 | Official Airdrop | Community incentives |
| Jan 20, 2022 | VESQ AMA | Community engagement |
| Jun 20, 2022 | Oasis Partnership | Multi-chain expansion |

---

## What Happened After?

Based on the blog archive, posts stop in June 2022. The project likely faced challenges in 2022:
- Bear market (June 2022 collapse)
- Team focus shift toward Entropyfi 2.0 H2E
- Eventually led to project wind-down

The last update mentioned "Entropyfi 2.0 H2E coming soon" but never materialized in public posts.

---

## Full Links

All original articles linked to medium.com/entropyfi:
- https://medium.com/entropyfi (main publication)
- https://welcometoentropyfi.medium.com (alternate account)

---

**Archive Date:** May 2026  
**Collection:** Complete Medium blog, 2021-2022
