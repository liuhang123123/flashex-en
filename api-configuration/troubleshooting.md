# Troubleshooting

## FlashEx — Supported Trading Types

🎯 **Supported Exchange**\
Currently supported: **OKX** (via API integration for trading)

💰 **Supported Contract Type**\
✅ USDT-Margined Perpetual Futures\
FlashEx focuses exclusively on:\
**USDT contracts × Perpetual Futures × Manual entry + Auto take-profit arbitrage**

🔄 **Supported Trading Pairs** _(based on OKX platform)_\
All USDT-margined perpetual futures pairs available on OKX, such as:

* BTC/USDT
* ETH/USDT
* SOL/USDT
* XRP/USDT
* DOGE/USDT\
  ...and many other major or trending tokens.

📌 Newly listed USDT perpetual contracts on OKX are typically supported by FlashEx automatically.

⚙️ **Supported Order Types**

| Order Type        | Description                                                                 | Suitable For                         |
| ----------------- | --------------------------------------------------------------------------- | ------------------------------------ |
| **Market Order**  | Executes immediately at the best market price                               | Quick entries, momentum trading      |
| **Limit Order**   | Places an order at a specified price, waits for execution                   | Price control, slippage avoidance    |
| **Planned Order** | Automatically triggers entry + take-profit based on user-defined conditions | Strategic entries with profit target |

🧠 **FlashEx Arbitrage System Highlights**

* ✅ One-click order entry + auto-generated take-profit limit order
* ✅ Supports long & short positions
* ✅ Customizable profit targets (% based)
* ✅ Real-time tracking of PnL and take-profit status
* ✅ No black-box logic: 100% user-initiated & controlled

❌ **Currently Not Supported**

* Spot trading (token-to-token swaps)
* Margin accounts
* Coin-margined or delivery contracts
* Automated quantitative strategies (e.g., grid bots, martingale)

***

## 🔎 FlashEx — API Connection Verification Guide

📌 **Context**\
After completing API authorization with OKX, users should verify if the connection is successful and data is properly synced.

👉 _If you have not yet configured OKX API access, please refer to: \[_[_API Setup Guide_](api-configuration.md)_]_

***

#### ✅ Step-by-Step Connection Checks

#### 1️⃣ **Check API Connection Status**

* Open FlashEx App
* Go to **Main menu → Settings (API Management)**
* Confirm that the status shows **“Connected to OKX”**\
  ✅ If connected, API read access is working.

***

#### 2️⃣ **Check Balance Sync**

* On the FlashEx home screen (bottom left), confirm:
  * Whether your USDT balance from OKX is displayed
  * If balance shows **0**, but you have assets on OKX:
    * Check whether funds are in the **Futures Account**
    * FlashEx only reads **USDT balance from the Futures Account**, not from Funding or Spot

✅ If your balance appears correctly, the API is connected successfully.

***

#### 3️⃣ **Test Order Execution**

Try placing a small test order:

* Select a supported contract (e.g., BTC/USDT)
* Choose a Market or Limit Order
* Enter size, then click **Long** or **Short**

✅ If the order is placed and an auto take-profit order is generated, API connection & trading permission are both functioning.

***

#### ❌ If API Connection Fails, Please Check:

* Whether you're using the **recommended OAuth (automatic) authorization**
* Whether your API permission includes both **“read” and “trade”** (withdrawal not required)
* If the API key has been deleted, expired, or disabled in OKX backend
* If there are any network issues or outdated FlashEx App versions in use

***

### ❗ FlashEx — “No Balance” Troubleshooting

#### 📍 Problem:

FlashEx successfully logged in, but the bottom of the home screen shows:\
&#xNAN;**“Available Balance: 0”**

👉 _If you have not yet configured OKX API access, please refer to: \[_[_API Setup Guide_](api-configuration.md)_]_

***

#### ✅ Step-by-Step Troubleshooting

**① Ensure API Authorization is Completed**

* ✅ Login to FlashEx → Check API status in settings shows “Connected”
* ✅ Ensure OKX is the authorized exchange, with both “read” and “trade” permissions 👉 If not authorized or expired, re-bind via **OAuth (recommended)**

***

**② Ensure Funds are in the OKX Futures Account**

FlashEx reads data only from **Futures Account**, not Spot or Funding.

✅ Steps:

* Open OKX App
* Go to **Assets → Account Types: Funding / Spot / Futures**
*   If funds are not in the Futures Account:

    > Tap **Transfer → From: Funding → To: Futures → Enter amount → Confirm**

📌 FlashEx supports: **USDT in Futures Account**

***

**③ Ensure You Are Using a Supported Contract**

FlashEx only supports **USDT-margined perpetual futures** on OKX.\
If your funds are in spot/other accounts, balance won't show, and you can’t place orders.

***

#### 🚨 Additional Notes:

* 📌 **FlashEx never holds your funds** — your assets remain entirely in your own OKX account
* ⏱ If you've just transferred funds, refresh or re-enter the app to update
* 📲 Make sure you're using the latest version of the FlashEx App
