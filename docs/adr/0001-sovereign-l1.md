# ADR 0001: Sovereign Layer 1 Foundation

- Status: Accepted as project direction
- Date: 2026-10-31

## Context
AETHER must be an independent blockchain with its own native asset. An ERC-20 deployed on an existing chain does not satisfy this requirement.

## Decision
Use Polkadot SDK Solochain as the architectural starting point, FRAME for runtime composition, and Parity Frontier for EVM compatibility. PoS is the consensus mechanism. AI useful-work remains separate from consensus validity and finality.

## Consequences
- AETHER must operate its own node software, genesis, chain specification, peer network, and validator set.
- SDK and Frontier revisions must be pinned together after compatibility testing.
- EVM adds runtime, RPC, fee, and security integration work.
- Useful-work cannot bypass PoS.
- Supply cap and allocation policy require runtime invariants and tests.
