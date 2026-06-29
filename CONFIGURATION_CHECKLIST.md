# Publication Configuration Checklist

This file separates confirmed public-testnet configuration from information that still requires an engineering or product announcement.

## Confirmed

- [x] Project name: Qantera
- [x] Network stage: Public Testnet
- [x] Network name: Qantera Public Testnet
- [x] EVM-compatible execution
- [x] Chain ID: `974621`
- [x] Chain ID hex: `0xEDF1D`
- [x] Native token name: Qantera
- [x] Native token symbol: `QTER`
- [x] Native token decimals: `18`
- [x] Primary HTTP RPC: `https://rpc1.qantera.network`
- [x] Backup HTTP RPC: `https://rpc2.qantera.network`
- [x] WebSocket RPC: `wss://rpc1.qantera.network`
- [x] Explorer: `https://explorer.qantera.network`
- [x] Faucet claim amount: `0.1 QTER`

## Product information still pending

- [ ] Faucet URL
- [ ] Faucet cooldown and daily limits
- [ ] Official docs domain
- [ ] GitHub organization and source repositories
- [ ] X, Telegram, Discord, support, and security contacts
- [ ] Dedicated network status page
- [ ] Social Tasks point table
- [ ] Yap Task scoring rules
- [ ] Genesis NFT contract, supply, dates, and eligibility
- [ ] Leaderboard season rules

## Protocol information still pending

- [ ] Consensus mechanism and client names
- [ ] Target and observed block time
- [ ] Finality model and expected finality time
- [ ] Gas model and supported transaction types
- [ ] Supported EVM revision
- [ ] Mempool behavior and throughput targets
- [ ] Node release, genesis file, bootnodes, ports, and hardware requirements
- [ ] Validator eligibility, staking, rewards, slashing, and exit rules

## Post-quantum specification still pending

Publish the exact:

- signature algorithm and parameter set;
- classical or hybrid signature model;
- signed message and transaction envelope;
- wallet or signer requirements;
- mempool, validator, or execution-layer verification rules;
- key and signature sizes;
- gas or resource cost;
- replay protection and domain separation;
- account migration and crypto-agility process;
- test vectors, audit reports, and known limitations.

Use **quantum-resistant** or **post-quantum ready**. Do not publish absolute claims such as “quantum-proof,” “unbreakable,” or “impossible to hack.”
