# AETHER Implementation Bootstrap

## Actual Current State

* **No root `Cargo.toml` currently.** The repository does not yet contain a top-level `Cargo.toml` file.
* **No built node, runtime, Wasm, or genesis/devnet.** Nothing has been compiled or produced yet.
* **Frontier not integrated.** Frontier EVM compatibility has not been integrated.
* **NPoS / BABE / GRANDPA decisions only.** These consensus mechanisms are the only decisions recorded at this stage.
* **Founder amount documented but address/genesis not configured.** The founder allocation amount (210,000 AETH) is documented in `docs/TOKENOMICS.md`, but the receiving address and genesis configuration are not yet set.

## Upstream Baseline

* Intended upstream baseline: Polkadot SDK `stable2603-8` tree, commit `ed30dfeb9818b48373a7aa69f6c6195677f9bad3`.

## SDK Monorepo Note

* The Polkadot SDK monorepo template at `templates/solochain` is **not** a standalone root. It must not be copied alone.

## Implementation Sequence

1. Establish the root `Cargo.toml` and `Cargo.lock` for the workspace.
2. Scaffold the node, runtime, and pallets directories under the workspace.
3. Pin the upstream to the intended stable2603-8 baseline commit.
4. Build and verify the node, runtime, and Wasm output.
5. Generate genesis configuration and devnet artifacts.
6. Document each completed step as it is finished.

## Tests

* `cargo metadata --locked --format-version 1 --no-deps` (verify workspace members nonempty)
* `cargo check --workspace --locked`
* `cargo test --workspace --locked`

These checks are automated by `.github/workflows/bootstrap-solochain.yml` on the `engineering/solochain-bootstrap` branch.
