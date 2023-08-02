# Market Neutral Liquid Staking

## Description

Liquid staking is one of the largest markets in DEFI. It offers staking returns to investors while alleviating the constraints related to staking: lock-in periods, minimal amounts, and most importantly the need to provide and manage hardware. Liquid staking protocols such as Lido Finance, allows anyone to stake ETH or other assets (Solana, Matic) and receive “staked tokens” as a deposit receipt. The staked tokens are exposed to the price changes of the underlying asset. By offering a hedge against the asset price change, this strategy effectively offers a fixed income product.



## Benefits

* Fixed income with alternative risk profile (source of income is from PoS networks)
* Cheaper execution obtained by batching of trades. An individual trader will need to execute many trades to achieve the same portfolio.

## Risks

* Operational and Execution Risks
* Third party protocol risks
* Market risks that can result in bad hedging

## Vault Strategy

The vault is collecting stable coins (eg USDC) and they are used by the vault to buy assets (ETH, Matic, Solana, and others) from DEXes. Then those assets are deposited into liquid staking protocols such as LIDO and RPL. This will create an exposure to the price of the underlying asset (ETH, SOL, etc). In order to hedge to neutralise the market exposure, the vault also opens a short perpetual position in a perpetual future exchange such as GMX.

\


\
