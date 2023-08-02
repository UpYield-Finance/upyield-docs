# Protective Puts

In this strategy the investor sells out of the money put options on underlying asset (e.g. Bitcoin). Typically an investor would deposit stable-coins into a vault and it will accrue yield from the options premium. The protocol will automatically create and sell put options at a price calculated by an algorithm based on market conditions.\


**Benefits**

* Best in bull to moderately bearish markets
* Put selling is ideal for a user who wants to accumulate more stable coins and holds the a market view that the market will be moving sideways or upwards for the duration of the sold put option.\


**Risks**

* If the price of the underlying asset goes below the put option’s strike price at expiration and the options are in-the-money, The vault may incur a loss.
* Operational and Execution Risks
* Third party protocol risks



**Vault strategy**

Weekly European Call Options are sold every Friday at an auction. The strike price is selected in order to achieve a delta of less than 0.2. This is on order to minimise the likelihood of the options expiring at the money.

\
