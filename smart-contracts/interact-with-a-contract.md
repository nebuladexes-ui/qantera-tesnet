# Interact with a contract

After deployment, you can read data or send transactions to the contract.

### Read a contract

Read operations do not change blockchain state and normally do not require gas.

Example with ethers:

```
import { JsonRpcProvider, Contract } from "ethers";

const provider = new JsonRpcProvider(
  "https://rpc1.qantera.network"
);

const contract = new Contract(
  "YOUR_CONTRACT_ADDRESS",
  [
    "function count() view returns (uint256)"
  ],
  provider
);

const value = await contract.count();

console.log(value.toString());
```

### Write to a contract

Write operations require:

* a connected wallet;
* a signature;
* QTER for gas.

Example:

```
const writableContract = contract.connect(wallet);

const transaction = await writableContract.increment();

await transaction.wait();
```

### Check the result

Open the contract or transaction on the [Qantera Explorer](https://explorer.qantera.network/).

Confirm:

* transaction status;
* contract address;
* called function;
* gas used;
* emitted events.
