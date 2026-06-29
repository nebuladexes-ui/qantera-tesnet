# Glossary

This glossary explains the main terms used throughout the Qantera documentation.

### Address

A public identifier used to receive QTER and interact with smart contracts.

An EVM address normally begins with `0x`.

### Block

A group of transactions added to the blockchain.

Each block has a unique block number and block hash.

### Block Explorer

A website used to view blocks, transactions, wallet addresses, and smart contracts.

[Open Qantera Explorer](https://explorer.qantera.network/)

### Chain ID

A unique number that identifies an EVM network.

Qantera Public Testnet uses:

```
974621
```

Hexadecimal format:

```
0xEDF1D
```

### Contract Address

The blockchain address of a deployed smart contract.

A contract address is different from the address used on another network.

### EVM

The Ethereum Virtual Machine is the execution environment used by Solidity smart contracts.

Qantera is EVM-compatible.

### Faucet

A tool that distributes testnet tokens.

The Qantera faucet will distribute:

```
0.1 QTER per successful claim
```

### Finality

The point at which a block is considered permanently accepted by the network.

Qantera's finality model will be documented when the consensus specification is published.

### Gas

The fee required to process transactions and smart-contract operations.

Gas fees on Qantera are paid in QTER.

### JSON-RPC

A communication interface used by wallets, applications, and developer tools to connect to a blockchain node.

### Native Token

The main token used by a blockchain network.

Qantera's native token is:

```
QTER
```

### Node

Software that connects to the network, receives blockchain data, and may provide RPC services.

### Post-Quantum Cryptography

Cryptographic systems designed to resist known attacks from both classical and quantum computers.

### Private Key

A secret value used to control a blockchain account.

Never share your private key.

### Public Testnet

A public blockchain environment used for testing before mainnet.

Testnet tokens have no monetary value.

### RPC Endpoint

A URL used by wallets and applications to communicate with the network.

Qantera RPC endpoints:

* [Primary RPC](https://rpc1.qantera.network)
* [Backup RPC](https://rpc2.qantera.network)

### Smart Contract

A program deployed and executed on the blockchain.

### Transaction Hash

A unique identifier created when a transaction is submitted.

It can be searched on the [Qantera Explorer](https://explorer.qantera.network/).

### Validator

A network participant that helps validate blocks and participate in consensus.

Public Qantera validator participation is not yet available.

### WebSocket

A persistent connection used for real-time blockchain updates.

Qantera WebSocket endpoint:

```
wss://rpc1.qantera.network
```
