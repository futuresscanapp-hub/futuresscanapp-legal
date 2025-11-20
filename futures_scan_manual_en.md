# Futures Scan – User Manual (EN)

**Document version:** 1.0  
**App:** Futures Scan (Android)

---

## 1. Introduction

Futures Scan is an application for **technical analysis and signal generation** on the cryptocurrency futures market.  
The app:

- scans selected pairs and timeframes,
- uses **multiple filters** (Trend, Momentum, Bollinger Bands, RSI, Donchian, MACD, Z-Score, ATR, Volume, EMA200),
- calculates **targets TP1 / TP2 / TP3 and SL**,
- supports **retest logic**, post-SL signal blocking and **background work**.

> ⚠️ **DISCLAIMER – no investment advice**  
> Futures Scan is NOT an investment advisory tool.  
> You make all trading decisions on your own and at your own risk.  
> Leveraged trading (futures) involves a risk of losing all your capital.

---

## 2. Requirements and installation

### 2.1. Requirements

- Android phone / tablet (recommended Android 8+).
- Stable Internet connection (Wi-Fi or LTE/5G).
- Exchange account (e.g. Bybit / other) if you want to trade live – **the app does not place orders for you**.

### 2.2. Installation

1. Install the app from **Google Play**.
2. On first launch:
   - accept the terms / disclaimer,
   - grant necessary permissions (notifications, background work – if you want to use it).

---

## 3. Trial and subscriptions

### 3.1. Trial period

After installation the app starts a **trial period**.  
During the trial you effectively have access to full functionality (similar to **ELITE** tier).

On the screen **App settings → Subscription** you can see:

- whether the trial is active,
- how many days are left.

After the trial expires:

- if you **do not purchase a subscription**, the app switches to a limited mode (**NONE** tier),
- you can activate a paid tier at any time.

### 3.2. Subscription tiers

The app supports 3 paid tiers:

- **BASIC**
- **PRO**
- **ELITE**

Each can have periods:
- **1 week**,
- **1 month**.

Exact prices and available periods are shown on the **subscription screen** – they are fetched directly from Google Play.

#### 3.2.1. Tier NONE (after trial, no subscription)

- No background work.
- Targets: only **Fixed** (constant percentages).
- Limit **1 pair**.
- Limit **1 TF per filter**.
- No detailed signal view (limited access).

#### 3.2.2. Tier BASIC

- Allowed background mode: **REST**.
- Targets: **Fixed**.
- Limit: **2 pairs**.
- Limit: **2 TF per filter**.
- No detailed signal view.

#### 3.2.3. Tier PRO

- Allowed background modes: **REST + SMART**.
- Targets: **Fixed + Levels R/S (local support/resistance)**.
- More pairs (e.g. up to 5).
- No TF-per-filter limit.
- Detailed signal view enabled.

#### 3.2.4. Tier ELITE

- All background modes: **REST / LIVE / SMART**.
- All target modes (Fixed, **Levels R/S**, etc.).
- **No TF-per-filter limit.**
- **No pair limit.**
- Full signal details.

---

## 4. “App settings” screen

Entry: **Menu → App settings**.

### 4.1. Background work – Foreground Service

**Switch:** “Background work / scanning in background”

- When enabled the app starts a **Foreground Service** (icon in status bar).
- The signal engine runs regardless of screen state or whether the app is in the foreground.

Requirements:

- Active **trial** or BASIC/PRO/ELITE tier,
- Notifications enabled for the app.

If conditions are not met the app informs you that background work is available only during trial or with a subscription.

### 4.2. Background mode (REST / LIVE / SMART)

In the “Engine mode” section you can choose:

- **REST** – polling data via HTTP in intervals,
- **LIVE** – (if available) more real-time mode using streams (e.g. WebSocket),
- **SMART** – hybrid / intelligent mode (chooses data source depending on network and load).

> Available modes depend on your tier (BASIC – REST only, PRO – REST+SMART, ELITE – all).

### 4.3. Notifications

“Notifications” switch:

- Enables/disables notifications about new signals.
- On Android 13+ a separate “Show notifications” permission is required – the app asks for it when you first start background work.

### 4.4. Battery optimization

“Battery optimization” card:

- Helps you configure the system correctly so it does not kill the background service.
- Recommended:
  - Disable battery optimization for Futures Scan,
  - Allow background work in system settings (especially on aggressive vendor ROMs).

### 4.5. Trial / Subscription section

You will see:

- trial info (active / expired, days left),
- buttons:
  - **“Manage subscription”** – opens the subscription screen,
  - **“Buy / extend”** – also opens the subscription screen.

---

## 5. “Subscription” screen

The screen shows **three tiers**: BASIC, PRO, ELITE.

For each tier:

- a short description (what it unlocks),
- buttons:
  - **1 week – [price from Google Play]**,
  - **1 month – [price from Google Play]**.

After pressing:

- the standard Google Play purchase dialog opens,
- after a successful purchase/renewal the app automatically updates your tier.

---

## 6. “Signal settings” screen

Entry: **Menu → Signal settings**.

