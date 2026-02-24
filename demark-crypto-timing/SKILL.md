---
name: demark-crypto-timing
description: >
  DeMark-style technical analysis and cycle timing for Bitcoin, Ethereum, and crypto assets.
  Use this skill whenever the user asks about crypto entry/exit timing, TD Sequential signals,
  DeMark indicators, BTC/ETH cycle analysis, counter-trend exhaustion signals, buy/sell zone
  identification, or building entry-rule sheets for crypto positions. Also trigger when the user
  mentions Tom DeMark, Fundstrat, Tom Lee crypto timing, "13" signals, setup/countdown cycles,
  90-day cycle flips, or wants to map technical conditions to dollar-cost-averaging or stepped
  entry strategies. Trigger even for casual questions like "is now a good time to buy BTC" or
  "where are we in the crypto cycle" — the DeMark framework applies.
---

# DeMark Crypto Timing Skill

## Purpose

Provide DeMark-indicator-informed analysis for Bitcoin and Ethereum timing decisions, combining:
1. **DeMark mechanical signals** (TD Sequential, TD Combo, TD Setup, TD Countdown)
2. **Cycle analysis** (90-day flips, halving cycles, macro liquidity windows)
3. **Fundstrat/Tom Lee macro framing** (long-term target ranges as directional bias)
4. **Actionable entry-rule sheets** that pair signal conditions with position-sizing math

## Who This Is For

The user is a sophisticated investor with a pre-IPO portfolio who treats crypto as a satellite allocation. She is NOT a day-trader. Frame all output for **swing-to-strategic timeframes** (daily/weekly charts, not 4H scalps) unless she explicitly requests shorter timeframes. She understands IRR, cost-basis math, and risk-adjusted returns — skip basics.

---

## Core Framework: Two-Layer Analysis

Every crypto timing response should operate on two layers:

### Layer 1: Macro Directional Bias (Fundstrat / Tom Lee Style)

Before any DeMark signal discussion, establish the macro context:

- **BTC secular trend**: Where are we relative to halving cycle? Post-halving years historically front-load gains.
- **Long-term target bands**: Lee's framework typically anchors BTC at $100K–$200K+ in bull cycles, ETH at $7K–$12K. These are directional, not precision targets.
- **Macro catalysts**: ETF flows, Fed policy regime, institutional adoption curve, on-chain metrics (MVRV, SOPR, exchange reserves).
- **Risk regime**: Is the macro backdrop risk-on or risk-off? This determines whether DeMark buy signals are high-conviction or fade-worthy.

> Always web-search for current BTC/ETH price, recent macro developments, and any recent DeMark-related commentary from Fundstrat before responding.

### Layer 2: DeMark Micro-Timing (Signal-Based Entry Windows)

Once macro bias is established, apply DeMark mechanics to identify entry/exit windows.

---

## DeMark Indicator Reference

For detailed indicator mechanics, read: `references/demark-indicators.md`

### Quick Reference — The Signals That Matter Most for Crypto

| Signal | What It Flags | Timeframe That Matters | Crypto Application |
|--------|--------------|----------------------|-------------------|
| TD Sequential "9" (Setup) | Trend pause / potential inflection | Daily, Weekly | Early warning — trend may be tiring |
| TD Sequential "13" (Countdown) | Trend exhaustion — higher-probability reversal | Daily, Weekly | **Primary entry/exit signal** for swing positions |
| TD Combo "13" | Exhaustion with stricter conditions | Daily, Weekly | Confirmation layer — stronger when aligns with Sequential |
| TD Setup Trend (TDST) | Support/resistance levels from setup range | All | Key price levels — if broken, signal is invalidated |
| 90-Day Cycle Flip | ~Quarterly rhythm in BTC price action | Calendar | Aligns DeMark signals with cyclical tendency |

### Signal Confluence = Higher Conviction

A single "13" on a daily chart is informational. **Confluence** is what makes it actionable:

