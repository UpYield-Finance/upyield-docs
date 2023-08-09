# Collar

## Description

This strategy combines a holding in a digital asset (e.g., Bitcoin) with the simultaneous sale of an out-of-the-money (OTM) call option and purchase of an OTM put option on the same asset and with the same expiration. Typically, an investor would deposit their digital assets into a vault and accrue a small yield periodically from the net option premiums (the price of the call net of the price of the put). Their downside is significantly reduced (by the put strike plus the net premium received) if their assets’ price declines. Their upside is limited by the strike price of the call option (typically 10%) for the duration of each contract (typically 1 week). The protocol will automatically trade options subject to pre-defined rules (min yield, min strike) and based on market conditions.



Since the goal of the vault strategy is to generate yield, the difference between the premium collected for selling the call option (OTM) and the premium paid to buy the put option needs to be positive.



## Use case

&#x20;   • Investors who are willing to retain some exposure to their digital assets in the medium/long term but worry about significant permanent loss of capital while also like generating some current yield.

&#x20;   • Investors who believe in the gradual price appreciation of their digital assets in the long term, but not necessarily in an imminent strong rally.

\


## Risks

&#x20;   • The price of the digital assets may decline. The investor will incur losses, until the protective put kicks in, which may not be covered by the profit from the net option premium. In any declining market, if options are traded by the vault, the investor will always be better off than if they simply held on to their assets.

&#x20;   • If the price of the assets is above the call strike price on the expiry of the contract (e.g., at the end of the week), the investor will miss out on any additional upside beyond the strike price. A portion of their asset worth the additional upside will be automatically sold to settle the expiring call option (in this case the put will naturally expire unexercised).



## Trading process

Weekly European call and put options will be sold at auctions every Friday. The strike prices will be set subject to transparent rules to achieve a balance between yield, upside and downside protection. E.g., in the current market conditions, we can suggest a strike of 110% for the calls and 90% for the puts. The protocol would not sell options in certain situations when market demand is insufficient and potential yields are too low. E.g., in the current market conditions, we can suggest a min of 1% annualised yield (roughly 0.02% per week).

\


## Example

&#x20;   • Selling 10% OTM (the strike is 110% of the current market price) weekly BTC calls while buying 10% OTM puts (the strike is 90% of the current market price) at the market can generate c.3% annualised yield currently. The investment will be protected if BTC drops more than 10% over the week, while BTC price appreciation upside will also be limited to 10%.

&#x20;   • The investor receives the net option premium but top slices their upside (in case their Bitcoin rallies hard) while protecting their downside (in case their BTC tanks).\


<img src="https://lh4.googleusercontent.com/wTF4VNGh2HG96md0vrYaI8thL44YFmcAljdc_ldqrfXHgB6wYd7O4woxqgdz7iXute0qoFM4_nkjysn02HT6JFvO0m-M_tbtCIcRBKrRBo8kwpovkSZZx5gdO-Lyg3S_hOXQSPdR21e_V8WGsOKiAqw" alt="" data-size="original">



\
