# Binance Futures Bot

Professional Windows desktop app for Binance USDT-M Futures with a clean dashboard, deterministic signal logic, and practical risk controls.

![Binance Futures Bot Logo](binancebot_128.png)

## 🚀 Release v2

Download from the GitHub release assets:

- **Installer (recommended):** [BinanceBot-v2-portable-win-x64.exe](releases/download/v2/BinanceBot-v2-portable-win-x64.exe)
- **Portable (no install):** [BinanceBot-v2-portable-win-x64.exe](https://github.com/fancyarcadia/BinanceBot/releases/download/v2/BinanceBot-v2-portable-win-x64.exe)

## 🧭 Product Summary

- ⚡ **Fast desktop experience** (WinForms, low-overhead runtime)
- 📈 **Binance USDT-M Futures focused** workflow
- 🧠 **Deterministic strategy checks** on closed candles only
- 🛡️ **Risk-first execution** with protective stop and trailing behavior
- 🔌 **Testnet + Mainnet support** in one app
- 📋 **Clear logs and trade history** for visibility and review

## ✅ Who Is This For?

- Traders who want a **simple GUI bot** instead of command-line tooling
- Users who prefer **per-symbol settings** (size, leverage, stop loss, cooldown)
- Users who want to **start on Testnet**, then move to Mainnet when ready

## 🖥️ System Requirements

- Windows 10/11 (64-bit)
- Internet connection
- Binance account with USDT-M Futures access

## 📦 Install Guide

### Option A: Installer (Recommended)

1. Download `BinanceBot-v1-setup.exe` from Releases.
2. Run the installer and complete setup.
3. Launch **Binance Futures Bot** from Start Menu/Desktop.

### Option B: Portable

1. Download `BinanceBot-v1-portable-win-x64.exe`.
2. Place it in any folder.
3. Run directly (no installation required).

## 🛠️ Quick Start (Easy)

1. Open the app.
2. Go to **Binance Futures API Setup**.
3. Enter API key + API secret.
4. Start with **Testnet** first.
5. Add symbol(s) like `BTCUSDT`.
6. Set quantity, leverage, stop loss, RSI threshold, cooldown.
7. Enable auto-trade and monitor logs/trade history.

## 📊 Strategy (SL + RSI/BOS)

Minimal strategy summary for real usage:

- Timeframe: evaluates on each new **15m candle close** (closed candles only).
- **BOS trigger**
  - Long setup: `C1.close > C2.high`
  - Short setup: `C1.close < C2.low`
- **RSI confirmation**
  - RSI(6), RSI(14), RSI(24) are checked together.
  - Long: all RSI changes from `C2 -> C1` are positive and pass threshold.
  - Short: all RSI changes from `C2 -> C1` are negative and pass threshold.
- **SL (Stop Loss)**
  - Set in USDT per symbol.
  - Bot places a protective stop after entry and can trail it as profit grows.
- **Cooldown**
  - After exit, symbol waits for configured cooldown hours before new entry.

## 🔐 Security & Trust

- API credentials are protected using **Windows DPAPI encryption** on the local machine.
- Strategy uses **closed-candle evaluation** to reduce noisy/repainting behavior.
- Runtime includes protective stop management, reconciliation checks, and detailed logs.
- Mainnet trading has extra safety flow (including explicit live arming in-app).

Recommended account safety:

- Use API keys with **minimum required permissions** only.
- Keep **withdrawals disabled** on API keys.
- Prefer Testnet validation before any live deployment.

## ⚠️ Risk Notice

Trading futures is high risk. This software helps with automation, but it does not remove market risk, slippage, or exchange-side execution variance. You are fully responsible for your trades and capital.

## 🤝 Contribute / Developer Contact

Contributions are welcome:

- Open an issue for bugs/feature requests
- Submit a pull request with clear changes
- Discuss collaboration by email: **fancyarcadia@gmail.com**

## ❤️ Donate

If this project helps you, donations are appreciated.

**BNB (BEP-20) Address**

`0x46510768443cbfdb3f15f96118e7d71c9eb7da91`

**Scan QR**

![Donate QR](qr-code.png)