The screen is divided into two tabs:

- **BASIC** – main settings,
- **ADVANCED** – TF-per-filter configuration.

### 6.1. BASIC tab

#### 6.1.1. Signal sensitivity

**Slider:** 30–90%

- Defines how “strict” the signal logic is.
- Lower sensitivity (30–40%):
  - fewer filters must agree,
  - more signals but looser quality.
- Higher sensitivity (70–90%):
  - more filters must point in the same direction,
  - fewer but more selective signals.

#### 6.1.2. Trading style

Options:

- **Scalping**
- **Day trading**
- **Swing trading**
- **Position trading**

Style impacts **default filter TFs**, targets, retest, etc.  
You can change it and the app will adjust baseline settings.

#### 6.1.3. Presets

Presets let you:

- save your current configuration as a **preset** (“Save”),
- pick a preset from the list and **apply** it,
- **delete** a preset.

Example use:

- “Aggressive BTC/ETH scalp”
- “Conservative altcoin swing”

Presets cover: sensitivity, filters, targets, retest, TFs, etc.

---

### 6.2. Targets (TP/SL)

Two modes:

1. **Fixed (percent-based)**  
2. **Levels R/S (local support/resistance)** – in PRO/ELITE tiers.

#### 6.2.1. Fixed

You set:

- **TP1, TP2, TP3** (percentage move),
- **SL** (percentage).

Example:

- TP1: `0.6 %`
- TP2: `1.2 %`
- TP3: `1.8 %`
- SL: `0.8 %`

For scalp you can use lower values, for swing – higher.

##### TP1 final (Scalping)

Option: **“TP1 final (scalp)”**

- When enabled:
  - once TP1 is hit the position is treated as **fully closed** (for stats),
  - the app logs the trade as exited at TP1 (no further targets).

Useful for ultra-fast scalps.

#### 6.2.2. Levels R/S (local support/resistance)

In this mode targets and SL can be aligned to **local support/resistance levels**.

Parameters:

1. **TF for R/S levels**
   - You choose the timeframe used for level detection (e.g. M15 / H1).
   - `Default (from style)` – TF is chosen automatically from current style (Scalp/Day/Swing).

2. **Lookback (number of candles)**
   - Data window for swing high/low detection.
   - Larger lookback:
     - more significant levels,
     - but farther from the current price.

3. **Number of levels (1–3)**
   - How many strongest levels should be used as potential targets.

4. **Pivot mode (RsPivotMode)**

   - **Time-based (Time recent)** – prefers **most recent** pivots;
   - **Price-based (Price nearest)** – prefers levels **closest to current price**.

   This lets you:
   - focus on fresh market reactions (time),
   - or on price-perfect levels (price).

> **Note:** R/S logic is advanced but the market can be very volatile – do not treat it as a guaranteed reversal predictor. It is a tool, not an oracle.

---

### 6.3. Filters (on/off)

You can enable/disable each filter separately.

The more active filters, the stricter the signal logic.

Main filters:

#### 6.3.1. Trend

- Checks overall market direction (e.g. using moving averages).
- Goal: filter out signals **against the trend**.
- Example:
  - Uptrend → prefer long signals,
  - Downtrend → prefer short signals.

#### 6.3.2. Momentum

- Measures **strength and speed of movement** (e.g. ROC).
- Can block signals during “flat” phases.
- Very useful for scalping – avoid dead markets.

#### 6.3.3. Bollinger Bands (BB)

- Uses **Bollinger Bands** to assess price location:
  - band breakouts,
  - behavior near deviations.
- Can be used for:
  - breakout trading,
  - or mean reversion (depending on filter combo).

#### 6.3.4. RSI

- Classic **Relative Strength Index**.
- Helps to filter:
  - extreme overbought/oversold,
  - lack of momentum.

#### 6.3.5. Donchian Channel

- Channel built from **highest highs/lowest lows over a window**.
- Useful for breakout detection.

#### 6.3.6. Slope

- Measures “slope” of price/trend.
- In practice: checks if the move is strong and decisive enough.

#### 6.3.7. MACD

- **Moving Average Convergence Divergence**.
- Used to:
  - confirm direction,
  - avoid trades against strong MACD signals.

#### 6.3.8. Z-Score

- Statistical deviation from the mean.
- Helps detect **overextended** price levels.

#### 6.3.9. ATR Regime

- Uses **Average True Range**:
  - if volatility is too low – can block signals (no point scalping),
  - if too high – you might choose to avoid extremely wild markets.

#### 6.3.10. Volume Pressure

- Analyzes **volume**:
  - is the move backed by real trading,
  - or is it just a random “air” spike.
- Can reject signals without volume confirmation.

#### 6.3.11. EMA200 Distance

- Checks distance from **EMA200** (often seen as “major trend” line).
- Helps avoid entries extremely far from EMA200 (blindly catching tops/bottoms).

---

### 6.4. Retest

**Retest logic** enforces that after a breakout the price:

- returns into a defined **band**,
- or touches a **channel**,
- and only then a signal is emitted.

This helps reduce false breakouts.

Parameters:

