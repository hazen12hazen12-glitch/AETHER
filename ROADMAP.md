# AETHER Delivery Roadmap

## Phase 0 — Protocol foundation
- [x] Record sovereign L1 identity and baseline constraints.
- [x] Confirm PoS is consensus and AI useful-work is separate.
- [x] Record fixed maximum supply target and unresolved monetary decisions.
- [ ] Approve token denomination and genesis allocation policy.

## Phase 1 — Reproducible technical base
- [ ] Select official Polkadot SDK Solochain template.
- [ ] Pin exact SDK revision.
- [ ] Select compatible Frontier revision and pin exact SHA.
- [ ] Import/adapt node and runtime crates with upstream notices.
- [ ] Configure CI toolchain and reproducible build.

## Phase 2 — Native asset and consensus
- [ ] Implement AETH genesis configuration.
- [ ] Implement issuance cap invariant and tests.
- [ ] Configure PoS validator/staking/session lifecycle.
- [ ] Configure fees, weights, block limits and telemetry.
- [ ] Test validator rotation, restart, downtime and equivocation handling.

## Phase 3 — EVM
- [ ] Integrate Frontier.
- [ ] Choose and reserve unique EVM chain ID.
- [ ] Configure gas and fee payment.
- [ ] Test Ethereum RPC, transfers, contract deployment, logs and reorgs.

## Phase 4 — AI useful-work
- [ ] Specify task classes and off-chain compute interface.
- [ ] Implement bounded submissions and replay protection.
- [ ] Implement deterministic verification/challenge workflow.
- [ ] Add reward accounting under the supply cap.
- [ ] Threat-model sybil, collusion, fabricated work and denial-of-service.

## Phase 5 — Private devnet and public testnet
- [ ] Generate deterministic chain spec/genesis.
- [ ] Operate multiple independent validators.
- [ ] Test upgrades, backups, restore and network partitions.
- [ ] Publish faucet/explorer/RPC policies and incident response.
- [ ] Complete external security review before public testnet.

## Phase 6 — Mainnet readiness
- [ ] Independent audit findings resolved.
- [ ] Validator diversity and operational runbooks demonstrated.
- [ ] Governance and emergency procedures approved.
- [ ] Genesis ceremony independently verified.
- [ ] Mainnet launch decision explicitly approved.
