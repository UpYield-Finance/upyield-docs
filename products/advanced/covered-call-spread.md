# Covered Call Spread

Selling covered Calls is a great strategy to generate yield from the collection of option premiums. However, if the underlying asset price increases above the strike price, the investor is giving up any upside. If a call option is purchased, it can offer profit from price appreciation. This type of strategy is typically called a vertical spread. Buying and selling the same option at the same time at different strike prices. Since the goal of the vault strategy is to generate yield, the difference between the premium collected for selling a call option and the premium paid to buy the second call needs to be positive. That means that the option that is bought needs to be even further out of the money than the options sold.



**When to Use:**&#x20;

* Lower yield than covered calls but higher upside in a bull market
* In a bearish scenario, the investor loses less than from just holding the asset (he receives the option premium)
* In a mildly bullish scenario, the investor forgives part of the upside from just holding the asset.
* In a bullish scenario the investor still benefits from the upside

**Risks**:

* If the price of the asset declines too much, the investor will incur potential losses, that may not be covered by the profit from option premiums
* Operational and Execution Risks
* Third party protocol risks\


**Vault strategy:**

&#x20;Weekly European Call Options are sold and bought every Friday at an auction. The strike price of the call option to be sold is selected in order to achieve a delta of less than 0.2. This is in order to minimise the likelihood of the options expiring at the money.

The price of the option to be bought needs to lower in order to generate positive cash flow.

\
\
