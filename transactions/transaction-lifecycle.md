# Transaction lifecycle

A transaction passes through several steps before it is completed.

### 1. Create

A wallet or application prepares the transaction.

The transaction may include:

* recipient;
* QTER amount;
* contract data;
* gas settings;
* network chain ID.

### 2. Sign

The wallet asks the user to review and sign the transaction.

Before signing, confirm:

* the network is Qantera Public Testnet;
* the chain ID is `974621`;
* the recipient is correct;
* the amount is correct;
* the gas fee is acceptable.

### 3. Broadcast

The signed transaction is sent to a Qantera RPC endpoint.

Primary RPC:

[https://rpc1.qantera.network](https://rpc1.qantera.network)

Backup RPC:

[https://rpc2.qantera.network](https://rpc2.qantera.network)

### 4. Pending

The transaction waits to be included in a block.

During this stage, the wallet may display the transaction as **Pending**.

### 5. Execution

The network processes the transaction.

The transaction may:

* complete successfully;
* fail and revert;
* remain pending if the network or fee settings cause a delay.

### 6. Block inclusion

The transaction is added to a block.

A block number and transaction receipt become available.

### 7. Confirmation

The transaction can be viewed on the [Qantera Explorer](https://explorer.qantera.network/).

The explorer displays:

* status;
* sender;
* recipient;
* transferred value;
* gas used;
* block number;
* transaction data.
