# Why post-quantum security matters

Blockchains use digital signatures to confirm that a transaction was authorized by the owner of an account.

Most existing blockchain networks were designed using classical public-key cryptography. In the future, sufficiently powerful quantum computers may be able to weaken some of these cryptographic systems.

Qantera is being developed with this long-term risk in mind.

### The challenge

Blockchain networks are designed to store assets, contracts, and ownership records for many years.

Even if large-scale quantum computers are not available today, long-lived networks need a clear plan for:

* protecting transaction authorization;
* upgrading cryptographic algorithms;
* migrating accounts when security standards change;
* keeping wallets and applications compatible;
* avoiding disruption to users.

### Qantera's direction

Qantera is designed around two important principles:

#### Quantum-resistant security

The network aims to support transaction-security mechanisms designed to resist known quantum attacks.

The exact post-quantum algorithm, parameter set, and transaction-verification model will be published in the technical specification.

#### Cryptographic agility

Qantera is designed to evolve as cryptographic standards change.

This means the network should be able to introduce stronger algorithms, update security parameters, and phase out outdated cryptographic methods through controlled upgrades.

### What quantum-resistant security does not solve

Quantum-resistant cryptography protects against a specific category of cryptographic risk.

It does not prevent:

* stolen private keys;
* phishing attacks;
* malicious wallet extensions;
* smart-contract vulnerabilities;
* fake websites;
* validator or infrastructure attacks.

Users must still follow normal wallet and Web3 security practices.

### Current status

Qantera Public Testnet focuses on testing the network, wallets, transactions, smart contracts, and infrastructure.

More information about the post-quantum implementation will be added when the technical specification is released.

> Qantera uses the term **quantum-resistant** rather than absolute claims such as “quantum-proof” or “unbreakable.”
