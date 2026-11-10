# Trading Terminal

A crypto trading terminal in a single HTML file: manual demo trading with charts, three trading bots (15-minute, 1-hour and 4-hour), a Smart Money Concepts (SMC) assistant, market news analytics, live quotes, and a trader's encyclopedia with a wiki and glossary.

No server, no installation, no external libraries. Open the file in a browser, or install the Android app.

> **Demo by default.** All trades are virtual unless you connect an exchange account. Prices are real public market data from Bybit and Binance. This is not financial advice. Past results do not guarantee future returns.

The interface is in Russian.

## Download

Version 1.3. All files are in the [`download`](download) folder: open a file there and press the download button. [`torgovyi-terminal-1.3.zip`](download/torgovyi-terminal-1.3.zip) contains everything at once.

| File | What it is |
|---|---|
| `torgovyi-terminal.html` | **Pro**: everything, including bots and SMC. A real exchange account is read-only |
| `torgovyi-terminal-basic.html` | **Basic**: no bots and no SMC assistant |
| `torgovyi-terminal-client.html` | **Client**: same as Pro, but can trade a real account directly from the browser |
| `torgovyi-terminal.apk` | Pro for Android 7.0+ |
| `torgovyi-terminal-basic.apk` | Basic for Android; installs alongside Pro |

## Getting started

- **Desktop:** download an HTML file and open it in Chrome, Edge or Firefox.
- **Android:** download the APK on your phone and open it. Allow installation from this source when asked. New versions install over old ones and keep your data.

## Features

**Terminal**
- Custom canvas chart: candles, volume, position, stop, take-profit and liquidation levels, trade markers.
- Drawing tools: lines, rays, levels, zones, Fibonacci (with the 0.618–0.786 OTE zone), long/short position tool with risk:reward.
- Order ticket with position sizing from risk (% or $), stop and take-profit from the chart, leverage, trailing stop. Shows size, margin, loss at stop, profit at target, R:R, liquidation price and fees.
- Strategy profiles and a risk manager: daily loss limit with a lock until the end of the day, "stop for today", weekly limit freeze.
- Trade journal and statistics in R, equity curve, notes, CSV export.

**Bots**
- Three independent bots (15m, 1h, 4h), each with its own deposit, coin basket, positions, log, risk settings and emergency stop.
- Strategy: long-only pullback to the 20 EMA in an uptrend, with a BTC daily trend filter and a wide trailing stop ("runner").
- Ten presets; the same code runs the backtest and the live bot, so they match candle for candle.

**SMC assistant**
- Market structure (BOS/CHoCH), order blocks, fair value gaps, liquidity sweeps, premium/discount zones.
- Setup card with reasoning and historical statistics for similar setups.

**Analytics, quotes, encyclopedia**
- News radar with impact estimates, refreshed several times a day.
- Quotes with a trend score and market regime (BTC vs. its 200-day average).
- Encyclopedia: learning path, wiki articles, library of books and research papers, glossary, a "dictionary of schools" (the same market phenomenon under different names), and a weekly-updated "What's new in trading" section.

## Exchange connection

Window "Счёт на бирже" (Exchange account) → "Подключить биржу" (Connect exchange). Bybit and Binance USDT futures: demo account, testnet, live account.

- Create an API key **without withdrawal permission**. Keys with withdrawal rights are rejected.
- Keys are stored only on your device, encrypted with your password, and are never sent anywhere else.
- Start with a demo account.

## Backtest results (honest numbers)

Parameters were tuned on 2019–2023 and evaluated on 2024–2026 data the tuning never saw, with Bybit fees (maker 0.02%, taker 0.055%) and 0.02% slippage:

- Bots: roughly +17% to +56% per year on the test period, with drawdowns around 27–28%. Holding the same coins returned about −3% per year.
- A later independent re-check of the 4-hour strategy on 12 coins (1% risk per trade, up to 5 positions) gave about +12% per year with a −29% maximum drawdown on 2024–2026. Simply holding BTC while it was above its 200-day average gave about +24% per year with a −32% drawdown.
- Scalping on 15-minute and 1-minute candles and "bare" SMC rules lost money after fees.

The test period is under three years and mostly a rising market. Treat these numbers as a range, not a promise.

## Limitations

- Bots run only while the page or app is open.
- Data (journal, settings, encrypted keys) lives in the browser or app. Uninstalling the app or clearing browser data erases it.
- Long-only strategy: in a long bear market the bots will mostly stay idle.

## Disclaimer

For education and research. Not financial advice. Trading cryptocurrencies, especially with leverage, can lose you all of your money.
