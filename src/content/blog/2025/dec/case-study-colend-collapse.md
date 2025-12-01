---
title: "Case Study: Colend Collapse"
description: "This case study exposes how Colend’s failure to liquidate insolvent whale positions, combined with opaque, unilateral rule changes, reveals deeper structural flaws in DeFi when protocol teams hold too much discretionary power."
pubDate: "Dec 2, 2025"
heroImage: https://i.ibb.co/pvzPJrQ8/colend-events.jpg
---

For years, decentralized finance (DeFi) has marketed itself as a trustless, permissionless, rule-based alternative to traditional finance.

Smart contracts were supposed to automate execution; governance tokens were supposed to democratize control; transparency was supposed to prevent fraud.

But as the ecosystem has matured, a different reality has repeatedly surfaced: many DeFi protocols operate with **centralized chokepoints, opaque decision-making, and teams that can arbitrarily change rules when under stress**. These governance flaws often remain invisible, until the moment they cause catastrophic losses to the users.

Few recent examples illustrate this better than the collapse of **Colend**, a lending/borrowing protocol whose downfall was not simply a technical failure, but a governance failure. The main problem is this:

> **Colend’s team had excessive control over liquidation policies, collateral rules, and risk parameters, and they exercised that power in ways that ultimately harmed users.**

In this case study, we break down what happened, why it happened, and what Colend’s failure reveals about the fragile reality of DeFi governance today.

---

## What Happened with Colend?

After October 10 liquidation cascade, the Colend lending protocol on Core experienced a major stress event when the price of CORE crashed from approximately $0.38 to $0.2 within hours.

Several of the largest borrowers saw their Health Factors fall below 1.0, with some going more than $1.5 million negative. Under standard DeFi lending mechanics, such positions should have been liquidated immediately to protect depositors.

However, liquidations failed to execute because the Core DEX ecosystem only had around $1.2 million in effective stablecoin liquidity, meaning a forced sale of millions in CORE would incur massive losses due to slippage. As a result, these underwater positions remained open while whales were allowed to manually add collateral and avoid liquidation.

<div class="img-container">
  <img src="https://i.ibb.co/N2NGhvhT/colend-price.jpg" alt="CORE price on October 10">
</div>

Shortly after, Colend raised its stablecoin deposit rate to 11.85% even though the pool was already fully utilized, an unusual move made without governance oversight.

The team later explained that they had privately negotiated a repayment schedule with the largest borrowers, who agreed to return roughly $100,000 per week despite more than $11 million of user deposits being locked.

Over the following days, the team continued making parameter changes unilaterally, including increasing supply caps for CORE and stCORE twice in one week. These adjustments gave major borrowers additional time and flexibility to stabilize their positions, further reducing the likelihood of liquidation. Meanwhile, rumors circulated regarding the project team’s close ties to those same borrowers, though none were formally substantiated.

## How DeFi Lending Is Supposed to Work

At the core of every lending protocol, like Aave, Compound, MakerDAO, and numerous others, lies a straightforward logic:

1. Borrowers deposit collateral.
2. They receive loans pegged to a collateralization ratio.
3. If collateral falls below a safety threshold, **the system automatically liquidates it** to protect lenders.

This liquidation mechanism is _not optional_. It is not negotiable. It is the foundation that protects depositors from bad debt.

In a truly decentralized system:

- No core team can pause or block liquidations.
- No admin key can override risk parameters.
- No centralized committee can decide which borrowers get liquidated and which do not.
- Smart contracts enforce the rules consistently and transparently.

But DeFi does not always function that way in practice.

---

## What Happened at Colend: A Failure of Governance

Colend’s downfall was rooted in a systemic governance flaw:

**The team retained, and used, the power to arbitrarily modify liquidation logic, collateral rules, and risk thresholds.**

This power ultimately enabled actions (or non-actions) that hurt users.

### The key issues:

- **Unhealthy collateral positions were not liquidated**, even when far below required LTV thresholds.
- **Some borrowers were seemingly protected** from liquidation by discretionary decisions.
- **Bad debt accumulated silently**, without disclosure to lenders or depositors.
- **Risk parameters were changed abruptly**, without community consent.
- **The team controlled critical contracts**, allowing them to intervene (or not intervene) at will.

Colend presented itself as an automated, rules-based DeFi protocol but operated like a centralized credit desk making opaque, discretionary decisions.

---

## Why Users Lost: Governance Failures Cascade

The failure to liquidate undercollateralized positions is not just a theoretical governance problem, it is a direct financial one.

<div class="img-container">
  <img src="https://i.ibb.co/8gdbLTVL/colend-borrow-cap.jpg" alt="Colend USDT borrow capped">
</div>

By choosing _not_ to trigger liquidations, the protocol:

**1. Allowed borrowers to slip further and further underwater**

Bad debt increased daily as collateral values continued to fall.

**2. Depleted the reserve buffer meant to protect lenders**

Without liquidation revenue, the protocol lost one of its main defenses against insolvency.

**3. Forced losses onto depositors and liquidity providers**

Lenders rely on liquidation proceeds to remain whole. Without them, users absorbed the losses.

**4. Created asymmetric outcomes**

Reports suggest some borrowers effectively enjoyed “immunity” from liquidation while lenders had no such protections.

**5. Undermined all credibility**

When liquidation is optional, lending becomes arbitrary — not algorithmic.

Put simply, **the team created a two-tier system: privileged borrowers and second-class depositors.**

This is the antithesis of DeFi’s claim to fairness and decentralization.

---

## A Protocol Without Immutable Rules Is Not DeFi

The Colend collapse proves a critical point:

_If a protocol’s core risk flows can be altered by a human decision, then it is not decentralized_

DeFi is supposed to be trustless.
Colend required trust, and that trust was violated.

True DeFi requires:

- **Immutable liquidation logic**
- **Transparent, auditable governance**
- **Non-custodial control over assets**
- **Admin minimization or removal**
- **Predictable risk parameters**

Anything less becomes CeFi with a DeFi interface.

---

## How Users Can Protect Themselves

Colend teaches users what to look for, and what to avoid, when evaluating a DeFi lending protocol.

**Before depositing funds, users should ask:**

1. Is the liquidation mechanism fully automated?

If liquidations can be paused or altered by humans, it’s a red flag.

2. Who controls risk parameters?

Admin keys, multisigs, and privileged roles should be minimized, ideally removed.

3. Is the team able to protect certain borrowers?

If yes, the system is not fair or trustless.

4. Can governance decisions happen without community voting?

If the team can push emergency changes at will — beware.

5. Does the protocol disclose liquidation history?

If liquidation data is hidden, something is wrong.

---

## Final Thoughts: Colend as a Case Study

At surface level, the Colend situation appears to be a liquidation failure, but at its core, it was a **governance failure**

<div class="img-container">
  <img src="https://i.ibb.co/bMhbdPbn/colend-tvl.jpg" alt="Colend TVL crashing">
</div>

The protocol did not collapse because of market volatility.

It collapsed because:

- The team had too much centralized authority.
- They could arbitrarily change or ignore liquidation rules.
- Users had no say in risk decisions that affected their capital.
- Critical safety mechanisms were discretionary, not automatic.

This case study exposes the uncomfortable truth:

**DeFi is only as decentralized as its governance. If governance is centralized, DeFi is an illusion.**

For protocols, Colend reinforces the need for genuine decentralization.
For users, it reinforces the need for vigilance and skepticism.

Because in DeFi, as Colend showed, the difference between safety and disaster often lies not in the code, but in who controls it.
