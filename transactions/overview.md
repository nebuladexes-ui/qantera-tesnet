# Overview

Transactions are used to change data on the Qantera Public Testnet.

A transaction can be used to:

* send QTER to another address;
* deploy a smart contract;
* call a function that changes contract data;
* interact with a decentralized application.

### Transaction information

A transaction normally includes:

* sender address;
* recipient address;
* transferred amount;
* gas fee;
* transaction data;
* transaction hash;
* block number;
* execution status.

### Read and write operations

#### Read operations

Read operations retrieve blockchain data without changing it.

Examples:

* checking a wallet balance;
* reading a contract value;
* viewing transaction information.

Read operations do not require gas.

#### Write operations

Write operations change blockchain state.

Examples:

* sending QTER;
* deploying a contract;
* updating contract data.

Write operations require a wallet signature and QTER for gas.

### Check a transaction

Use the [Qantera Explorer](https://explorer.qantera.network/) to search for:

* transaction hashes;
* wallet addresses;
* blocks;
* smart contracts.

A transaction can be:

* **Pending** — waiting to be included in a block;
* **Success** — executed successfully;
* **Failed** — included but execution was reverted.
