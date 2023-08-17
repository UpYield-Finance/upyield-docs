# Vault Lifecycle

This is the typical flow of funds in a vault:\


1. Users deposit funds into the vault and receive tokens representing a share in the vault. Those funds are redeemable at all times until they are locked during an “epoch”. An epoch is a weekly options cycle for options based products. Users send their vault tokens to redeem their funds.
2. When a new epoch starts, deposited funds get locked. All subsequent deposits during the “epoch” remain unlocked and ‘on-hold’ until the next  epoch.
3. The vault calls the pricing algorithm that uses market data from oracles and on-chain metrics to produce pricing parameters for the derivatives to be created (eg. option strike price).
4. The vault uses third-party minting protocols to create and mint derivative tokens with the supplied parameters (e.g. minting option tokens). The vault  provides required collateral to the minting contract, and collects the tokens representing the derivative contracts.
5. The new derivative tokens are traded  on the market typically at auction in the absence of deep and liquid orderbook markets .
6. Premiums are collected and unsold tokens are destroyed/burned.
7. At settlement time, potential profits or losses are settled by the vault with derivative token  holders.
8. Each minting protocol provides  a dispute period to manage any possible technical issues and litigation.
9. At the end, the epoch is completed  and funds are unlocked.
10. Any remaining  funds will automatically be rolled over to the next epoch.