1. **Retest mode**
   - **ENTRY BAND** – classic entry retest:
     - price breaks out then returns into a band around the level,
     - you define band width in % (e.g. 0.2–0.5%).
   - **CHANNEL TOUCH** – channel retest:
     - logic based on a channel (e.g. Donchian/Bollinger),
     - requires touching channel boundaries within lookback.

2. **Retest enabled**
   - Master switch for retest logic.

3. **Confirm close**
   - If enabled:
     - retest is valid only when the **candle closes** inside the band/channel.
   - If disabled:
     - a wick touch (intra-candle) is enough.

4. **Breakout bypass**
   - Allows some strong breakouts to bypass retest (e.g. extreme momentum moves).

5. **Base TF for retest**
   - TF used to compute retest (M1 / M3 / M5 etc.).
   - `Default (from style)` – automatically chosen per style.

6. **Channel lookback** (CHANNEL_TOUCH mode)
   - Candle window to build the channel from.

7. **Band width (%)**
   - Retest band in percent.
   - Example:
     - 0.2% – very tight retest,
     - 0.6% – wider, more tolerant band.

8. **Timeout (minutes)**
   - Maximum time after breakout when retest must occur.
   - After timeout the opportunity is skipped.

There is a **“Restore defaults for style”** button – it resets retest parameters to style-specific defaults (Scalp/Day/Swing).

---

### 6.5. Post-SL signal block

Section **“Block after SL”**:

- Switch – enables/disables cooldown logic after SL.
- Time slider (minutes) – how long after an SL on a given pair **no new signals in the same direction** will be emitted.

This helps mitigate:

- “flip-flop” behavior,
- revenge trading patterns.

---

## 7. ADVANCED tab – TF per filter

In the **ADVANCED** tab you specify which **timeframes (TF)** each filter will use.

Example:

- Trend: M15 / H1,
- Momentum: M1 / M3,
- Bollinger: M3,
- RSI: M5,
- Donchian: M5 / M15,
- etc.

Each filter has a **Multi TF Picker**:

- you choose one or multiple TFs (M1, M3, M5, …),
- empty list = use default TFs derived from the current style.

Limits:

- NONE/BASIC – limited TF count per filter (e.g. 1–2),
- PRO/ELITE – no (or very high) limit.

This tab is mostly for advanced users who want:

- higher TF for trend (H1/H4),
- lower TFs for entries and momentum (M1/M3).

---

## 8. Main screen and signal history

### 8.1. Signal list

On the main screen you see recent signals:

- pair (e.g. BTCUSDT),
- direction (LONG / SHORT),
- entry price,
- targets (TP1/TP2/TP3),
- SL,
- signal status:
  - active,
  - hit TP1 / TP2 / TP3,
  - BE (Break Even),
  - SL.

### 8.2. History

A dedicated tab or screen shows **full signal history**:

- emission time,
- pair,
- result (TP/SL/BE),
- extra diagnostic info (as the app evolves).

---

## 9. Tuning tips

These are **guidelines only**, not a ready-made holy grail.

### 9.1. Start simple

For the beginning:

- Style: **Scalping** or **Day trading**.
- Sensitivity: around **60–70%**.
- Filters:
  - Enable: Trend, Momentum, Donchian, BB, RSI, MACD.
  - Initially you may disable Z-Score / ATR / Volume / EMA200 to see the “core” logic.
- Targets: Fixed,
  - TP1: 0.6–0.8%,
  - TP2: 1.2–1.5%,
  - TP3: 1.8–2.5%,
  - SL: 0.8–1.0%.

### 9.2. Testing changes

- Change **only 1–2 parameters at a time** (e.g. Donchian TF or retest band only).
- Observe **at least dozens to hundreds of signals** before drawing conclusions.
- Look not only at **winrate**, but also:
  - R:R,
  - behavior in different regimes (trend vs. range).

---

## 10. FAQ / common issues

### 10.1. “I see no signals”

Check:

1. Do you have **pairs selected**?
2. Is background work **enabled** (if you expect continuous scanning)?
3. Are your filters too strict:
   - Sensitivity > 80%,
   - every filter enabled,
   - very tight retest band with short timeout.
4. Is your trial/subscription active (otherwise background engine might be limited)?

### 10.2. “Too many SL / poor PF”

Try:

- raising sensitivity (e.g. 60% → 70–75%),
- enabling more trend/momentum filters,
- widening retest band or timeout,
- using **post-SL block** for a few minutes.

### 10.3. “Too few signals”

Try:

- lowering sensitivity (e.g. 80% → 60–65%),
- disabling some filters (Z-Score, ATR, EMA200),
- relaxing retest (wider band, longer timeout).

---

## 11. Summary

Futures Scan:

- combines classic and advanced indicators,
- lets you build your own **signal profile** (scalp/day/swing),
- gives strong control over:
  - filters,
  - targets,
  - retest,
  - background behavior.

Remember:

- the app does not guarantee profit,
- you are responsible for risk management, leverage and psychology,
- the best configurations come from **testing and observation**, not from someone else’s “magic preset”.
