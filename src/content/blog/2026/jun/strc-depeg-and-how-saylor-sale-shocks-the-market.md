---
title: "STRC Depeg and How Saylor's Sale Shocks The Market"
description: 'Michael Saylor selling 32 BTC shattered the "never sell" HODL narrative, triggering a sharp depeg of STRC preferred stock and cascading collateral crises across DeFi protocols like Apyx and Saturn'
pubDate: "June 11, 2026"
heroImage: https://i.ibb.co/qLP9Nrd0/0-btc-sale.jpg
---

Recently, Michael Saylor did the unthinkable: they sold Bitcoin.

While the sale was insignificant, just 32 BTC, it sent a big message that Strategy was willing to dump their BTC holding to pay off dividends obligation.

The worse thing is that Strategy's perpetual preferred stock, STRC, depegged sharply. Two of the prominent RWA DeFi projects that built on top of STRC also suffered collateral damage.

---

## The Inoculation Trade

To understand why just a sale of 32 BTC caused such carnage, we need to first understand STRC.

Strategy launched STRC as a variable-rate perpetual preferred stock. STRC was designed to act like a bond, trading near $100 par value and a dividends to investors.

And the dividend for STRC has been increasing month over month, up to 11.5% recently. It was sold as a "risk-free" way to get exposure to Strategy's Bitcoin yield.

But every DeFi user knows there's no such thing as risk-free in a high yield product. The double digit dividends put massive pressure on Strategy to pay.

Saylor tried to control the narrative before the sale that it was a strategic "inoculation." He claimed it was a controlled metehod to show the market that they were willing to sell their Bitcoin to fulfill their dividends obligation.

### The Depeg

The inoculation trade turned out to be a crack in Saylor's promise. He has spent years cultivating a HODL persona while preaching that he would never sell his Bitcoin.

He finally sold. And the community sentiment was negative.

Critics pointed out that if Strategy had to sell Bitcoin during a market dip, then the entire Digital Asset Treasury (DAT) narrative is flawed from the start.

The immediate result of the sale on STRC was a fast depeg to $97 after the sale. The stock closed as low as $93 in the following days. This was a massive red flag for a product marketed as bond-like and stable.

<div class="img-container">
  <img src="https://i.ibb.co/d4BhPN5Y/1-strc-depeg.jpg" alt="STRC Depeg">
</div>

---

## 1st Casualty: Apyx

The first domino to fall was Apyx, a protocol that bills itself as the first Dividend-Backed Stablecoin (DBS) protocol. Apyx has a stablecoin called apxUSD, but when STRC depegged, the value of apxUSD fell to $0.93.

For users who had parked their capital in Apyx to capture a seemingly risk-free 13% APY, seeing their stablecoin trade at a 7% discount was a harsh awakening. Many users who were burned by the LUNA catastrophe quickly withdrew their money.

<div class="img-container">
  <img src="https://i.ibb.co/C3mTChjg/2-apxusd-depeg.jpg" alt="apxUSD Depeg">
</div>

The incident highlighted a fundamental vulnerability. Apyx is custodial at its core; the underlying STRC sits off-chain in traditional brokerage accounts.

When the collateral's market price drops, the over-collateralization ratio is threatened, forcing the protocol to rely on market arbitrageurs to restore the peg, which can easily fail during market stress.

## 2nd Casualty

While Apyx suffered a direct depeg of its base stablecoin, Saturn faced a more complex contagion effect. Saturn is a stablecoin yield protocol aiming to Strategy's STRC yield on-chain.

Saturn utilizes a dual-token structure: USDat, a non-yielding stablecoin, and sUSDat, the yield-bearing token that captures the dividends from STRC.

When STRC depegged, the value of the tokenized digital credit backing Saturn’s ecosystem wobbled. While USDat claims to be backed 100% by tokenized treasuries and credit, the secondary market for sUSDat and the yield tokens took a massive hit. If STRC’s underlying value drops, the future dividend payouts that sUSDat holders are expecting are suddenly at risk.

<div class="img-container">
  <img src="https://i.ibb.co/v4xrMqxY/3-susdat-depeg.jpg" alt="sUSDat Depeg">
</div>

The panic selling of these yield-bearing tokens dragged the entire Saturn ecosystem into the red, proving that even with sophisticated tranching, systemic collateral risk cannot be entirely engineered away.

---

## The Road Ahead for RWA Yields

The STRC depeg and the subsequent wobbles at Apyx and Saturn serve as a massive stress test for the RWA credit sector.

Both Apyx and Saturn are heavily, if not exclusively, reliant on Strategy’s STRC. If Strategy mismanages its Bitcoin treasury, faces regulatory crackdowns, or if MSTR stock enters a death spiral, STRC will follow, taking Apyx and Saturn down with it. They have replaced "smart contract risk" with "Michael Saylor risk."

If Bitcoin enters a prolonged bear market, Strategy might be forced to sell more BTC to maintain the 11.5% dividend. This creates a vicious cycle: selling BTC depresses the price, which further strains Strategy's balance sheet, leading to more BTC sales, and potentially causing STRC to permanently depeg.

Apyx and Saturn have proven that the technology to tokenize corporate credit works, and the demand for double-digit on-chain yield is insatiable. However, they have also learned a brutal lesson: there is no such thing as "risk-free yields" in crypto. As these protocols move forward, they must diversify their collateral baskets beyond a single company, improve their liquidation mechanisms, and prepare users for the reality that "RWA credit" still carries the same volatility as the digital assets that back it.
