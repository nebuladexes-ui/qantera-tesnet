# Quickstart

## Quickstart

Follow these steps to connect to Qantera Public Testnet and begin testing.

### 1. Install a wallet

Use an EVM-compatible wallet such as:

* MetaMask;
* OKX Wallet;
* Rabby.

For security, use a separate wallet created only for testnet activities.

### 2. Add Qantera Public Testnet

For the latest RPC endpoints, chain ID, native token, and explorer information, see [**Network Details**.](network-details.md)

### 3. Request QTER

The Qantera faucet will distribute:

```
0.1 QTER per successful claim
```

The faucet URL will be added to this documentation when it becomes available.

QTER is used to pay gas fees and test applications on the network.

### 4. Send a test transaction

After receiving QTER:

1. Open your wallet.
2. Select **Send**.
3. Enter another testnet address.
4. Enter a small amount of QTER.
5. Confirm the transaction.
6. Copy the transaction hash.

### 5. Check the transaction

Open the Qantera Explorer:

```
https://explorer.qantera.network
```

Paste the transaction hash into the search bar to view:

* transaction status;
* sender and receiver;
* transferred amount;
* gas fee;
* block number.

### Troubleshooting

#### The wallet cannot connect

Switch the RPC URL to:

```
https://rpc2.qantera.network
```

#### The network information is incorrect

Confirm that the chain ID is:

```
974621
```

#### The wallet has no QTER

The public faucet is not available yet. The official faucet link will be published in this documentation.

### Next steps

Continue with:

* Set Up Your Environment
* Transactions
* Smart Contracts
* JSON-RPC API
