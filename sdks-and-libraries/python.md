# Python

Use [Web3.py](https://web3py.readthedocs.io/) to connect Python applications to Qantera.

### Install Web3.py

```
python -m pip install web3
```

### Connect to Qantera

```
from web3 import Web3

RPC_URL = "https://rpc1.qantera.network"

w3 = Web3(Web3.HTTPProvider(RPC_URL))

if not w3.is_connected():
    raise ConnectionError("Unable to connect to Qantera RPC")

print("Chain ID:", w3.eth.chain_id)
print("Latest block:", w3.eth.block_number)
```

Expected chain ID:

```
974621
```

### Check a QTER balance

```
address = Web3.to_checksum_address(
    "0xYOUR_WALLET_ADDRESS"
)

balance_wei = w3.eth.get_balance(address)
balance_qter = w3.from_wei(balance_wei, "ether")

print("Balance:", balance_qter, "QTER")
```

### Read a transaction receipt

```
transaction_hash = "0xYOUR_TRANSACTION_HASH"

receipt = w3.eth.get_transaction_receipt(
    transaction_hash
)

print("Status:", receipt["status"])
print("Block:", receipt["blockNumber"])
print("Gas used:", receipt["gasUsed"])
```

Receipt status:

```
1 = Success
0 = Failed
```

### Backup RPC

If the primary endpoint is unavailable, use:

```
RPC_URL = "https://rpc2.qantera.network"
```

Never place a real private key directly inside source code.
