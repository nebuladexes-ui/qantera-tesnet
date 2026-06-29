# Overview

Qantera is EVM-compatible, so developers can connect using common Ethereum libraries.

### Available options

| Language                  | Recommended Library                                                                   |
| ------------------------- | ------------------------------------------------------------------------------------- |
| JavaScript and TypeScript | [ethers](https://docs.ethers.org/) or [viem](https://viem.sh/)                        |
| Python                    | [Web3.py](https://web3py.readthedocs.io/)                                             |
| Go                        | [go-ethereum ethclient](https://pkg.go.dev/github.com/ethereum/go-ethereum/ethclient) |
| Java                      | [Web3j](https://docs.web3j.io/)                                                       |

### Network configuration

```
Network: Qantera Public Testnet
Chain ID: 974621
RPC: https://rpc1.qantera.network
Backup RPC: https://rpc2.qantera.network
WebSocket: wss://rpc1.qantera.network
Native Token: QTER
Explorer: https://explorer.qantera.network
```

### What you can do

These libraries can be used to:

* read blocks and balances;
* inspect transactions;
* call smart contracts;
* estimate gas;
* sign and send transactions;
* listen for contract events.

Standard EVM libraries currently provide the simplest way to build on Qantera.
