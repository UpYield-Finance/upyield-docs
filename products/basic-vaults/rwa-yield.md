# RWA Yield

Real World Assets (RWA) tokenisation is coming of age. More and more protocols offer tokenised RWA and tokenised loans and even T bills. This vault is an index vault investing in a basket of tokenised fixed income products trying to hedge risk by rebalancing assets and using derivatives when those are available (eg interest swap, credit default swaps).

## Benefits

* Risk reduced fixed income
* Cheaper execution obtained by batching of trades. An individual trader will need to execute many trades to achieve the same portfolio.
* Risk management and hedging

## Risks

* Credit Default
* Interest rate risks
* Operational and Execution Risks
* Third party protocol risks

## Vault Strategy

The vault is collecting stable tokens. The vault uses frequent batches to buy tokenised loans from third party protocols. The batching saves fees and helps manage execution risk. That means that every deposit into the vault does not trigger an immediate purchase of tokens by the vault. The vault also buys or sells derivatives for hedging purposes.

\
