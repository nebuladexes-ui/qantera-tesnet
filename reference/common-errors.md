# Common errors

This page explains common problems when using Qantera Public Testnet.

### Wrong Chain ID

#### Problem

The wallet is connected to the wrong network.

#### Solution

Confirm:

```
Chain ID: 974621
```

Remove the incorrect custom network and add Qantera again.

### RPC Connection Failed

#### Problem

The wallet or application cannot connect to the primary RPC.

#### Solution

Switch to the backup endpoint:

[https://rpc2.qantera.network](https://rpc2.qantera.network)

Also check:

* internet connection;
* RPC URL spelling;
* browser or firewall restrictions.

### Insufficient Funds

#### Problem

The wallet does not have enough QTER to complete the transaction.

#### Solution

Make sure the balance covers:

* the transferred amount;
* the gas fee.

The public faucet will distribute `0.1 QTER` per successful claim when it becomes available.

### Transaction Pending

#### Problem

The transaction has been submitted but has not been included in a block.

#### Solution

Check:

* wallet balance;
* transaction nonce;
* RPC availability;
* current network activity.

Search the transaction hash on the [Qantera Explorer](https://explorer.qantera.network/).

Do not repeatedly submit the same transaction without checking its status.

### Transaction Failed

#### Problem

The transaction was included in a block but execution failed.

#### Solution

Check:

* transaction receipt;
* gas limit;
* contract error;
* function parameters;
* wallet permissions.

A failed transaction may still consume gas.

### Transaction Not Found

#### Problem

The explorer cannot find the transaction hash.

#### Solution

* confirm that the hash is correct;
* wait briefly for explorer indexing;
* check the connected chain ID;
* query the transaction through the RPC.

### Contract Call Reverted

#### Problem

A smart-contract function rejected the transaction.

#### Possible causes

* invalid input;
* insufficient permission;
* contract requirement not met;
* insufficient token balance;
* paused contract;
* incorrect network or contract address.

Review the contract error and transaction data.

### Incorrect Contract Address

#### Problem

The application is using a contract address from another network.

#### Solution

Confirm that the contract was deployed specifically to Qantera Public Testnet.

Ethereum, BNB Chain, and Qantera may use different contract addresses for the same application.

### QTER Balance Is Not Visible

#### Problem

The wallet shows a zero balance or does not display QTER.

#### Solution

QTER is the native token, so no token contract needs to be imported.

Try:

* refreshing the wallet;
* switching networks and returning;
* changing to the backup RPC;
* checking the address on the explorer.

### Faucet Unavailable

#### Problem

The faucet cannot be accessed.

#### Solution

The official faucet URL has not yet been announced.

Do not use unofficial faucet links or buy testnet QTER from third parties.

### Contract Verification Failed

#### Possible causes

* incorrect compiler version;
* different optimizer settings;
* missing constructor arguments;
* incomplete source files;
* bytecode mismatch.

Use the same build settings that were used during deployment.
