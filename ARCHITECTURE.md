# AETHER Technical Architecture

## Layer 1 components

1. **Node/client:** networking, transaction pool, block import, RPC, database, telemetry and consensus service.
2. **Runtime:** deterministic state transition compiled to Wasm.
3. **FRAME pallets:** system, balances, timestamp, staking/session/consensus integration, fees, governance (when designed), and custom AETHER pallets.
4. **Frontier:** EVM execution and Ethereum-compatible RPC integration.
5. **Useful-work subsystem:** submission, validation, scoring, anti-replay controls, and optional reward accounting.

## Upstream foundation

Use the Polkadot SDK Solochain template as the standalone-chain starting point. Do not use a parachain template unless the project direction explicitly changes. Pin exact SDK and Frontier revisions after compatibility validation; do not mix arbitrary crate versions.

Official references:
- Polkadot SDK runtime customization: https://docs.polkadot.com/parachains/customize-runtime/
- Solochain and template guidance: https://docs.polkadot.com/parachains/customize-runtime/
- Frontier EVM compatibility layer: https://github.com/polkadot-evm/frontier

## Runtime composition (target)

- `frame_system`
- native balances and transaction-payment configuration
- staking/session/authority machinery compatible with the selected SDK release
- timestamp and block-weight/length limits
- Frontier EVM pallet and required fee/RPC components
- `pallet_aether_work` (custom; not yet implemented)
- governance and treasury only after explicit policy decisions

The exact pallet names and APIs must be confirmed against the pinned SDK release before implementation.

## Useful-work design constraints

- deterministic on-chain verification; expensive AI computation remains off-chain;
- signed submissions with nonce/epoch and replay protection;
- bounded payload size and bounded verification weight;
- verifiable evidence or challenge mechanism;
- sybil resistance and anti-collusion policy;
- no privileged path that can alter consensus state;
- rewards must obey the AETH supply invariant;
- dispute, timeout, fraud and slashing rules specified before enabling rewards.

## Build and release gates

1. Pin SDK + Frontier commits and document licenses.
2. Build node and runtime in a reproducible environment.
3. Unit-test custom pallets and runtime invariants.
4. Test chain-spec/genesis determinism.
5. Test EVM transfers, contract deployment, logs, RPC and gas accounting.
6. Run multi-validator private devnet with node restarts and network partitions.
7. Run security review and upgrade/migration rehearsal.
8. Only then plan public testnet.
