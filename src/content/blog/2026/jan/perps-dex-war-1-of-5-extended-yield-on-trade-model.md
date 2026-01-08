---
title: "Perps DEX War (1/5): Extended’s Yield-on-Trade Model"
description: "Extended is a perp DEX built by ex-Revolut engineers that combines CEX-level speed and UX with a unique yield-on-trade margin system, letting active traders earn up to ~35% APR while they trade."
pubDate: "Jan 8, 2026"
heroImage: https://i.ibb.co/xqrMkTD9/0-extended-infographic.jpg
---

## Extended Summary

| Feature       | Rating   | Notes                                                                                                                  |
| ------------- | -------- | ---------------------------------------------------------------------------------------------------------------------- |
| Liquidity     | ⭐⭐⭐⭐ | Strong hybrid order book; however, spreads can widen significantly compared to CEXs during extreme "flash" volatility. |
| UX/UI         | ⭐⭐⭐⭐ | Industry-leading; the unified margin and "one-click" trading effectively bridge the gap between DeFi and CEXs.         |
| Yield         | ⭐⭐⭐   | XVS carries high-reward risk. 35% APR relies heavily on token emissions; sensitive to price pullbacks and inflation.   |
| Asset Variety | ⭐⭐⭐   | Good mix, but "Permitless" listings can occasionally result in low-depth markets with predatory slippage.              |
| Safety        | ⭐⭐⭐   | Non-custodial but utilizes an off-chain sequencer. The Oct '25 downtime highlights a specific point of failure.        |

If you have been tracking the decentralized derivatives market over the last two years, you know the narrative has shifted. It is no longer just about "being on-chain"; it is about beating Centralized Exchanges (CEXs) at their own game.

We are seeing a new generation of hybrid exchanges emerging, platforms that offer the latency and liquidity of Binance but with the non-custodial security of DeFi. Leading this charge in early 2026 is **Extended**.

Built by former executives from Revolut, Extended has quietly become one of the most technically impressive trading platform. With over **$100 million in TVL** and daily volumes peaking at **$1.45 billion**, it is no longer just a "promising project", it is a heavyweight contender.

<div class="img-container">
  <img src="https://i.ibb.co/Rk2qmjr9/1-extended-volume.jpg" alt="Extended perps volume">
</div>

Let's break down Extended’s architecture, its unique "Yield-on-Trade" vault mechanics, and the details of its interesting points campaign.

---

## Fintech Meets DeFi

To understand Extended, you have to look at who built it. The platform was founded by the former Head of Crypto Operations at **Revolut**, Ruslan Fakhrutdinov, a man who oversaw more than 10 million crypto users. This isn't a team of anonymous devs forking code; this is a team that understands high-performance trading infrastructure for traditional finance (TradFi).

<div class="img-container">
  <img src="https://i.ibb.co/Qvy4wg8Y/2-extended-founder.jpg" alt="Extended founder">
</div>

Launched initially as **X10** in mid-2024, the project rebranded to **Extended** and went live on the **Starknet mainnet in August 2025**. Their mission was specific: address the trust gap left by the collapse of FTX without forcing traders to suffer through the slow, clunky UX often associated with on-chain trading.

The result is a "Hybrid" model. It looks like a CEX, feels like a CEX, and executes like a CEX (sub-10ms latency), but it settles on-chain. You maintain self-custody of your assets until the moment of execution.

---

## Technical Architecture

Extended leverages Starknet’s Layer-2 scaling solution (using validity rollups) to achieve what they call "quantum-resilient" security. But for the average trader, the tech stack manifests in three tangible benefits:

### 1. Speed and Latency

The platform boasts an end-to-end order latency of **under 10 milliseconds**. If you have traded on older AMM-based perp DEXs, you know the pain of "waiting for the block." Extended eliminates this. It uses a hybrid order book model, combining off-chain matching with on-chain settlement. This prevents the Front-running and Maximal Extractable Value (MEV) exploits that plague other DEXs.

### 2. Gas-Free Trading

Because of the account abstraction and L2 architecture, users enjoy a gas-free trading experience. You sign transactions, but you aren't paying ETH gas fees for every limit order you adjust. This is critical for active market makers and day traders.

### 3. Unified Margin & Liquidity

Extended sources liquidity from both professional market makers and its own user-funded vaults (more on that later). More importantly, it offers **Unified Margin**. You can cross-margin your positions across BTC, ETH, and even meme coins. This capital efficiency is a major upgrade from the isolated margin silos found on many competitors.

---

## "Yield-on-Trade": Extended Vault Shares (XVS)

If there is one feature that sets Extended apart from competitors like Hyperliquid or dYdX, it is the **Extended Vault Shares (XVS)** system.

In traditional DeFi, you usually have to choose: _Do I trade with this capital, or do I stake it to earn yield?_ Extended solves the "idle asset" problem by allowing you to do both.

### How XVS Works

When you deposit USDC into the Extended Vault, you receive XVS. This isn't just a receipt token; it is yield-bearing collateral.

- **Collateral Utility:** You can use your XVS as margin for trading (up to **90% LTV** as of early 2026).
- **Passive Yield:** While you are trading, that collateral is still earning a **Base Yield** (approx. 5-15% APR) derived from the platform's market-making profits, liquidations, and fees.

<div class="img-container">
  <img src="https://i.ibb.co/PvKx1YFc/3-xvs-vault.jpg" alt="XVS vault">
</div>

### The "Extra Yield" Boost

This is where it gets interesting for active users.

> The platform incentivizes activity through a gamified tier system. Active traders can earn **Extra Yield** on top of the base rate, pushing total APRs up to **35%** in some weeks.

