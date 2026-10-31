# AETHER Protocol Baseline

## Identity

| Parameter | Baseline |
|---|---|
| Network name | AETHER |
| Native currency | AETH |
| Network type | Sovereign standalone Layer 1 |
| Consensus | Proof of Stake |
| Smart contracts | EVM-compatible execution via Parity Frontier |
| Maximum supply | 21,000,000 AETH |
| Fundraising | No ICO, no presale, no external token sale |

## Consensus boundary

PoS is the only mechanism responsible for selecting/authorizing block production and finality. AI useful-work is a separate application/reward subsystem. A useful-work result cannot make an invalid block valid, bypass validator authorization, or override finality.

## Monetary invariant

The protocol target is a hard maximum of 21,000,000 AETH. Runtime implementation must define smallest units, genesis issuance, staking rewards, transaction fees, burns (if any), and all mint/burn permissions. Tests must prove that total issuance never exceeds the maximum under every permitted dispatch path.

The supply cap alone does not define the distribution. Genesis allocations and ongoing issuance/reward policy remain unapproved.

## EVM compatibility

The EVM integration must specify and test:
- unique EVM chain ID;
- account/address mapping and signature behavior;
- gas schedule and fee payment in AETH (or an explicitly approved alternative);
- Ethereum JSON-RPC methods supported;
- precompiles and their access controls;
- transaction receipt/log indexing and reorg behavior;
- runtime upgrade compatibility and state migration.

## Network launch requirements

A real sovereign network requires a chain specification, deterministic genesis, bootnodes, peer discovery, node software, consensus configuration, validator onboarding, telemetry/monitoring, backup/recovery procedures, and independently operated validators.
