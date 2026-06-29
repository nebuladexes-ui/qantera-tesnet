# Verify a contract

## Verify a Contract

Contract verification connects deployed bytecode with its Solidity source code.

This helps users understand and review the contract.

### Information required

Prepare:

* contract address;
* Solidity source code;
* compiler version;
* optimizer settings;
* constructor arguments;
* imported contracts;
* linked libraries.

### Verification process

When contract verification is enabled on the Qantera Explorer:

1. Open the contract address.
2. Select **Verify and Publish**.
3. Choose the compiler version.
4. Add the source code.
5. Enter the optimizer settings.
6. Add constructor arguments if required.
7. Submit the verification request.

### Important

The submitted settings must match the deployment exactly.

Verification may fail when:

* the compiler version is incorrect;
* optimizer settings are different;
* constructor arguments are missing;
* imported source files are incomplete;
* the deployed bytecode does not match.

### Current status

The exact Qantera verification workflow and API will be updated when contract verification is officially enabled.

Use the [Qantera Explorer](https://explorer.qantera.network/) to check the current available options.
