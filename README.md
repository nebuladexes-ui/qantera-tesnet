# Qantera Public Testnet Docs

Qantera is an EVM-compatible Layer 1 public testnet designed to explore quantum-resistant transaction security, cryptographic agility, open infrastructure, and a familiar Web3 developer experience.

This documentation is written for four audiences:

* **Users** connecting a wallet, claiming QTER, and sending test transactions.
* **Developers** deploying Solidity contracts and integrating Qantera through JSON-RPC.
* **Infrastructure operators** preparing to run nodes or validators when public binaries and participation rules are released.
* **Security researchers and contributors** evaluating the network model, testing applications, and participating in community programs.

> **Public testnet notice:** QTER is a test token used for gas and application testing. It has no monetary value. Testnet state, configuration, and features may change during development.

## Official network configuration

| Parameter              | Value                                 |
| ---------------------- | ------------------------------------- |
| Network name           | Qantera Public Testnet                |
| Network type           | EVM-compatible Layer 1 public testnet |
| Chain ID               | `974621`                              |
| Chain ID — hexadecimal | `0xEDF1D`                             |
| Native currency        | Qantera                               |
| Symbol                 | `QTER`                                |
| Decimals               | `18`                                  |
| Primary HTTP RPC       | `https://rpc1.qantera.network`        |
| Backup HTTP RPC        | `https://rpc2.qantera.network`        |
| WebSocket RPC          | `wss://rpc1.qantera.network`          |
| Block explorer         | `https://explorer.qantera.network`    |
| Faucet                 | Coming soon                           |
| Faucet amount          | `0.1 QTER` per successful claim       |
| Faucet cooldown        | Not yet announced                     |

### Build on Qantera

1. Set up a development environment.
2. Connect Hardhat, Foundry, Remix, ethers, viem, or Web3.py.
3. Compile and deploy a Solidity contract.
4. Verify the transaction and contract address in the explorer.
5. Use the JSON-RPC reference when integrating infrastructure or applications.

### Understand the security model

Read the pages on post-quantum security, cryptographic agility, EVM compatibility, and current limitations. Qantera documentation intentionally distinguishes confirmed network configuration from protocol details that have not yet been published.

## Documentation status

The following information is confirmed in this release:

* public testnet stage;
* chain ID;
* native currency;
* token decimals;
* HTTP and WebSocket endpoints;
* block explorer;
* faucet claim amount.

The following information remains unpublished and is not inferred:

* consensus mechanism;
* target block time and finality guarantees;
* public node client and validator participation rules;
* exact post-quantum algorithm, parameter set, transaction envelope, and verification path;
* audit reports and test vectors.

These pages will be updated as the corresponding specifications are released.
