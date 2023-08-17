# Cross-Chain Execution

UpYield Finance is a multi chain protocol. That means that the smart contracts can be deployed on different chains. There are different approaches to implement that:

* Independent deployments of vaults to different networks. This means that different vault contracts are deployed on different networks. Then tokens need to be bridged between networks. Also the DApp frontend needs to offer integration with different wallets, especially for non EVM compatible chains.
* Using an inter-chain communication network such as Axelar.network or Layer Zero. This allows the vault contracts to be domiciled in one chain e.g. Arbitrum and use the inter-chain network to transfer assets and execute contracts on other networks.
* Building on Cosmos or Polkadot. These networks are designed as block-chain interoperability hubs. However they limit communication to their respective ecosystems.
* Leveraging Polygon 2.0. Polygon 2.0 aims to develop an universal value layer of the internet. Combining the concepts of decentralised network of chains and inter-chain communication, it takes the best of the Cosmos/Polkadot networks and interchain communication networks. It remains to be seen how it will be implemented.

\


In the first version of the protocol we are choosing to deploy the vault contracts on an EVM compatible network (e.g. Arbitrum) and use an inter-chain communication network such as Axelar. This is because of the maturity of the EVM ecosystem both from a development and liquidity point of view.

\
