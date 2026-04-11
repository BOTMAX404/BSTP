# Zihad Broker — Binance Spot Trading Terminal

> **Developed by MD GOLAM SAROWER ZIHAD**

A professional browser-based Binance Spot trading terminal with a 4-Line automated trading bot. Runs entirely in your browser — no backend server, no data collection.

---

## 🚀 Live Site

**[https://YOUR-USERNAME.github.io/YOUR-REPO-NAME](https://your-username.github.io/your-repo-name)**

*(Replace with your actual GitHub Pages URL after setup)*

---

## ✨ Features

### Real-Time Trading
- Live Binance WebSocket price feeds (real-time candlestick charts)
- Supports **Live Account** (real money) and **Demo / Testnet** mode
- 12+ trading pairs: BTC, ETH, BNB, SOL, XRP, ADA, DOT, LINK, AVAX, MATIC, DOGE, LTC
- Multiple timeframes: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 1d

### 4-Line Automated Bot
| Line | Function |
|------|----------|
| **Buy Line** | Bot places a market buy when price touches this level |
| **Pass Line** | Activates the pass zone — allows candle to move through 1st Sell upward; triggers instant sell on reversal |
| **1st Sell Line** | Trailing stop — moves up automatically every X minutes by $Y; sells instantly when touched |
| **2nd Sell Line** | Hard take-profit target; optional auto-move-up on every new candle close |

### Security
- API keys stored **only in your browser's localStorage** — never sent to any third party
- All signing done client-side using Web Crypto API (HMAC-SHA256)
- No server, no database, no tracking

---

## 📦 How to Deploy on GitHub Pages

### Step 1 — Create a GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Name it anything (e.g. `zihad-broker`)
3. Set to **Public**
4. Click **Create repository**

### Step 2 — Upload the Files
Upload these files to the root of your repository:
```
index.html   ← main trading terminal
404.html     ← page redirect (required for GitHub Pages)
README.md    ← this file
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main` | Folder: `/ (root)`
4. Click **Save**

### Step 4 — Access Your Site
Your site will be live at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```
*(Takes 1–2 minutes to go live after first deploy)*

---

## 🔑 API Key Setup

### For LIVE Trading (Real Money)
1. Log in to [binance.com](https://binance.com)
2. Go to **Profile → API Management → Create API**
3. Enable **Spot Trading** permission only
4. ❌ **Disable withdrawal permissions** (safety)
5. Whitelist your IP address if possible
6. Paste Key + Secret into the terminal gate

### For DEMO Trading (Testnet)
1. Go to [testnet.binance.vision](https://testnet.binance.vision)
2. Log in with GitHub
3. Generate API keys there
4. Select **Demo / Testnet** tab in the terminal gate
5. Paste Testnet Key + Secret

---

## ⚠️ Security Rules

- **Never share your API keys** with anyone — not in chat, not in screenshots
- **Never enable withdrawal permissions** on a trading API key
- If you ever accidentally expose a key, **delete it on Binance immediately**
- This app runs 100% in your browser — your keys never leave your device

---

## 🛠 Tech Stack

| Component | Technology |
|-----------|------------|
| Charts | TradingView Lightweight Charts v4.2 |
| Fonts | Space Grotesk + JetBrains Mono (Google Fonts) |
| API Signing | Web Crypto API (HMAC-SHA256) |
| Data | Binance REST API + WebSocket Streams |
| Hosting | GitHub Pages (static) |
| Backend | None |

---

## 📋 File Structure

```
/
├── index.html    # Complete trading terminal (self-contained)
├── 404.html      # GitHub Pages redirect
└── README.md     # This file
```

---

*Developed by **MD GOLAM SAROWER ZIHAD***
