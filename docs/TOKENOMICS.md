# AETH Tokenomics — Decisions Register

## Confirmed
- Native asset: AETH.
- Maximum supply target: 21,000,000 AETH.
- No ICO, presale, or external token sale.
- AETH is native to the AETHER sovereign chain, not an ERC-20 on another network.

## Open decisions
| Decision | Status |
|---|---|
| Genesis allocation and recipient accounts | OPEN |
| Smallest denomination / decimals | OPEN |
| Validator/staker reward curve | OPEN |
| Post-genesis issuance | OPEN |
| Fee distribution or burn policy | OPEN |
| Treasury controls | OPEN |
| Vesting and lockups | OPEN |
| Useful-work reward budget | OPEN |

Do not implement allocations until approved. Enforce the cap in runtime logic and test all issuance paths. Required invariant: total_issuance &lt;= 21,000,000 * units_per_AETH. The denomination must be selected before implementation.
