# OPSA Agent Building Blocks — Sales × Procurement

## The Core Equation

A wholesaler's entire business comes down to one thing:

**Buy at the right price → Sell at a higher price → Protect the margin in between**

Right now the landing page has three building blocks — all on the sell side. To tell the full story (even if procurement ships later), you need to map both sides and, critically, the block that connects them.

---

## SALES SIDE — "Sell at a Higher Price"

These are the current blocks. They answer: **who do I sell to, how do I reach them, and how do I close?**

| # | Block | What It Does (Wholesaler Terms) | Key Interactions |
|---|---|---|---|
| S1 | **Buyer Finder** (currently: Researcher) | Scans your ERP, buyer lists, and market data to find accounts ready to order — new prospects, dormant accounts coming back to season, buyers whose competitors just stocked up. | Feeds targets → S2. Receives "what's in stock and at what margin" from **P4** (Margin Pilot). |
| S2 | **Outreach Rep** (currently: Sales Rep) | Sends personalized offers by email/WhatsApp. Handles follow-ups. Answers product questions. Keeps the conversation going until the buyer is ready to talk price. | Receives targets from S1. Hands warm leads → S3. Uses catalog/pricing from **M1** (Catalog Brain). |
| S3 | **Deal Closer** (currently: Deal Maker) | Negotiates pricing within your rules, generates quotes, handles pushback, and books the order in your ERP. | Receives warm leads from S2. Checks margin floor with **P4** (Margin Pilot). Confirms inventory availability with **P2** (Stock Watcher). |

**What's missing on the sell side?** These three blocks cover the outbound sales motion well. But they're blind to two things: (1) what the product actually cost you (so they might sell at thin margin), and (2) what's about to run out of stock (so they might sell something you can't fulfill). Those answers come from the procurement side and the connector block.

---

## PROCUREMENT SIDE — "Buy at a Lower Price"

These blocks answer: **what do I need to buy, who do I buy from, and how do I get a better deal?**

| # | Block | What It Does (Wholesaler Terms) | Key Interactions |
|---|---|---|---|
| P1 | **Demand Reader** | Looks at sales velocity, seasonal patterns, open quotes from S3, and upcoming commitments to predict what you'll need to stock in the next 2–4 weeks. Not just "what's low" — "what's about to move." | Reads from S1 (what buyers are being targeted), S3 (open deals/quotes). Feeds restock needs → P2 and P3. |
| P2 | **Stock Watcher** | Monitors real-time inventory levels against the demand forecast. Flags when SKUs are running low, when slow-movers are tying up cash, and when overstock creates a clearance opportunity (which feeds back to S1 as a sell-through campaign). | Receives demand forecast from P1. Alerts S1 ("push these SKUs — we're overstocked"). Triggers P3 when restock is needed. |
| P3 | **Supplier Negotiator** | Finds the best price across your approved suppliers for what you need to buy. Compares quotes, checks lead times, negotiates volume discounts or early-pay terms. Places the PO. | Receives restock needs from P2. Checks margin targets from P4 before committing. Sends cost-basis data → P4. |

**Why these three?** They mirror the sales side structurally:
- P1 (Demand Reader) ↔ S1 (Buyer Finder) — both are about "where's the opportunity?"
- P2 (Stock Watcher) ↔ S2 (Outreach Rep) — both are about "keeping things moving"
- P3 (Supplier Negotiator) ↔ S3 (Deal Closer) — both are about "getting the best price"

---

## THE MISSING BLOCK — The Connector

Here's the gap. Right now, sales and procurement in most wholesale businesses operate in silos. The sales guy doesn't know what the buyer paid for the product. The purchasing manager doesn't know what deals are in the pipeline. Margin gets squeezed from both ends with nobody optimizing the middle.

| # | Block | What It Does | Why It's the Missing Piece |
|---|---|---|---|
| **M1** | **Margin Pilot** | Sits between Sales and Procurement. It knows the cost basis of every SKU (from P3), the sell price and margin rules (from S3), and the demand forecast (from P1). It dynamically sets the **margin floor** for every deal and the **cost ceiling** for every purchase. | **This is the block that makes the two sides talk.** Without it, S3 might close a deal at 12% margin when your cost just went up. Or P3 might pass on a bulk discount because it doesn't know S1 just identified 40 buyers for that SKU. |

**What the Margin Pilot does in practice:**

