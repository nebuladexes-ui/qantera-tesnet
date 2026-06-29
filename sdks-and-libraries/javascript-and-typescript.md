# JavaScript and TypeScript

Developers can connect to Qantera using ethers or viem.

### Option 1: ethers

Install [ethers](https://docs.ethers.org/):

```
npm install ethers
```

Connect to Qantera:

```
import {
  JsonRpcProvider,
  formatEther
} from "ethers";

const provider = new JsonRpcProvider(
  "https://rpc1.qantera.network"
);

const network = await provider.getNetwork();
const blockNumber = await provider.getBlockNumber();

console.log("Chain ID:", network.chainId.toString());
console.log("Latest block:", blockNumber);
```

Expected chain ID:

```
974621
```

#### Check a balance

```
const address = "0xYOUR_WALLET_ADDRESS";

const balance = await provider.getBalance(address);

console.log("Balance:", formatEther(balance), "QTER");
```

#### Read a transaction receipt

```
const receipt = await provider.getTransactionReceipt(
  "0xYOUR_TRANSACTION_HASH"
);

console.log(receipt);
```

### Option 2: viem

Install [viem](https://viem.sh/):

```
npm install viem
```

Define the Qantera chain:

```
import {
  createPublicClient,
  defineChain,
  formatEther,
  http
} from "viem";

const qantera = defineChain({
  id: 974621,
  name: "Qantera Public Testnet",
  nativeCurrency: {
    name: "Qantera",
    symbol: "QTER",
    decimals: 18
  },
  rpcUrls: {
    default: {
      http: [
        "https://rpc1.qantera.network",
        "https://rpc2.qantera.network"
      ]
    }
  },
  blockExplorers: {
    default: {
      name: "Qantera Explorer",
      url: "https://explorer.qantera.network"
    }
  },
  testnet: true
});

const client = createPublicClient({
  chain: qantera,
  transport: http()
});

const blockNumber = await client.getBlockNumber();

console.log("Latest block:", blockNumber);
```

#### Check a balance with viem

```
const balance = await client.getBalance({
  address: "0xYOUR_WALLET_ADDRESS"
});

console.log(formatEther(balance), "QTER");
```

### Which library should you use?

Use **ethers** for a simple and widely used interface.

Use **viem** when you want strong TypeScript typing and explicit chain configuration.
