# ADR 0001: Sovereign Layer 1 Foundation

- Status: Accepted as project direction
- Date: 2026-10-31

## Context

AETHER is intended to be an independent blockchain with its own native asset. Deploying an ERC-20 contract on an existing chain does not meet this requirement.

## Decision

Use Polkadot SDK Solochain as the architectural starting point, FRAME for runtime composition, and Parity Frontier for EVM compatibility. Use PoS for consensus. Keep AI useful-work separate from consensus validity/finality.

## Consequences

- The project must operate its own node software, genesis, chain specification, peer network and validator set.
- SDK and Frontier versions must be pinned together after compatibility testing.
- EVM compatibility adds runtime, RPC, fee and security integration work.
- Useful-work cannot be allowed to bypass PoS.
- A supply cap and allocation policy require runtime-level invariants and tests.
