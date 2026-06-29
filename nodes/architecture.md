# Architecture

A blockchain node contains several components that work together.

### Main components

#### Peer-to-peer network

The peer-to-peer layer connects the node to other Qantera nodes.

It is responsible for sharing:

* blocks;
* transactions;
* network messages;
* peer information.

#### Execution layer

The execution layer processes EVM transactions and smart contracts.

It updates:

* account balances;
* contract storage;
* transaction receipts;
* events and logs.

#### Blockchain database

The node stores blockchain data such as:

* blocks;
* transactions;
* account state;
* smart-contract data.

The required storage depends on the node type and synchronization mode.

#### RPC service

The RPC service allows wallets, applications, and developer tools to communicate with the node.

Public Qantera endpoints include:

* [https://rpc1.qantera.network](https://rpc1.qantera.network)
* [https://rpc2.qantera.network](https://rpc2.qantera.network)

#### Monitoring service

Node operators should monitor:

* connection status;
* block height;
* peer count;
* synchronization progress;
* CPU usage;
* memory usage;
* disk usage;
* RPC response time.

### Node types

Qantera may support different node configurations.

#### Full node

Stores and verifies the blockchain data required to follow the network.

#### Archive node

Stores historical blockchain state for advanced queries and indexing.

#### RPC node

Provides blockchain access to wallets and applications.

#### Validator node

Participates in network validation and consensus.

The final supported node types will be confirmed when the node software is released.
