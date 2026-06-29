# Gas and fees

Gas is the fee required to process transactions and smart-contract operations on Qantera.

Gas fees are paid using the native token:

```
QTER
```

### Why gas is required

Gas helps the network measure the resources required to execute a transaction.

Simple operations normally use less gas than complex smart-contract interactions.

Examples:

| Operation                      | Expected gas usage      |
| ------------------------------ | ----------------------- |
| Send QTER                      | Low                     |
| Call a contract                | Medium                  |
| Deploy a contract              | Higher                  |
| Execute complex contract logic | Depends on the contract |

### Gas limit

The gas limit is the maximum amount of gas a transaction can use.

Most wallets and developer tools estimate the gas limit automatically.

Avoid setting a gas limit lower than the estimated requirement because the transaction may fail.

### Gas price

Gas price determines the amount of QTER paid for each unit of gas.

The total transaction fee depends on:

```
Gas Used × Gas Price
```

### Estimate gas through RPC

Applications can use:

```
eth_estimateGas
```

Example request:

```
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_estimateGas",
    "params": [{
      "from": "0xYOUR_ADDRESS",
      "to": "0xRECIPIENT_ADDRESS",
      "value": "0x0"
    }],
    "id": 1
  }'
```

### Tips

* Let your wallet estimate gas automatically.
* Keep enough QTER in your wallet to pay fees.
* Review gas before confirming a transaction.
* A failed transaction may still use gas.
