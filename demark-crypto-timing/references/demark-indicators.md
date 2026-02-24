# DeMark Indicators — Technical Reference

## Table of Contents
1. [TD Sequential](#td-sequential)
2. [TD Combo](#td-combo)
3. [TD Setup Trend (TDST)](#tdst)
4. [Cycle Framework for Crypto](#cycle-framework)
5. [Fundstrat Integration](#fundstrat-integration)
6. [Crypto-Specific Adaptations](#crypto-adaptations)

---

## TD Sequential {#td-sequential}

The primary DeMark indicator. Two phases: **Setup** and **Countdown**.

### Setup Phase (Bars 1–9)

**Buy Setup:**
- Requires 9 consecutive closes LESS THAN the close 4 bars earlier
- Each bar must satisfy: `Close[i] < Close[i-4]`
- Bar 1 must be preceded by a close >= the close 4 bars prior (the "flip")
- Setup completes on bar 9

**Sell Setup:**
- Mirror: 9 consecutive closes GREATER THAN the close 4 bars earlier
- `Close[i] > Close[i-4]`

**Setup Perfection:**
- A buy setup is "perfected" when bar 8 or 9 has a low ≤ the low of bars 6 and 7
- Perfection increases signal reliability
- If not perfected, signal may need additional confirmation

### Countdown Phase (Bars 1–13)

Begins after a completed Setup. Countdown bars do NOT need to be consecutive.

**Buy Countdown:**
- Each qualifying bar: `Close[i] ≤ Low[i-2]`
- Count advances only on bars meeting this condition
- Bar 13 completes the countdown — this is the **primary exhaustion signal**
- Bar 13 qualification: close must be ≤ the close of bar 8 of the countdown

**Sell Countdown:**
- Each qualifying bar: `Close[i] ≥ High[i-2]`
- Bar 13 = exhaustion signal for the uptrend

### The "13" Signal — What It Means

A completed 13-count signals **trend exhaustion**, not necessarily immediate reversal:
- The existing trend has used up its momentum
- A pause, consolidation, or reversal becomes more probable
- In crypto, these signals are most reliable on **daily and weekly** timeframes
- On intraday charts (4H, 1H), false signals are more common due to crypto volatility

### Recycling / Cancellation

- A new Setup in the SAME direction can "recycle" the countdown (reset to 0)
- A Setup in the OPPOSITE direction can cancel an active countdown
- TDST level break (see below) can also invalidate

---

## TD Combo {#td-combo}

A stricter exhaustion indicator that runs parallel to Sequential.

### Key Differences from Sequential

| Feature | Sequential | Combo |
|---------|-----------|-------|
| Countdown condition | Close vs Low/High 2 bars back | Close vs close 1 bar back (+ additional filters) |
| Strictness | Moderate | Higher — fewer false signals |
| Speed | Typically completes faster | Typically slower |
| Crypto reliability | Good on daily/weekly | Better confirmation when both align |

### Buy Combo Countdown
- Close ≤ the low 2 bars earlier AND close < close of prior bar
- More restrictive = fewer signals but higher quality

### When Both Align

**Sequential 13 + Combo 13 at the same zone = highest conviction DeMark signal.** This confluence is rare but historically powerful in crypto. When it occurs at a known support/resistance level AND aligns with cycle timing, treat as Tier 1.

---

## TD Setup Trend (TDST) {#tdst}

The TDST levels are support and resistance lines derived from the Setup phase.

### Calculation
- **TDST Support** (from Buy Setup): The highest HIGH within the Buy Setup (bars 1–9)
- **TDST Resistance** (from Sell Setup): The lowest LOW within the Sell Setup (bars 1–9)

### Application in Crypto
- TDST levels act as key S/R that can validate or invalidate signals
- **If price breaks TDST support after a buy signal → signal is invalidated** — this is the stop-loss logic
- TDST levels from weekly setups carry more weight than daily
- In BTC: TDST breaks often coincide with capitulation events

---

## Cycle Framework for Crypto {#cycle-framework}

### The 90-Day (Quarterly) BTC Cycle

Empirical observation (not DeMark-original, but widely paired with DeMark signals):

- BTC tends to form intermediate lows on roughly 80–100 day intervals
- These aren't precise clocks — they're probabilistic windows (±2 weeks)
- When a DeMark exhaustion signal occurs within a cycle low window, conviction increases significantly

### Halving Cycle Overlay

- BTC halving occurs every ~210,000 blocks (~4 years)
- Historical pattern: major bull runs initiate 6–18 months post-halving
- DeMark signals during post-halving accumulation phases have historically been high-quality entry points
- The halving cycle provides the macro directional bias; DeMark provides the micro-timing

### Cycle Mapping Process

1. Identify last confirmed 90-day cycle low (search recent analysis)
2. Project next window: prior low + 80–100 days
3. Check for active DeMark Setup or Countdown on daily/weekly
4. Assess TDST levels relative to current price
5. Overlay macro context (Fed, ETF flows, on-chain)
6. Assign conviction tier (1/2/3)

---

## Fundstrat Integration {#fundstrat-integration}

### How Fundstrat Uses DeMark

Tom Lee's Fundstrat team integrates DeMark signals into their crypto research:

- **Counter-trend framework**: They use Sequential/Combo to identify when strong trends may reverse
- **Not contrarian for contrarian's sake**: DeMark signals are used to TIME entries within a pre-existing macro bullish thesis
- **Cycle alignment**: Fundstrat pairs DeMark mechanical signals with their own cycle work and on-chain analysis

### Tom Lee's Typical Framing

- Establishes long-term BTC/ETH target ranges based on fundamental and flow analysis
- Uses DeMark signals to identify tactical entry windows within that bullish framework
- Emphasizes that DeMark signals mark "windows of opportunity" not "sell everything" or "buy everything" moments
- Often references "13" signals in public commentary when they occur on weekly charts

### How to Reference Fundstrat in Analysis

- Always search for recent Fundstrat/Tom Lee commentary before citing specific targets
- Historical target ranges are directional context, not investment advice
- When Fundstrat targets are cited, note the date of the call — targets evolve

---

## Crypto-Specific Adaptations {#crypto-adaptations}

### Volatility Adjustments

Crypto's higher volatility vs. equities means:
- **Setup phases complete faster** — 9-bar setups on daily BTC happen more frequently than in SPX
- **False signals are more common on lower timeframes** — daily minimum, weekly preferred
- **TDST levels need wider buffers** — a wick through TDST that closes back above isn't a true break in crypto
- **Weekend trading** — unlike equities, crypto trades 24/7; weekly candle closes matter (Sunday UTC)

### BTC vs ETH Signal Behavior

- **BTC**: More institutional flow → DeMark signals tend to be more reliable, especially on weekly
- **ETH**: Higher beta, more retail-driven → signals are noisier; use BTC signals as lead indicator
- **ETH/BTC ratio**: DeMark signals on the ratio chart can flag rotation opportunities

### Recommended Timeframe Hierarchy

1. **Weekly chart**: Primary signal source — "13" here is highest conviction
2. **Daily chart**: Secondary — good for timing entries within weekly setup context
3. **4-Hour**: Only for fine-tuning entry price within an already-confirmed daily/weekly signal
4. **Monthly**: Secular trend context only — too slow for entry timing

### Position Sizing Framework

For satellite crypto allocation within a broader portfolio:

```
Total Crypto Allocation Target: X% of investable assets

Tiered Entry Structure:
├── Tier 1 (40% of allocation): Deploy on Sequential 13 + Combo + Cycle confluence
├── Tier 2 (30%): Deploy on Sequential 13 + one confirming factor
├── Tier 3 (15%): Deploy on Setup 9 near support with positive macro
└── Reserve (15%): Opportunistic / black swan deployment

Risk Management:
├── Per-entry stop: TDST support break on the timeframe of the signal
├── Portfolio stop: If total crypto drawdown exceeds [user-defined]% of allocation, pause
└── Rebalance trigger: If crypto grows to >1.5x target allocation, trim to target
```
