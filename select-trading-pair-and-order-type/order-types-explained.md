# Order Types Explained

## Order types&#x20;

FlashEx supports three order types to meet different trading needs:\
**Limit Order**, **Market Order**, and **Planned Order**.

<figure><img src="../.gitbook/assets/Group 219.png" alt=""><figcaption></figcaption></figure>

***

### 🟩 **Limit Order**

In **Limit Order** mode, the system places an entry order at the latest market price of the selected trading pair from the exchange. The order remains open at that price until it is fully filled.

📌 **Important Note:**\
Limit orders are **not guaranteed to fill immediately**, especially during periods of high market volatility. If the market price rapidly moves away from the specified limit, the order may be delayed or partially filled, resulting in **waiting time or slippage**.

✅ This mode is suitable for traders who:

* Require precise entry pricing
* Are willing to wait for better execution conditions

***

### 🟦 **Market Order**

A **Market Order** executes immediately at the best available market price. Once the user places the order, the system automatically matches it with existing orders in the order book to ensure the **fastest possible execution**.

✅ Recommended for:

* Users who prioritize **execution speed** over price
* Scenarios such as **urgent market entries** during news or sudden price movements

⚠️ Market orders may experience some slippage due to price fluctuation during execution.

***

### 🟨 **Planned Order**

The **Planned Order** mode allows users to predefine both the **entry price** and **take-profit price** based on specific market conditions. Once the criteria are met, FlashEx automatically executes both the entry and exit orders — creating a fully automated trading cycle.

**How it works:**

* **Entry Price:**\
  Automatically calculated as a percentage offset from the current market price (e.g., "a%" below or above the current price)
* **Take-Profit Price:**\
  Automatically calculated based on the entry price with a profit target percentage ("b%")

***

**📈 Long Position Logic:**

* Entry is triggered when the market price **drops to (current price - a%)**
* Once the entry is filled, the system automatically places a **take-profit order at (entry price + b%)**
* If the market rises to the take-profit level, the position is closed and profit is secured

**📉 Short Position Logic:**

* Entry is triggered when the market price **rises to (current price + a%)**
* Once the entry is filled, the system places a **take-profit order at (entry price - b%)**
* If the market falls to the take-profit level, the position is closed with profit

✅ This mode is ideal for:

* Traders with clear entry and profit targets
* Executing trades in specific price zones
* Lowering potential entry cost compared to market orders
