# Add Qantera to MetaMask

This guide explains how to add Qantera Public Testnet to MetaMask.

### Install MetaMask

Download MetaMask from the official website:

[Download MetaMask](https://metamask.io/download/)

Create a new wallet or use a separate account for testnet activities.

> Never share your Secret Recovery Phrase or private key.

### Add Qantera manually

1. Open MetaMask.
2. Open the network selector.
3. Select **Add Network**.
4. Choose **Add a Network Manually**.
5. For the latest RPC endpoints, chain ID, native token, and explorer information, see [**Network Details**.](../introducing/network-details.md)
6. Select **Save**.
7. Switch to **Qantera Public Testnet**.

### Verify the connection

Confirm that MetaMask displays:

```
Network: Qantera Public Testnet
Chain ID: 974621
Native Token: QTER
```

You can also open the [Qantera Explorer](https://explorer.qantera.network/) to check network activity.

### Backup RPC

If the primary RPC is unavailable, use:

[https://rpc2.qantera.network](https://rpc2.qantera.network/)

### Troubleshooting

#### The network cannot be added

Check that the chain ID is exactly:

```
974621
```

#### MetaMask cannot connect

Replace the primary RPC with the backup RPC:

```
https://rpc2.qantera.network
```

#### QTER does not appear

QTER is the native token of Qantera Public Testnet. You do not need to import a token contract.

The balance will appear after your wallet receives QTER from the faucet.
