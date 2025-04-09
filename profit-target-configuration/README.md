# Profit Target Configuration

FlashEx supports three types of order placement modes: **Limit Order**, **Market Order**, and **Planned Order**.\
In all three modes, users can complete both the **entry (open)** and **exit (close)** configuration in a single setup process.

***

### 🟩 **Limit Order Mode**

**Entry (Open Position):**\
The system places a limit order using the **current market price** as the reference. The order remains pending until the market price matches the set price and the position is fully opened.

**Exit (Take-Profit):**\
Once the entry order is filled, the system calculates the take-profit price based on the **actual filled price and the user's preset profit percentage**, then automatically places a limit close order.

**Details:**

* **Long Position:**\
  After a successful long entry, the system sets a limit take-profit order at:\
  `Filled Price + (Filled Price × Target Profit %)`.\
  Once the market price rises to the take-profit level, the order is executed, completing the full trade cycle.
* **Short Position:**\
  After a successful short entry, the system sets a limit take-profit order at:\
  `Filled Price - (Filled Price × Target Profit %)`.\
  Once the market price falls to this level, the order is executed, and the trade is closed.

***

### 🟦 **Market Order Mode**

**Entry (Open Position):**\
The system instantly executes the order at the **best available market price**, enabling fast order fulfillment.

**Exit (Take-Profit):**\
After the market order is filled, the system calculates the take-profit target using the **actual filled price and user-defined profit percentage**, and places a limit close order automatically.

**Details:**

* **Long Position:**\
  After opening a long, the system sets a limit close order at:\
  `Filled Price + (Filled Price × Target Profit %)`.\
  When the market reaches this level, the order is executed.
* **Short Position:**\
  After opening a short, the system sets a limit close order at:\
  `Filled Price - (Filled Price × Target Profit %)`.\
  The position is closed when the market hits this price.

***

### 🟨 **Planned Order Mode**

**🟢 For Long Positions:**

* **Entry:**\
  The system calculates a buy-limit price at:\
  `Current Price - Entry Offset % (user-defined)`\
  and places the order when the market hits this level.
* **Exit:**\
  Once the entry is filled, the system places a limit sell order at:\
  `Filled Entry Price + (Filled Entry Price × Target Profit %)`\
  to close the trade when the target is reached.

**🔴 For Short Positions:**

* **Entry:**\
  The system calculates a sell-limit price at:\
  `Current Price + Entry Offset % (user-defined)`\
  and places the order when the market rises to this level.
* **Exit:**\
  After the short entry is filled, the system places a limit buy order at:\
  `Filled Entry Price - (Filled Entry Price × Target Profit %)`\
  to close the position when the market drops to the take-profit price.

📌 This mode is ideal for traders who:

* Want **precise entry and exit pricing**
* Can **wait for favorable price conditions**
* Seek to **automate the entire arbitrage cycle**
