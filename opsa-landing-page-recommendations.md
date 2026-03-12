# OPSA Landing Page — Build Spec

**Reference site (current production):** https://opsa-website-7biri2eja-opsa-934bd8f0.vercel.app/

**Goal:** Rebuild the landing page with updated copy, restructured sections, and new layout patterns. Keep the existing visual identity (dark/light theme alternation, purple accent color, serif headline + sans-serif body typography, card-based layouts) unless noted otherwise.

**Vision tagline:** OPSA helps you build the future sales team with AI agents that find buyers, send the right offer, follow up, and close.

**Language principle:** Keep "AI" front and center — it's a selling point. Remove investor jargon ("autonomous agents," "intelligence layer," "agentic commerce"). Use wholesaler vocabulary: reps, quoting, follow-ups, orders, buyers, margins. "Physical economy" stays in the label only.

---

## Page Structure (top to bottom)

| # | Section | Background | Anchor ID |
|---|---|---|---|
| 1 | Nav Bar | Sticky, transparent over hero → solid on scroll | — |
| 2 | Hero | Dark (full-viewport, background image — keep current handshake photo or similar) | `#hero` |
| 3 | Why Now / Problem | Light (white/off-white) | `#why-now` |
| 4 | OPSA Intelligence | Dark (dark navy/charcoal, matches current dark sections) | `#intelligence` |
| 5 | Sales Agent Deep-Dive | Dark (continuation or slightly different shade) | `#sales-agent` |
| 6 | How It Works (Timeline) | Light (white/off-white) | `#how-it-works` |
| 7 | Testimonials / Results | Dark | `#results` |
| 8 | Final CTA | Dark banner (inline, not full section) | `#cta` |
| 9 | Footer | Dark | — |

---

## 1. NAV BAR

**Reference:** Keep current sticky nav behavior from the reference site. Logo left, links center, CTA right.

**Content:**

| Element | Value |
|---|---|
| Logo | "OPSA" (keep current purple serif logo) |
| Link 1 | "OPSA Intelligence" → scrolls to `#intelligence` |
| Link 2 | "Sales Agent" → scrolls to `#sales-agent` |
| Link 3 | "How It Works" → scrolls to `#how-it-works` |
| Link 4 | "Results" → scrolls to `#results` |
| CTA button | "Get in Touch" (keep current red/coral pill button style) |

---

## 2. HERO

**Reference:** Same full-viewport dark hero as current site — background image with overlay, text left-aligned. Keep the "SCROLL" indicator at the bottom.

**Layout:** Full viewport height. Text block left-aligned, vertically centered, max-width ~700px.

**Content:**

| Element | Value | Style Notes |
|---|---|---|
| Headline | "AI Teams for the Physical Economy" | Large serif font (keep current headline style). "the Physical Economy" in purple accent color. No label above — headline IS the positioning statement. |
| Sub-copy | "OPSA helps you generate revenue through an AI team that finds, reaches, and closes buyers — working alongside your team without any changes to your workflow." | Body sans-serif, muted white/light gray, max-width ~600px |
| Trust line | "Trusted by wholesale distributors across the US" | Small, muted text below sub-copy (keep current treatment) |
| Scroll indicator | "SCROLL" + down chevron | Bottom center, keep current |

---

## 3. WHY NOW / PROBLEM SECTION

**Reference:** Same layout pattern as current "Why Now" section — intro text block, then 4 cards in a horizontal row. Keep light background (white/off-white) with dark text.

**Layout:**
- Section label + headline + intro paragraph (centered or left-aligned)
- 4 pain-point cards in a 4-column grid (on desktop), stacking to 2x2 or single column on mobile
- Each card has: icon (keep current icon style — small purple icon in light circle), title (bold), description (body text)

**Content:**

| Element | Value |
|---|---|
| Label | "WHY NOW" (small caps, purple) |
| Headline | "AI can now think like your best rep — and act like one too." |
| Intro paragraph | "You invested in ERP, CRM, even e-commerce — and they made your team more efficient. But none of them generate revenue. OPSA does." |

