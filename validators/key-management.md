# Key management

Validator keys authorize important actions on the network.

A compromised validator key can affect both the operator and the network.

### Key security principles

Validator operators should:

* generate keys on a secure machine;
* store keys in an encrypted location;
* restrict file permissions;
* keep backups offline;
* avoid sending keys through chat or email;
* separate validator keys from personal wallets;
* limit server access;
* document recovery procedures.

### Avoid duplicate signing

The same validator key should not run on multiple active validator instances unless the protocol explicitly supports it.

Running duplicate instances may create conflicting signatures and could result in penalties when slashing is enabled.

### Backups

A secure backup process should include:

* encrypted backup files;
* more than one secure storage location;
* restricted access;
* tested recovery procedures;
* clear key-rotation instructions.

### Future documentation

The following information will be added when validator software is released:

* validator key type;
* key-generation command;
* keystore format;
* password handling;
* backup process;
* key rotation;
* recovery process;
* hardware-security support.

> Never upload validator keys to GitHub, cloud notes, screenshots, or support tickets.
