# Send your first transaction

Follow these steps to send QTER on the Qantera Public Testnet.

### Before you start

Make sure that:

* your wallet is connected to Qantera Public Testnet;
* the chain ID is `974621`;
* your wallet has QTER;
* the recipient is a valid testnet address.

The public faucet will provide:

```
1 QTER per successful claim
```

The faucet link will be added when available.

### Send QTER

1. Open your wallet.
2. Switch to **Qantera Public Testnet**.
3. Select **Send**.
4. Enter the recipient address.
5. Enter a small QTER amount.
6. Review the gas fee.
7. Confirm the transaction.
8. Copy the transaction hash.

### Check the transaction

Open the [Qantera Explorer](https://explorer.qantera.network/).

Paste the transaction hash into the search bar.

Check:

* transaction status;
* sender;
* recipient;
* amount;
* gas fee;
* block number.

### Troubleshooting

#### Insufficient balance

Make sure the wallet contains enough QTER for both the transferred amount and gas.

#### Transaction remains pending

Check the network connection and try the backup RPC:

[https://rpc2.qantera.network](https://rpc2.qantera.network)

#### Transaction failed

Review the transaction details and gas settings. Failed smart-contract interactions may also contain a contract error.
