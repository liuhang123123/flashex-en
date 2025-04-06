# Trading Workflow

## Pre-requisites

* Successfully bound OKX API
* USDT assets available in your OKX trading account (shown on FlashEX home screen)

## Step-by-Step Order Process

1. **Select a Trading Pair**
   * Navigate to the list of USDT-margined perpetual contracts on the FlashEX homepage
   * Search for additional tokens if not listed
2. **Choose Order Mode**
   * FlashEX supports: Limit Order, Market Order, and Planned Order
   * Any mode will include both entry and exit configuration

## Detailed Order Modes

**Limit Order**

* Opens a trade at a specified price. May not fill instantly in fast markets

**Market Order**

* Opens a trade immediately at the best available price. Ensures full fill but may have higher cost

**Planned Order**

* Automatically places entry/exit orders when prices hit user-defined thresholds (percentage-based deviation from current price)

## Profit Configuration

All order types allow setting a target profit percentage, automating both entry and exit:

* **Limit Mode**: Entry at latest price; exit at calculated profit target
* **Market Mode**: Entry at dynamic best price; exit based on profit percentage
* **Planned Mode**: Entry and exit prices calculated from user-set deviation and profit margin

## Order Management & Monitoring

After placing an order (long or short), users enter the **real-time PnL view** where they can:

* Track position status
* View entry, exit, liquidation, and stop-loss prices
* Monitor real-time profits and trade progress
* Execute manual close (market or limit)

When all steps are completed, FlashEX will automatically place a closing order upon position opening—executing automatically once the target price is reached.

<figure><img src="../.gitbook/assets/Group 1.png" alt=""><figcaption></figcaption></figure>
