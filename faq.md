---
description: Most Common Questions
---

# FAQ

### **What are tokenised vaults?**

A tokenized vault holds a specific ERC20 token and gives shares to the users that deposit assets in it. When a user deposits funds, the vault will mint a specific number of shares for the user. When the user withdraws tokens from the vault, the correspondent amount of shares will be burnt.

### **Do you have hidden fees?**

The vault fee structure consists of a 1% annualised management fee and a 10% performance fee. All fee payments are traceable on-chain.

### **What are structured products**

Structured products are pre-packaged investments that normally include assets linked to interest plus one or more derivatives. They are generally tied to an index or basket of securities, and are designed to facilitate highly customised risk-return objectives.

### **What are Decentralised Options Vaults**

Decentralised Options Vaults (DOVs) are structured products offered on-chain, closely related to TradFi counterparts that combine several financial instruments to create a whole new payoff curve. The core function of DOVs is to use investors’ capital and employ options trading strategies in a completely automated and decentralised manner. These strategies may include covered calls, protective puts, or straddles. Before DOVs, option strategies were only available to accredited investors through over-the-counter (OTC) trading or by self-execution on option exchanges like Deribit.

### **What are the risks involved?**&#x20;

While DEFI removes some of the risks related to centralisation, there are other risks such as smart contract risks. Please refer to the risk section in docs.

### **What are the staking rewards?**&#x20;

The governance token needs to be staked in order to be eligible for DAO votes and for staking rewards. At the moment 25% of the protocol fees are paid to staked token holders.

### When can I deposit?

A user can deposit into the a vault at any time. However most vaults (option vaults) run weekly epochs. On a new epoch, all deposited funds become locked and participate in the vault strategy. Before the epoch starts, funds that are unlocked can be withdrawn at anytime, but don't earn yield.

### When can I withdraw?

There are two phases to completing a withdrawal: initiating withdraw and claiming withdrawals. Funds that were not locked can be withdrawn at any time using "Claim Withdrawal" action. For funds that are locked, an "Initiate Withdrawal" Action needs to be called. Then, funds join the withdrawal pool and once. they are become unlocked (eg after Friday morning each week), they can be claimed using "Claim Withdrawal" action.

