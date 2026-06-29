# Java

Java applications can connect to Qantera using [Web3j](https://docs.web3j.io/).

### Connect to Qantera

Add Web3j to your Gradle or Maven project using the current version shown in the official Web3j documentation.

```
import java.math.BigInteger;

import org.web3j.protocol.Web3j;
import org.web3j.protocol.http.HttpService;

public class QanteraClient {
    public static void main(String[] args)
            throws Exception {

        Web3j web3 = Web3j.build(
            new HttpService(
                "https://rpc1.qantera.network"
            )
        );

        BigInteger chainId = web3
            .ethChainId()
            .send()
            .getChainId();

        BigInteger blockNumber = web3
            .ethBlockNumber()
            .send()
            .getBlockNumber();

        System.out.println(
            "Chain ID: " + chainId
        );

        System.out.println(
            "Latest block: " + blockNumber
        );

        web3.shutdown();
    }
}
```

Expected chain ID:

```
974621
```

### Check a balance

```
import java.math.BigDecimal;
import java.math.BigInteger;

import org.web3j.protocol.Web3j;
import org.web3j.protocol.core.DefaultBlockParameterName;
import org.web3j.protocol.http.HttpService;
import org.web3j.utils.Convert;

public class QanteraBalance {
    public static void main(String[] args)
            throws Exception {

        Web3j web3 = Web3j.build(
            new HttpService(
                "https://rpc1.qantera.network"
            )
        );

        BigInteger balanceWei = web3
            .ethGetBalance(
                "0xYOUR_WALLET_ADDRESS",
                DefaultBlockParameterName.LATEST
            )
            .send()
            .getBalance();

        BigDecimal balanceQter = Convert.fromWei(
            balanceWei.toString(),
            Convert.Unit.ETHER
        );

        System.out.println(
            "Balance: " + balanceQter + " QTER"
        );

        web3.shutdown();
    }
}
```

Use the backup endpoint when required:

```
https://rpc2.qantera.network
```

Never store a private key directly inside Java source code.
