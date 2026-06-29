# Overview

Qantera provides an EVM-compatible JSON-RPC interface for wallets, applications, scripts, and developer tools.

### RPC endpoints

| Endpoint         | URL                                                           |
| ---------------- | ------------------------------------------------------------- |
| Primary HTTP RPC | [https://rpc1.qantera.network](https://rpc1.qantera.network/) |
| Backup HTTP RPC  | [https://rpc2.qantera.network](https://rpc2.qantera.network/) |
| WebSocket RPC    | `wss://rpc1.qantera.network`                                  |

Use HTTP RPC for standard requests.

Use WebSocket RPC for real-time subscriptions when supported.

### Send an RPC request

A JSON-RPC request contains:

* JSON-RPC version;
* method name;
* parameters;
* request ID.

Example:

```bash
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_blockNumber",
    "params": [],
    "id": 1
  }'
```

Example response:

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x..."
}
```

Many numeric RPC values are returned in hexadecimal format.

### Verify the network

Use `eth_chainId` to confirm that the RPC is connected to Qantera Public Testnet.

```bash
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_chainId",
    "params": [],
    "id": 1
  }'
```

Expected result:

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0xedf1d"
}
```

This represents chain ID `974621`.

### Common RPC methods

| Method                      | Purpose                               |
| --------------------------- | ------------------------------------- |
| `eth_chainId`               | Return the connected chain ID         |
| `eth_blockNumber`           | Return the latest block number        |
| `eth_getBalance`            | Return the QTER balance of an address |
| `eth_getBlockByNumber`      | Return block information              |
| `eth_getTransactionByHash`  | Return transaction information        |
| `eth_getTransactionReceipt` | Return transaction execution result   |
| `eth_call`                  | Read data from a smart contract       |
| `eth_estimateGas`           | Estimate gas for a transaction        |
| `eth_sendRawTransaction`    | Submit a signed transaction           |
| `eth_getLogs`               | Return matching contract events       |

For the complete standard method reference, see the [Ethereum JSON-RPC documentation](https://ethereum.org/developers/docs/apis/json-rpc/).

### Check an address balance

```bash
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_getBalance",
    "params": [
      "0xYOUR_WALLET_ADDRESS",
      "latest"
    ],
    "id": 1
  }'
```

The balance is returned in wei as a hexadecimal value.

QTER uses `18` decimals.

### Check a transaction receipt

```bash
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_getTransactionReceipt",
    "params": [
      "0xYOUR_TRANSACTION_HASH"
    ],
    "id": 1
  }'
```

Receipt status:

```
0x1 = Success
0x0 = Failed
```

You can also inspect transactions through the [Qantera Explorer](https://explorer.qantera.network/).

### RPC safety

* Never send a seed phrase or private key to an RPC endpoint.
* Sign transactions locally in a wallet or application.
* Confirm chain ID `974621` before signing.
* Use the backup RPC when the primary endpoint is unavailable.
* Avoid sending the same signed transaction repeatedly without checking its status.

***

## Qantera-Specific Methods

Qantera currently supports developers through its EVM-compatible JSON-RPC interface.

No public Qantera-specific RPC methods have been documented at this stage.

Developers should use standard methods such as:

```
eth_chainId
eth_blockNumber
eth_getBalance
eth_call
eth_estimateGas
eth_sendRawTransaction
eth_getTransactionReceipt
eth_getLogs
```

Qantera-specific methods may be introduced later for network features that cannot be accessed through standard EVM RPC methods.

When available, this page will document:

* method name;
* parameters;
* response format;
* code examples;
* supported node version;
* rate limits;
* possible errors.

> Do not use undocumented custom RPC methods in production applications.
