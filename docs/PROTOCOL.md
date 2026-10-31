# AETHER Protocol Baseline

## Identity
- Network: AETHER, sovereign standalone Layer 1
- Native asset: AETH
- Consensus: Proof of Stake (PoS)
- EVM compatibility: Parity Frontier
- Maximum supply target: 21,000,000 AETH
- No ICO, presale, or external token sale

## Consensus boundary
PoS alone authorizes block production and finality. AI useful-work is a separate application and reward subsystem. Useful-work results must never validate an invalid block, bypass validator authorization, or override finality.

## Monetary invariant
The runtime must enforce total issuance at or below 21,000,000 AETH in base units. Denomination, genesis allocations, staking rewards, fee policy, burns, and mint permissions remain undecided and require approval. Tests must cover genesis, rewards, privileged calls, migrations, and edge cases.

## EVM requirements
Specify and test a unique EVM chain ID, address mapping, signature behavior, gas schedule, fee asset, supported Ethereum JSON-RPC methods, precompiles and access controls, receipts/log indexing, reorg behavior, and runtime state migrations.

## Launch requirements
A functioning network requires deterministic chain spec/genesis, node software, bootnodes, peer discovery, validator configuration, monitoring, backup/recovery procedures, and independently operated validators.