- **Tiers:** The system ranks users weekly into leagues:
  - _Pawn_ (bottom 40%)
  - _Knight_ (top 30%)
  - _Rook_ (top 15%)
  - _Queen_ (top 10%)
  - _King_ (top 5%)
- **The Kicker:** The yield multiplier accelerates non-linearly. If you are in the "King" tier, your yield on your vault collateral is significantly higher than a passive depositor.

This mechanism is brilliant because it prevents the dilution of yield by passive "farmers" while heavily rewarding the traders who actually generate volume and fees for the protocol.

---

## Trading Experience

Extended has been aggressive with its listing strategy. As of 2026, they aren't just sticking to the blue chips. They have categorized their offerings to suit different risk appetites.

<div class="img-container">
  <img src="https://i.ibb.co/YF4fKzTc/4-extended-markets.jpg" alt="Extended markets">
</div>

### Crypto Majors (50x Leverage)

BTC, ETH, and SOL. These markets have the deepest liquidity and lowest slippage. Internal analyses have shown Extended often ranks **#1 in slippage** for trade sizes between $10k and $1M against peers like Lighter.

### Alts & Memes (20-50x Leverage)

The platform has embraced the "supercycle" narrative, listing high-volatility assets like **DOGE, WIF, PEPE, MOODENG,** and **POPCAT**.

- _Note:_ In November 2025, they increased leverage limits on these assets to 50x, signaling confidence in their liquidation engine’s stability.

### TradFi Indices (10x Leverage)

For those looking to hedge macro exposure without leaving crypto, Extended offers **SPX (S&P 500)**, **NDX (NASDAQ)**, and **XAG (Silver)**. This is a massive value add for traders who want to trade the US stock market open using their USDC collateral.

### Pre-Launch Markets

They also support pre-launch tokens (like **LIT** and **MEGA**) using oracle blends. This allows traders to speculate on assets before they even hit spot markets, albeit with lower leverage (3-5x).

---

## The Airdrop Campaign

Extended has a very structured, albeit complex, rewards ecosystem. While the team often refers to it as a "Points System," the behavior strongly mimics a pre-token generation event (TGE) campaign designed to distribute future tokens.

### 1. The Points System

The core of the campaign is the weekly distribution of points.

- **Volume:** Approximately **1 million+ points** are distributed weekly to roughly 6-7k active users.
- **Epochs:** The campaign is divided into "Epochs." During specific events, such as the migration from StarkEx to Starknet or the launch of XVS, the reward pools have historically **doubled**. Keeping an eye on their discord for "Epoch shifts" is the best way to time your volume.

<div class="img-container">
  <img src="https://i.ibb.co/NdCYWvLr/5-extended-points.jpg" alt="Extended points">
</div>

### 2. Activity-Based Scoring

Points aren't just for volume. They are awarded based on a composite score of:

- **Taker Volume:** Executing market orders.
- **Maker Volume:** Providing liquidity via limit orders.
- **Vault Duration:** How long your capital stays in XVS.

### 3. Builder Codes (The "Referral" Hack)

Launched in late 2025, **Builder Codes** allow developers and power users to earn fees. If you trade through a specific frontend (like _Ready Wallet_ or the _Tengu Trade_ Telegram bot) or use a "Builder Code," you often qualify for fee discounts, while the "Builder" earns a rebate.

- _Strategy:_ If you are farming the airdrop, do not just trade on the vanilla interface. Look for a verified Builder Code or use an integrated partner like **Ready Wallet** to potentially stack additional ecosystem rewards on top of Extended points.

### 4. Reimbursement Bonuses

Following the brief downtime incident in October 2025, Extended distributed **bonus points** and cash reimbursements to affected users. This precedent suggests the team is willing to use points as a "goodwill" currency, which adds intrinsic value to holding them.

---

## The Risks: What You Need to Know

No analysis is complete without looking at the downsides. While Extended is "promising," it is not without risks.

- **Operational Resilience:** The platform experienced downtime in October 2025. While they handled the fallout well (reimbursing $500k to users), it highlighted the scaling challenges of high-throughput Starknet sequencing.

- **Oracle Risk:** Trading pre-launch assets (like MEGA) or high-volatility memes (like kBONK) relies heavily on Oracle price feeds. In extreme volatility, if an Oracle lags, liquidations can happen erroneously.

- **Regulatory Uncertainty:** Extended is pushing hard into "Fiat On-Ramps" and TradFi assets (SPX, Gold). This invites scrutiny. Unlike pure crypto-to-crypto DEXs, touching banking rails and securities indices could make them a target for stricter regulation.

---

## Comparison: Extended vs. The Field

How does it stack up against the big names?

- **vs. Hyperliquid:** Hyperliquid is the current king of market share (~10%), but Extended offers a better **native trading interface** and, arguably, superior mobile experience. Extended claims lower total execution costs (fees + slippage) than Hyperliquid's base tier.
- **vs. Lighter:** Lighter is fierce on fees (often zero-fee), but Extended wins on **asset variety**. If you want to trade Indices or Memes with unified margin, Extended is a great product to use in place of Lighter, and you get points for TGE.

---

## The "Must-Watch" DEX of 2026

Extended is successfully bridging the gap that has kept institutional volume off-chain. By combining **Revolut-tier UX**, **Starknet security**, and a **Yield-bearing margin system**, they have created a product that is genuinely "sticky."

For the airdrop hunter and the serious trader alike, the value proposition is clear:

> Why keep your capital idle on a CEX when it could be earning 30% APR + Points on Extended while you trade?

The "Perp DEX Wars" are heating up, and Extended has definitely brought the heavy artillery.
