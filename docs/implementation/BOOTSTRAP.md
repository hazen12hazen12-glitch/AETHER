AETHER — Sovereign Layer 1
==========================

**Native asset:** SYNAPSE AI (SAI) · **Maximum supply:** 21,000,000 · **Consensus:** PoS · **Execution:** EVM via Frontier

AETHER is intended to be an independent, sovereign Layer 1 blockchain. It is not an ERC-20 token deployed on another network.

Current repository stage
------------------------

This package establishes the protocol baseline and engineering plan. It does **not** contain a working node/runtime, a compiled Wasm runtime, a genesis state, or a running network. Do not describe AETHER as live, testnet-ready, or production-ready.

Architecture
------------

* Polkadot SDK **Solochain** foundation (standalone chain, not a parachain).
* FRAME runtime and native SYNAPSE AI (SAI) balances.
* Proof of Stake for block production/finality.
* Parity Frontier for EVM execution and Ethereum-compatible RPC.
* A separate useful-work subsystem for AI-related tasks. Useful-work scores must never determine block validity or replace PoS consensus.

Key documents
-------------

* [Protocol baseline](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/docs/PROTOCOL.md)
* [Architecture](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/docs/ARCHITECTURE.md)
* [Tokenomics decisions](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/docs/TOKENOMICS.md)
* [Security model](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/SECURITY.md)
* [Roadmap](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/docs/ROADMAP.md)
* [Architecture decisions](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/docs/adr/0001-sovereign-l1.md)

Decisions still required
------------------------

The initial allocation, validator reward curve, staking inflation/issuance policy, treasury rules, vesting, EVM chain ID, fee model, and useful-work reward policy are not approved. They must not be guessed or hard-coded.

Next engineering step
---------------------

Select and pin a mutually compatible Polkadot SDK Solochain template and Frontier revision, then adapt that upstream baseline. Record exact upstream commit SHAs and license notices before copying or vendoring source.

Security
--------

Never commit seed phrases, private keys, validator keystores, API tokens, or production secrets. See [SECURITY.md](/hazen12hazen12-glitch/AETHER/blob/engineering/solochain-bootstrap/SECURITY.md).