**Pain Cards (4 cards, left to right):**

| Card | Icon | Title | Description |
|---|---|---|---|
| 1 | Inbox/email icon | **Reps Buried in Admin, Not Selling** | Quoting, re-keying orders, chasing approvals — your salespeople spend more time on paperwork than in front of buyers. |
| 2 | Clock/timer icon | **Quotes Take Days. Deals Don't Wait.** | By the time a quote gets built, approved, and sent, the buyer's already called your competitor. |
| 3 | Falling/gap icon | **Follow-Ups Fall Through the Cracks** | Trade show leads go cold. Dormant accounts stay dormant. Your best cross-sell opportunities die in someone's inbox. |
| 4 | Dollar/leak icon | **Pricing Is a Mess. Margins Leak.** | Customer-specific pricing scattered across spreadsheets, emails, and people's heads. Every inconsistent quote is money left on the table. |

**Note:** The headline itself ("AI can now think like your best rep — and act like one too.") serves as both the section opener and the "why now" answer — no separate bridge line needed.

---

## 4. OPSA INTELLIGENCE — THE CENTER HUB

**Reference:** Similar layout to the current "Intelligence Layer" section (dark background, diagram in center). But replace the current 3-column input → brain → output diagram with a cleaner hub-and-spoke layout, plus insight cards below.

**Layout — two parts:**

### Part A: Headline + Diagram (upper half)

- Section label + headline + sub-copy (centered)
- Below: an animated or static diagram showing 3 data sources feeding into a center hub labeled "OPSA Intelligence," with a single output arrow to "Your AI Teams"

| Element | Value |
|---|---|
| Label | "THE BRAIN BEHIND YOUR AI TEAMS" (small caps, purple) |
| Headline | "OPSA Intelligence: Your Business Data, Powering Your AI Teams" |
| Sub-copy | "Your ERP, your reps' knowledge, your buyer history — OPSA Intelligence absorbs it all and powers your AI teams. The right offer, to the right buyer, at the right price. Every time." |

**Diagram spec:**

```
[Your ERP]
 Orders, inventory,    ──┐
 pricing rules           │
                         ▼
[Your Reps]          ──► OPSA Intelligence ──► Your AI Teams
 Deals, buyer            ▲             (that find, reach,
 preferences             │              and close buyers)
                         │
[Your Buyers]         ──┘
 Order history,
 reorder timing
```

- Use the current site's card styling for the 3 input sources (dark cards with icon + label + description, similar to current "What Goes In" cards)
- Center hub: prominent, glowing or highlighted element labeled "OPSA Intelligence"
- Single output: one arrow/flow to "Your AI Teams" (NOT 3 separate agent outputs)
- Consider subtle animation: data flowing from inputs → hub → output

**Footer line (below diagram):**
"Your ERP holds the data. Your reps hold the relationships. OPSA Intelligence combines both — so your AI teams make informed decisions, not guesses."

---

## 5. SALES AGENT DEEP-DIVE

**Reference:** Same layout as current "Sales Agent" section — headline + sub, then 3 cards (Researcher / Sales Rep / Deal Maker). Keep dark background, 3-column card grid.

**Layout:**
- Section label + headline + sub-copy
- 3 agent role cards in a row (dark cards with icon + role title + description)
- Connector line below the cards
- Teaser line at bottom of section

**Content:**

| Element | Value |
|---|---|
| Label | "SALES AGENT" (small caps, purple) |
| Headline | "Three AI Agents. One Sales Team." |
| Sub-copy | "OPSA's Sales Agent handles every step of the sale — research, outreach, and closing — without adding a single headcount." |

**Agent Cards (3 cards, left to right):**

