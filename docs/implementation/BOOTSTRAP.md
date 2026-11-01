AETHER Implementation Bootstrap
===============================

Actual Current State
--------------------

* **No root `Cargo.toml` currently.** The repository does not yet contain a top-level `Cargo.toml` file.
* **No compiled node, runtime, Wasm, or genesis/devnet.** Nothing has been built yet.
* **Frontier not integrated.** Frontier EVM compatibility has not been implemented.
* **NPoS / BABE / GRANDPA not implemented.** These consensus mechanisms are not implemented at this stage.

Upstream SDK Baseline
---------------------

* Intended upstream SDK baseline: Polkadot SDK `stable2603-8` tree, commit `ed30dfeb9818b48373a7aa69f6c6195677f9bad3`.
* The SDK monorepo template at `templates/solochain` is **not** standalone and must not be copied alone.

Implementation Sequence
-----------------------

1. Independent workspace (root `Cargo.toml` and `Cargo.lock`).
2. Pinned compatible SDK (`stable2603-8` / `ed30dfeb9818b48373a7aa69f6c6195677f9bad3`) + Frontier and `Cargo.lock`.
3. Native AETH issuance cap.
4. NPoS / BABE / GRANDPA.
5. Frontier EVM / RPC.
6. AI useful-work isolated from consensus.
7. Tests.
8. CI.

Note: No root `Cargo.toml` exists yet, so no builds can proceed until the workspace is established.