- **Tier 1 (Highest conviction)**: Sequential "13" + Combo "13" + 90-day cycle low + price at known support zone + macro risk-on
- **Tier 2 (Strong)**: Sequential "13" + price at support + one confirming factor (cycle timing OR macro)
- **Tier 3 (Monitor only)**: Isolated "13" without supporting context — note it, don't act on it alone

---

## Response Templates

### When Asked "Should I Buy BTC/ETH Now?"

Structure the response as:

1. **Current Price & Macro Context** (search first — never use stale data)
2. **Where Are We in the Cycle?** (halving cycle position, macro liquidity regime)
3. **Active DeMark Signals** (search for any recent Fundstrat/DeMark commentary on BTC/ETH)
4. **Signal Confluence Assessment** (Tier 1/2/3 per above)
5. **Recommended Posture**: One of:
   - **Aggressive entry zone** (Tier 1 confluence)
   - **Scaled entry** (Tier 2 — step in with partial position)
   - **Wait for signal** (no active confluence — define what to watch for)
   - **Reduce/hedge** (exhaustion signal on existing longs)

### When Asked to Build an Entry-Rule Sheet

Create a structured decision matrix:

```
ENTRY RULE SHEET — [Asset] — [Timeframe]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

MACRO BIAS: [Bullish / Neutral / Bearish]
Target Range: $[X] – $[Y] (Fundstrat framework)
Current Price: $[Z] (as of [date])

ENTRY ZONES (ordered by conviction):
┌──────────────┬───────────────────────────────┬────────────┬──────────┐
│ Zone         │ Conditions Required           │ Price Band │ Size     │
├──────────────┼───────────────────────────────┼────────────┼──────────┤
│ Tier 1       │ Seq 13 + Combo 13 + Cycle Low │ $XX–$XX    │ 40% pos  │
│ Tier 2       │ Seq 13 + Support Hold         │ $XX–$XX    │ 30% pos  │
│ Tier 3       │ Seq 9 + Approaching Support   │ $XX–$XX    │ 15% pos  │
│ Opportunistic│ Flash crash / black swan      │ Below $XX  │ 15% pos  │
└──────────────┴───────────────────────────────┴────────────┴──────────┘

INVALIDATION:
- TDST support break below $[X] → pause entries, reassess
- Macro regime shift to risk-off → reduce target allocation by 50%

COST BASIS MATH:
- If all tiers fill: Blended entry = $[weighted avg]
- Monthly DCA overlay: $[amount]/mo adds $[X] exposure over [N] months
- Effective cost per coin at full allocation: $[X]
```

### When Asked About Cycle Timing

Reference the 90-day cycle framework:
- Identify last confirmed cycle low (search for it)
- Project approximate next cycle window (+/- 2 weeks)
- Overlay with any active DeMark signals on weekly chart
- Note: Cycles stretch and compress — they're probabilistic zones, not clocks

---

## Critical Guardrails

1. **Always search before responding** — crypto moves fast. Never rely on training data for prices, signals, or market conditions.
2. **DeMark signals are probabilistic, not deterministic** — always frame as "higher-probability window" not "guaranteed reversal."
3. **Position sizing > entry price** — emphasize that the tiered entry structure matters more than catching the exact bottom.
4. **This is satellite allocation** — the user's core wealth is in RE and pre-IPO. Crypto sizing should reflect that context.
5. **No "financial advisor" disclaimers** — the user is a licensed broker and sophisticated investor. Treat as peer.
6. **Show your work** — when calculating cost basis, blended entries, or DCA math, show the arithmetic.

---

## Search Strategy

When this skill triggers, always run these searches before responding:

1. `BTC price today` or `ETH price today`
2. `DeMark Sequential Bitcoin [current month/year]` or `Fundstrat BTC signal`
3. `Bitcoin 90 day cycle [current year]` or `BTC cycle analysis`
4. Any additional context-specific searches based on the user's question

If Fundstrat/DeMark-specific commentary isn't found, synthesize from available technical analysis sources that reference Sequential/exhaustion signals.