| Card | Icon | Title | Description |
|---|---|---|---|
| 1 | Search/magnifying glass icon | **AI Researcher** | Finds buyers who are ready to order — based on what they've bought before, when they reorder, and what's trending in your market. |
| 2 | Chat/message icon | **AI Sales Rep** | Reaches out to buyers over email and messaging with personalized offers. Answers questions, handles follow-ups, and keeps in touch — automatically. |
| 3 | Handshake/deal icon | **AI Deal Maker** | Negotiates pricing within your rules, sends quotes, handles pushback, and closes the order. Your team gets notified when the deal is done. |

**Connector line (below cards, centered):**
"Every agent is powered by OPSA Intelligence — your inventory, your pricing rules, your buyer history — so every decision is informed, not generic."

Style: Smaller text, muted color, acts as a bridge between this section and Section 4 above.

**Teaser line (bottom of section, centered, slightly emphasized):**
"This is step one. Selling smarter. Step two: buying smarter. Stay tuned."

Style: Italic or slightly different weight to signal it's a forward-looking statement. Subtle — not a CTA, just a seed.

---

## 6. HOW IT WORKS (Implementation Timeline)

**Reference:** NOT the current 5-step horizontal stepper. Replace with a scroll-triggered vertical or horizontal timeline (reference design: progressive Day/Week milestones with checkboxes that advance as user scrolls). Light background section.

**Layout:**
- Section label + headline at top
- Horizontal timeline bar with 3 milestone dots (Week 1 / Week 2 / Week 3)
- Below the timeline: 3 columns (one per week), each with a milestone title and checkbox items
- Scroll-triggered animation: as user scrolls, the timeline progresses from Week 1 → 2 → 3, and checkboxes fill in. Milestone content fades/slides in as it becomes active.
- On mobile: stack vertically, each week as a separate block

**Content:**

| Element | Value |
|---|---|
| Label | "IMPLEMENTATION" (small caps, red/coral accent — matching CTA color for urgency) |
| Headline | "Live in Weeks, Not Months" |
| Sub-copy | "No new software to learn. No workflow to change. OPSA plugs into your existing systems and works where your team already does — email, ERP, and WhatsApp." |

**Why this sub-copy matters:** This is where you preempt the #1 objection from any wholesaler who's been burned by a CRM rollout. Unlike Salesforce or HubSpot that require reps to log into a new dashboard and change how they work, OPSA works in the background. Your reps keep doing what they do — OPSA just does more of it, automatically.

**Timeline milestones:**

| Milestone | Title | Checkbox Items |
|---|---|---|
| **WEEK 1** | **Connect Your Systems** | ☑ Connect your ERP and inventory feeds · ☑ Upload your buyer lists and contact database · ☑ Share your pricing rules and margin targets |
| **WEEK 2** | **OPSA Learns Your Business** | ☑ AI profiles every buyer — order history, preferences, pricing · ☑ Learns your product catalog and what's in stock · ☑ Studies your reps' past deals and what's worked |
| **WEEK 3** | **Start Closing Deals** | ☑ AI reaches out to the right buyers with personalized offers · ☑ Handles replies, follows up, negotiates pricing · ☑ Orders flow directly into your ERP — your team gets notified |

**Visual treatment:**
- Week 1 and 2 checkboxes: filled/dark (completed state)
- Week 3 checkboxes: lighter/grayed (future state) — until user scrolls to it, then they fill in
- Timeline bar: solid line connecting the three dots, with progress fill animation on scroll
- Each week's title should be prominent (20-24pt bold)

---

## 7. TESTIMONIALS / RESULTS

**Reference:** Keep current layout from the reference site — 3 metric cards on top, 3 testimonial quote cards below. Dark background.

**Layout:**
- Section label + headline
- 3 metric cards (top row): large number, label, sub-label
- 3 quote cards (bottom row): quote text, attribution

**Content:**

| Element | Value |
|---|---|
| Label | "RESULTS" (small caps, purple) |
| Headline | "Proof, Not Promises" |

**Metric Cards (3 cards, top row):**

| Card | Number | Label | Sub-label |
|---|---|---|---|
| 1 | **$125K+** | New revenue per month | Per partner, 90-day average |
| 2 | **60%** | Quiet accounts started ordering again | Within 3 months |
| 3 | **40+** | Orders closed | First customer, first 90 days |

