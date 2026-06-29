# Deploy a contract

his example deploys a simple counter contract.

### Example contract

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract QanteraCounter {
    uint256 public count;

    event CountUpdated(uint256 newCount);

    function increment() external {
        count += 1;
        emit CountUpdated(count);
    }
}
```

### Before deployment

Make sure that:

* the contract compiles successfully;
* tests pass;
* the deployer wallet contains QTER;
* the wallet is connected to chain ID `974621`;
* the contract does not contain unnecessary permissions.

### Deployment process

1. Compile the contract.
2. Connect the deployment tool to Qantera.
3. Deploy using a test wallet.
4. Approve the transaction.
5. Wait for confirmation.
6. Save the contract address.
7. Open the deployment transaction in the explorer.

### Information to save

Keep a record of:

* contract address;
* deployment transaction hash;
* deployer address;
* compiler version;
* constructor arguments;
* source-code version.
