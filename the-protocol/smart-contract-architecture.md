# Smart Contract Architecture

The protocol is built using a modular and extensible architecture, allowing for easy implementation of new strategies. Vault contracts are separated from the Strategy contracts. Vaults manage the funding part - deposits, withdrawals etc. While the strategy contracts abstract the trading strategy part. A  vault could implement multiple strategies. This is a design that is also used by Yearn Finance.

\


![](https://lh6.googleusercontent.com/rbK8pfHKu1KKDUGJMku\_24qfjr\_CByVOfYOLoSivkk8xTjOdWfX8HRSV8f4VW1wSKstA95sCpLUqxgNz0HQyL15Nt-6-JOhfgyEz8cvGkDXwQAOr-eP3-h81sXuZEpH7mmWEI8uddZvW1hxaAxFrh0Y)

* BaseVault - base vault contract managing deposits and withdrawals
* OptionsVault - a generic contract for options based vaults
* VaultRegistry - registry managing vaults lifecycle
* Strategy - implements a trading strategy. a vault can have one or many strategies
* VerticallCallSpreadStrategy - a specific strategy
* OptionPriceOracle - base interface for option pricing data

\
Vault contracts are upgradable, using the upgradable proxy pattern: [https://docs.openzeppelin.com/upgrades-plugins/1.x/writing-upgradeable](https://docs.openzeppelin.com/upgrades-plugins/1.x/writing-upgradeable) . This is to avoid the need to migrate clients and their funds to new vaults if a change is needed. Every contract upgrade is controlled by the UpYield Finance DAO and its representatives.
