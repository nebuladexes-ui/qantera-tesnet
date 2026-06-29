# Network details

Use the following information to connect your wallet or application to the Qantera Public Testnet.

### Official network configuration

| Field          | Value                              |
| -------------- | ---------------------------------- |
| Network Name   | Qantera Public Testnet             |
| Chain ID       | `974621`                           |
| Chain ID — Hex | `0xEDF1D`                          |
| Native Token   | Qantera                            |
| Symbol         | `QTER`                             |
| Decimals       | `18`                               |
| Primary RPC    | `https://rpc1.qantera.network`     |
| Backup RPC     | `https://rpc2.qantera.network`     |
| WebSocket RPC  | `wss://rpc1.qantera.network`       |
| Block Explorer | `https://explorer.qantera.network` |
| Faucet         | Coming soon                        |

### Wallet setup

Enter these values when adding Qantera as a custom network:

```
Network Name: Qantera Public Testnet
RPC URL: https://rpc1.qantera.network
Chain ID: 974621
Currency Symbol: QTER
Block Explorer URL: https://explorer.qantera.network
```

Use the backup RPC if the primary endpoint is unavailable:

```
https://rpc2.qantera.network
```

### Add Qantera from a dApp

Developers can request compatible wallets to add the network automatically:

```javascript
await window.ethereum.request({
  method: "wallet_addEthereumChain",
  params: [
    {
      chainId: "0xEDF1D",
      chainName: "Qantera Public Testnet",
      nativeCurrency: {
        name: "Qantera",
        symbol: "QTER",
        decimals: 18
      },
      rpcUrls: [
        "https://rpc1.qantera.network",
        "https://rpc2.qantera.network"
      ],
      blockExplorerUrls: [
        "https://explorer.qantera.network"
      ]
    }
  ]
});
```

Always confirm that the connected chain ID is `974621` before signing a transaction.
