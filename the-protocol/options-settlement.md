# Options Settlement

Opyn uses Chainlink's spot prices as a data source to settle options. However, Chainlink's data source is not designed to be used for expiries because it uses data sources such as aggregators (CoinGecko or CoinMarketCap) which are often delayed. Chainlink is building a low latency, MEV mitigating oracle solution ([https://blog.chain.link/low-latency-oracle-solution/](https://blog.chain.link/low-latency-oracle-solution/)). Once it is live, it will be considered.

\


Pyth (https://pyth.network/) provides a more accurate view of the price data due to how it fetches real-time price data from exchanges. Until Pyth and Low latency Chainlink are integrated, we are relying on a stopgap solution for bringing over Pyth price data onto Ethereum:

\


* If the option expires out-the-money, we do not do anything. The Chainlink price is used for settlement by default.
* If the option expires in-the-money, we manually dispute the settlement price and set it to Pyth's first spot print at 8am UTC. The dispute process goes through Opyn's dispute multisig.
