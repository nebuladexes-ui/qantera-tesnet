# Monitoring

Monitoring helps operators detect synchronization problems and infrastructure failures.

### Important metrics

Node operators should monitor:

* service availability;
* latest block number;
* synchronization status;
* peer count;
* CPU usage;
* memory usage;
* disk usage;
* disk growth;
* network traffic;
* RPC latency;
* RPC error rate.

### Check the latest block

Use `eth_blockNumber`:

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

Compare the result with the latest block shown on the [Qantera Explorer](https://explorer.qantera.network/).

### Check synchronization status

```
curl -X POST "https://rpc1.qantera.network" \
  -H "Content-Type: application/json" \
  --data '{
    "jsonrpc": "2.0",
    "method": "eth_syncing",
    "params": [],
    "id": 1
  }'
```

A fully synchronized node commonly returns:

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": false
}
```

### Recommended alerts

Operators should create alerts for:

* node process stopped;
* block height not increasing;
* node falling behind the network;
* low peer count;
* disk almost full;
* high memory usage;
* repeated RPC errors.

The official Qantera metrics and monitoring integrations will be documented with the node release.
