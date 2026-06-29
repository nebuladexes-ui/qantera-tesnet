# Smart-contract security

Smart contracts execute according to their code.

A contract can contain vulnerabilities even when the underlying network is secure.

### Common risks

Developers should review contracts for:

* incorrect access control;
* reentrancy;
* calculation errors;
* unsafe token approvals;
* incorrect contract addresses;
* upgradeability risks;
* oracle manipulation;
* unsafe external calls;
* missing input validation.

### Recommended process

Before deploying:

1. Review the contract logic.
2. Write unit tests.
3. Test failure cases.
4. Check user permissions.
5. Review external dependencies.
6. Deploy to Qantera Public Testnet.
7. Test every important function.
8. Complete an independent audit before production use.

### Verify before interacting

Before using a contract, check:

* contract address;
* deployment network;
* source-code verification;
* owner or administrator permissions;
* token approvals;
* transaction details.

Use the [Qantera Explorer](https://explorer.qantera.network/) to inspect deployed contracts and transactions.

### Important

EVM compatibility allows developers to use familiar tools, but it does not guarantee that every deployed contract is safe.