**Quote Cards (3 cards, bottom row):**

| Card | Quote | Attribution |
|---|---|---|
| 1 | "We're closing deals on accounts we hadn't touched in months. OPSA found revenue we didn't know existed." | — Sales Manager, National Distributor |
| 2 | "The orders just started appearing in our ERP. My team didn't have to do anything different." | — VP Operations, Wholesale Company |
| 3 | "We scaled revenue without a single new hire. The ROI was obvious within the first month." | — CEO, Distribution Company |

**Note:** Consider adding more specificity to attributions when possible (e.g., company size, vertical, location) to build credibility.

---

## 8. FINAL CTA

**Reference:** Keep current inline CTA banner style — dark background strip with headline left, button right. Sits between testimonials and footer.

**Layout:** Full-width banner, single row. Headline + sub on the left, CTA button on the right.

**Content:**

| Element | Value |
|---|---|
| Headline | "Ready to Sell More Without Hiring More?" |
| Sub-copy | "See how OPSA's AI sales agent can drive new revenue for your business." |
| CTA button | "Schedule a Demo →" (keep current red/coral pill button style) |

---

## 9. FOOTER

**Reference:** Keep current minimal footer from reference site.

**Content:**

| Element | Value |
|---|---|
| Left | "Opsa Inc." |
| Right | tech@opsa.ai · Privacy Policy · Terms of Service |

---

## Quick Reference: Key Language Shifts

Use this table when writing any copy for the page. If you see the left column in the codebase, replace with the right column.

| Investor / Tech Language (remove) | Wholesaler Language (use instead) |
|---|---|
| Physical economy (in body copy) | Wholesale / distribution (keep in hero label only) |
| Agentic commerce | AI sales agent |
| Autonomous agents | AI that works alongside your reps |
| Intelligence layer | OPSA Intelligence / how OPSA learns your business |
| LLMs / APIs | AI that reads and responds |
| Enrich leads / enrichment | Build buyer profiles |
| Deploy agents | Set up OPSA / put OPSA to work |
| Tribal knowledge | What your reps know |
| Holistic view | Complete buyer profile |
| High-intent buyers | Buyers who are ready to order |
| Market signals | Buying patterns / order trends |
| Nurtures relationships | Keeps in touch / follows up |
| Revenue engine | Sales machine |
| Personalized at scale | The right offer to every buyer |

**Note:** "AI" itself is kept everywhere — it's a differentiator. Pair "AI" with familiar wholesaler actions (AI + quoting, AI + follow-ups, AI + buyer profiles), not tech abstractions (AI + intelligence layer, AI + autonomous agents, AI + agentic commerce). "Physical economy" is kept in the hero label ("AI TEAMS FOR THE PHYSICAL ECONOMY") because the headline earns it through contrast — avoid elsewhere in body copy.

---

## Sections Removed from Current Site

The following sections from the current production site (https://opsa-website-7biri2eja-opsa-934bd8f0.vercel.app/) should NOT be carried over to the new build:

| Removed Section | Reason |
|---|---|
| "Operations & Data Entry Agent" product card | Not part of the wedge — Sales Agent only for now |
| "Procurement Agent" product card | Not part of the wedge — teased via "Step two: buying smarter" line instead |
| 3-agent output in Intelligence diagram (Sales / Procurement / Operations) | Replaced with single "AI Sales Agents" output to match wedge focus |
| "Not Just AI Teammates. Autonomous Sales Agents for the Physical Economy." differentiator section | Removed — redundant with Sales Agent deep-dive. Messaging absorbed into other sections |
| 5-step horizontal "How It Works" stepper | Replaced with Week 1/2/3 scroll-triggered timeline layout |

---

## Supporting Documents

| Document | Purpose |
|---|---|
| `opsa-agent-building-blocks.md` | Full agent architecture: 7 building blocks (3 sell-side, 3 buy-side, 1 Margin Pilot connector). For internal strategy reference, not customer-facing. |
