# Cryptographic agility

Cryptographic agility is the ability of a network to update its security algorithms without rebuilding the entire blockchain.

This is important because cryptographic standards can change over time.

### Why it matters

An algorithm considered secure today may become weaker because of:

* new research;
* improved attacks;
* implementation vulnerabilities;
* new standards;
* more powerful computers;
* changes in network requirements.

A long-lived blockchain should not depend permanently on one cryptographic method.

### Qantera's approach

Qantera is being designed so that cryptographic systems can evolve through controlled network upgrades.

This may allow the network to:

* introduce new signature algorithms;
* update security parameters;
* support migration between algorithms;
* phase out outdated methods;
* coordinate wallet and validator upgrades.

### A controlled upgrade process

A cryptographic upgrade should normally follow these steps:

1. Publish the proposed technical specification.
2. Release an implementation for testing.
3. Activate the feature on the testnet.
4. Test wallet, node, and application compatibility.
5. Complete security reviews.
6. Announce the activation schedule.
7. Provide users with a migration period.
8. Deprecate the older method only after the ecosystem is ready.

### What this means for users

Users should not need to understand every cryptographic detail.

The network and wallet experience should clearly explain:

* whether an account needs to be upgraded;
* whether a new wallet version is required;
* whether the address will change;
* when the upgrade becomes active;
* what happens if no action is taken.

### What this means for developers

Developers should avoid hard-coding assumptions about a single signature system.

Applications should rely on official Qantera wallet, RPC, and SDK interfaces whenever network-specific authentication is required.

### Current status

The final cryptographic upgrade and account-migration model has not yet been published.

This page describes Qantera's design direction. Detailed implementation information will be added after the relevant protocol specification is released.
