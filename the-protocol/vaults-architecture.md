# Vaults Architecture

A vault is a smart contract that manages client funds. Vault users can deposit funds into the vault and they receive share tokens in return that play the role of vault shares. Vaults have infinite lifespan and users can deposit and withdraw funds at any time. However funds need to be locked for specific periods of time, typically a week for options-based products. Those funds are used as collateral for the trading strategy implemented by the vault. Trading profits accrue over time in the vault and the value of the token share is re-calculated with each weekly cycle. When users withdraw from a vault, they convert their vault tokens back to the original asset based on the latest vault token price.



Each Vault offers a unique trading product and risk/reward payoff, and can be deployed in different chains (Ethereum, Solana, Layer 2 chains). They are usable within the same base UI. Vaults are implemented as generic smart contracts (see smart contract architecture) as much as possible, in order to make it easy to extend the protocol with new strategies. There is a separation between the vault functionality which manages deposits and trading strategies. A vault could employ multiple strategies. Strategies are implemented as smart contracts, but they also require integration with external oracles for market data and integration with an external compute system in order to execute complex algorithms that cannot be executed as smart contracts. For example, for option selling strategies, the price feeds come from an oracle and the pricing algorithm is executed as an off-chain program using Black-Scholes formula.



Here is a high level diagram of the vault architecture:

\


![](https://lh5.googleusercontent.com/2LolwNO9rAjTWetZJocuOeUDdfwXnmokdWAEGFFo9Qv9XrhCOalBeHiDV2ATtq6Y22fmWkAGKlLKKdFPgzS2e9WM7kWHhzTFE3d1OUXB4E6JnBkZw7F6q-ayX0ypCzeKiK7BnOG4sqXOUQVNZPG-8GE)

\


**Investment wallet**: this is the investor’s wallet used to interact with the vault

**Vault**: A group of smart contracts implementing a specific vault

**Pricing algorithm**: vaults require input parameters from the market. For example, option strike price selection. The algorithm itself and the market data are off-chain.

**Minting  protocol**: The Minting  protocol is a third party protocol used by the vault to mint new DEFI derivative tokens. For example for DEFI options:  Opyn, Dopex, Lyra, Zeta.

**Market**: this is where the derivatives are traded once created. In some cases it can be the same protocol used to mint them like Dopex, Lyra, Zeta. In other cases those derivatives are sold at auction on a liquidity  platform like Paradigm.