1. **Tells Sales what to push.** "You just got a 20% discount on SKU X from the supplier. Your margin on this is now 35% instead of 18%. Push it." → Triggers S1 to find buyers for SKU X, S2 to send offers.

2. **Tells Procurement what to stock.** "S1 just identified 25 high-intent buyers for Category Y. Current inventory covers 10 orders. Buy more now before the supplier raises prices." → Triggers P3 to negotiate and buy.

3. **Sets guardrails for Deal Closer.** "This buyer wants a 15% discount. Your cost basis is $X. Minimum margin is 20%. You can go to $Y but no lower." → S3 negotiates within real margin boundaries, not static price sheets.

4. **Flags margin compression.** "Your average margin on Category Z dropped from 25% to 14% over the last 60 days. The issue is on the buy side — supplier costs are up 8%. Either renegotiate (→ P3) or raise sell prices (→ S3)."

5. **Optimizes timing.** "Supplier A offers 2% early-pay discount. Buyer B has a net-30 invoice outstanding. If you pay the supplier now and collect from the buyer on time, you net an extra $4K this month." → Coordinates cash flow across both sides.

---

## The Full Map — How They Interact

```
                        ┌──────────────────┐
                        │   MARGIN PILOT   │
                        │   (M1)           │
                        │                  │
                        │ • Cost basis     │
                        │ • Margin floors  │
                        │ • Push signals   │
                        └────────┬─────────┘
                                 │
                 ┌───────────────┼───────────────┐
                 │               │               │
                 ▼               │               ▼
    ┌─── SELL SIDE ───┐         │    ┌─── BUY SIDE ───┐
    │                 │         │    │                 │
    │  S1 Buyer       │◄────────┼───►│  P1 Demand      │
    │     Finder      │         │    │     Reader      │
    │       │         │         │    │       │         │
    │       ▼         │         │    │       ▼         │
    │  S2 Outreach    │         │    │  P2 Stock       │
    │     Rep         │◄────────┼───►│     Watcher     │
    │       │         │         │    │       │         │
    │       ▼         │         │    │       ▼         │
    │  S3 Deal        │◄────────┼───►│  P3 Supplier    │
    │     Closer      │         │    │     Negotiator  │
    │                 │         │    │                 │
    └─────────────────┘         │    └─────────────────┘
                                │
                        ┌───────┴────────┐
                        │     ERP        │
                        │ (Source of     │
                        │  truth)        │
                        └────────────────┘
```

**Key cross-interactions:**
- P2 → S1: "We're overstocked on SKU X, push it" (clearance campaigns)
- S3 → P1: "We have $200K in open quotes for Category Y, stock up" (demand signal)
- P3 → M1 → S3: "Cost went up on SKU Z, raise the floor" (margin protection)
- S1 → P1: "We're targeting 40 new buyers in Category Y next month" (forward demand)
- M1 → S2: "This SKU has 35% margin right now — lead with it in outreach" (profit-first selling)

---

## What This Means for the Landing Page (Section 5)

For the current landing page (wedge = Sales Agent), you only need to show S1 + S2 + S3. But here's how to hint at the bigger picture without over-promising:

**Current section:** "One Agent. Three Jobs Done." with Researcher / Sales Rep / Deal Maker

**Proposed addition — one line at the bottom of the section:**

> "Today, the OPSA Sales Agent handles finding, reaching, and closing buyers. Next: an AI procurement agent that negotiates better supplier pricing — so your margins grow from both sides."

Or even simpler:

> "This is step one. Selling smarter. Step two: buying smarter."

This plants the seed for the procurement product without listing it as a current offering. It also sets up the Margin Pilot story for when you're ready to pitch the full platform.

---

## Summary: The 7 Blocks

| # | Block | Side | One-Liner |
|---|---|---|---|
| S1 | Buyer Finder | Sell | Finds who to sell to |
| S2 | Outreach Rep | Sell | Does the selling |
| S3 | Deal Closer | Sell | Closes at the right price |
| P1 | Demand Reader | Buy | Predicts what you'll need |
| P2 | Stock Watcher | Buy | Knows what's running low (or sitting too long) |
| P3 | Supplier Negotiator | Buy | Gets the best cost from suppliers |
| **M1** | **Margin Pilot** | **Connector** | **Makes sales and procurement talk to each other — optimizes the spread** |

**The Margin Pilot is the missing block.** It's what turns two separate agent systems into a single margin-optimization engine. Without it, you have two smart but independent teams. With it, every sell decision is informed by the buy cost, and every buy decision is informed by the sell demand.
