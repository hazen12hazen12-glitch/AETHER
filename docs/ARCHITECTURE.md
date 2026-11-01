AETHER Technical Architecture
=============================

Components
----------

1. Node/client: networking, transaction pool, block import, RPC, database, telemetry, and consensus service.
2. Runtime: deterministic state transition compiled to Wasm.
3. FRAME pallets: system, balances, timestamp, staking/session/consensus integration, fees, and custom AETHER pallets.
4. Frontier: EVM execution and Ethereum-compatible RPC integration.
5. Useful-work subsystem: task submission, validation, scoring, anti-replay controls, and optional reward accounting.

Upstream foundation
-------------------

Use the Polkadot SDK Solochain template as the standalone-chain starting point, not a parachain template. Pin exact SDK and Frontier revisions only after compatibility validation. References: https://docs.polkadot.com/ and https://github.com/polkadot-evm/frontier

Runtime target
--------------

* frame_system and native balances
* transaction payment and block limits
* staking/session/authority machinery compatible with the pinned SDK
* timestamp
* Frontier EVM and required fee/RPC components
* custom pallet_aether_work (not implemented yet)
* governance/treasury only after policy decisions

Confirm exact pallet APIs against the pinned SDK release before coding.

Useful-work constraints
-----------------------

AI computation remains off-chain; on-chain verification must be deterministic, bounded, replay-protected, and challengeable. Define Sybil/collusion resistance, payload and weight limits, dispute/timeout/fraud rules, and reward limits. Useful-work must not alter consensus validity or finality.

Release gates
-------------

Pin dependencies and licenses; build reproducibly; test custom pallets and supply invariants; verify deterministic genesis; test EVM transfers/contracts/logs/RPC/gas; run a multi-validator private devnet; rehearse upgrades and recovery; complete independent security review before public testnet.
