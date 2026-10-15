# Protocol and economics ledger

Create one row for each asset, contract, mining/reward rule, reserve/pool, oracle,
maturity rule, fee, and cross-project integration. Link each row to the exact
source and distinguish code enforcement from source claim.

| System | Asset / protocol | Symbol / units | Chain / address | Supply / cap | Issuer / authority | Eligibility / proof | Formula / allocation / maturity | Backing / reserve / settlement | Fees / replay / concurrency | Code & test evidence | Deployment evidence | Conflict / status / next decision |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |  |  |  |  |  |

## Controlled vocabulary

Use `OBSERVED`, `SOURCE_CLAIM`, `PROPOSED`, `IMPLEMENTED`, `TESTED`,
`DEPLOYED`, `CONFLICT`, `BLOCKED`, `UNAVAILABLE`, and `COUNSEL_REQUIRED`.

## Unit and fund separation checklist

- [ ] Raw integer units, display units, decimals, and conversion direction shown.
- [ ] Activity/proof score is separate from accounting credit.
- [ ] Accounting credit is separate from minted token supply.
- [ ] Token supply is separate from market price and reserve.
- [ ] Reserve/collateral is separate from legal obligation and redemption promise.
- [ ] User claim eligibility is separate from transaction settlement.
- [ ] Contract authority, cap, replay control, and idempotency are evidenced.
- [ ] Tests and deployment evidence are separately recorded.
