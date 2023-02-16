# Vertical Call Spread

Currently the Katana.io SOL put selling vault is down over 5% since inception. Unfortunately the data is not available on specific drawdowns. From personal experience, we recall one losing week of approximately 14%.&#x20;

\
Digital assets are volatile. To not properly hedge in these markets is unforgivable. Enter the vertical spread, a simple long-short options strategy that caps downside loss.

\
**Trades:** \
Sell 1 10% OTM put for approx. 2.4%Buy 1 20% OTM put for approx. 0.67%\
Net premium 1.73%. Annualized 144% if no down weeks. \
This strategy will have losing weeks when the price of the underlying falls 11.7%. Losses will be capped at 8.27%\
Performance improvement through auctions for midpoint or better pricing, as well as proprietary modelling of optimal strike selection.

\
**Vault mechanics**

* User deposits USDC into vault at anytime-Deposit is held until Friday auction
* Auction held on Friday. Options minting using Zeta Flex or Opium Constructor (flex.zeta.markets or app.opium.finance/eth/constructor)&#x20;
* Auction quantities, in units of underlying = Total deposits  Price of underlying
* Options minted via Zeta lock collateral inside contract. If finishing OTM or ITM, we ‘release collateral’ from Flex UI. Counterparty also required to act to claim PNL if any.
* Proceeds from settled week are rolled to following week unless “Claimed” and withdrawn by user. Claims can be done at any time, withdraws are available after weekly settlement.\
