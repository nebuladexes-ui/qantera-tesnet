---
hidden: true
---

# Network status

The Network Status page will provide updates about Qantera infrastructure.

### Services monitored

The status page may include:

* Primary RPC;
* Backup RPC;
* WebSocket RPC;
* Block Explorer;
* Faucet;
* block production;
* contract verification;
* community applications.

### Current checks

Until a dedicated status page is available, users can check:

* [Qantera Explorer](https://explorer.qantera.network/)
* [Primary RPC](https://rpc1.qantera.network)
* [Backup RPC](https://rpc2.qantera.network)

### RPC check

Use the following request to check whether the network is responding:

```
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_blockNumber",
    "params": [],
    "id": 1
  }'
```

A successful response returns the latest block number.

### Incident updates

When a network issue occurs, Qantera will publish:

* affected service;
* current status;
* start time;
* user impact;
* resolution update.
