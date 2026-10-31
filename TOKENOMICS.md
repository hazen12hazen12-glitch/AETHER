# AETH Tokenomics — Decisions Register

## Confirmed

- Native asset: AETH.
- Maximum supply: 21,000,000 AETH.
- No ICO.
- No presale.
- No external token sale.
- AETH is intended to be native to the AETHER sovereign chain, not merely a wrapped asset or ERC-20 on a third-party chain.

## Not yet approved

| Decision | Status |
|---|---|
| Genesis allocation percentages and recipient accounts | OPEN |
| Validator/staker reward curve | OPEN |
| Whether any post-genesis issuance is permitted | OPEN |
| Transaction fee distribution/burn policy | OPEN |
| Treasury funding and spending controls | OPEN |
| Vesting and lockup schedules | OPEN |
| Useful-work reward budget and verification policy | OPEN |
| Smallest denomination / decimals | OPEN |

No allocation percentages should be implemented until approved. A hard cap must be enforced in runtime logic and covered by tests, including reward minting, genesis issuance, privileged calls, migrations and edge cases.

## Required invariant

For every reachable runtime state:

`total_issuance <= 21_000_000 * units_per_AETH`

The value of `units_per_AETH` must be explicitly selected and documented before runtime implementation.
