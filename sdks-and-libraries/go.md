# Go

Go applications can connect to Qantera using the official go-ethereum `ethclient` package.

### Install

```
go get github.com/ethereum/go-ethereum
```

### Connect to Qantera

```
package main

import (
	"context"
	"fmt"
	"log"

	"github.com/ethereum/go-ethereum/ethclient"
)

func main() {
	client, err := ethclient.Dial(
		"https://rpc1.qantera.network",
	)
	if err != nil {
		log.Fatal(err)
	}

	ctx := context.Background()

	chainID, err := client.ChainID(ctx)
	if err != nil {
		log.Fatal(err)
	}

	blockNumber, err := client.BlockNumber(ctx)
	if err != nil {
		log.Fatal(err)
	}

	fmt.Println("Chain ID:", chainID)
	fmt.Println("Latest block:", blockNumber)
}
```

Expected chain ID:

```
974621
```

### Check a balance

```
package main

import (
	"context"
	"fmt"
	"log"
	"math/big"

	"github.com/ethereum/go-ethereum/common"
	"github.com/ethereum/go-ethereum/ethclient"
)

func main() {
	client, err := ethclient.Dial(
		"https://rpc1.qantera.network",
	)
	if err != nil {
		log.Fatal(err)
	}

	address := common.HexToAddress(
		"0xYOUR_WALLET_ADDRESS",
	)

	balance, err := client.BalanceAt(
		context.Background(),
		address,
		nil,
	)
	if err != nil {
		log.Fatal(err)
	}

	qter := new(big.Float).Quo(
		new(big.Float).SetInt(balance),
		big.NewFloat(1e18),
	)

	fmt.Println("Balance:", qter, "QTER")
}
```

For the complete package reference, see [go-ethereum ethclient](https://pkg.go.dev/github.com/ethereum/go-ethereum/ethclient).
