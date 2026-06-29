# Security model

Qantera security is built across multiple layers.

No single algorithm can protect the entire network. Transaction security, wallet safety, smart-contract security, validators, and public infrastructure must work together.

### Account security

Users control their accounts through wallet keys.

A transaction is valid only when it is properly authorized by the account owner.

Users are responsible for:

* protecting their seed phrase and private key;
* checking the connected network;
* reviewing transaction details;
* avoiding malicious websites and wallet extensions;
* using a separate wallet for testnet activities.

Post-quantum security cannot protect an account if the private key or device is already compromised.

### Network security

Nodes and validators are responsible for processing transactions and maintaining the canonical blockchain state.

The final consensus mechanism, validator model, and finality rules will be documented when the protocol specification is published.

### Smart-contract security

Smart contracts execute exactly as written.

Application developers must protect their contracts against risks such as:

* incorrect access control;
* reentrancy;
* calculation errors;
* unsafe upgrades;
* malicious external dependencies;
* incorrect token or contract addresses.

EVM compatibility does not automatically make a smart contract secure.

### Infrastructure security

Wallets and applications connect to Qantera through RPC endpoints and the block explorer.

Official infrastructure includes:

```
Primary RPC: https://rpc1.qantera.network
Backup RPC: https://rpc2.qantera.network
Explorer: https://explorer.qantera.network
```

Users should verify the chain ID before signing:

```
974621
```

### Shared responsibility

Qantera provides the network and security infrastructure, but users and developers also have responsibilities.

#### Qantera is responsible for

* network protocol security;
* node and validator software;
* RPC and explorer infrastructure;
* protocol upgrades;
* publishing security information.

#### Users and developers are responsible for

* wallet security;
* private-key protection;
* smart-contract quality;
* verifying network information;
* reviewing transactions before signing.

### Public Testnet notice

Qantera Public Testnet is an experimental environment.

The network may be updated, restarted, or reset during development. Testnet QTER has no monetary value and should not be treated as a production asset.
