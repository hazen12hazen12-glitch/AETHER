# Security Policy

## Scope

This policy covers the AETHER node, runtime, custom pallets, EVM integration, build/release pipeline and network operations.

## Reporting

Do not publish exploitable vulnerabilities, private keys, validator seed material or sensitive operational details in public issues. Use a private security reporting channel configured by repository maintainers before any public testnet.

## Mandatory controls

- Never commit mnemonic phrases, private keys, keystores, API tokens or production secrets.
- Keep validator keys off developer workstations and source control.
- Require deterministic runtime builds and dependency pinning.
- Review all privileged runtime calls and storage migrations.
- Test total issuance cap and authorization boundaries.
- Bound all user-controlled inputs and computational weights.
- Separate AI work scoring from consensus validity and finality.
- Threat-model EVM precompiles, RPC exposure, transaction validation and fee accounting.
- Require independent review before public testnet/mainnet.

## Status

No production node or validator network is currently represented by this documentation package.
