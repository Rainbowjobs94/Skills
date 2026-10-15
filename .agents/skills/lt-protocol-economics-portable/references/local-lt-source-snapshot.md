# Local LT source snapshot

Prepared 2026-10-15 from a bounded inspection of the current workspace. The
expanded ZIP includes companion local reviews under `project-review/`; those are
dated project evidence, not portable defaults. This remains a source snapshot,
not an exhaustive protocol audit, not a chain-state check, and not authority to
change economics. Recheck all source paths and deployment state before use.

## Directly observed contract source

The workspace contains Solidity source files under `contracts/contracts/`,
including:

`BipartisanCoin.sol`, `BuschWorldCoin.sol`, `CFTCoin.sol`, `CryptoLeachingVault.sol`,
`CryptoValueBooster.sol`, `DemocraticCoin.sol`, `DisneyDimensionCoin.sol`,
`DrewBarrymoreCoin.sol`, `EpicCoin.sol`, `EpicUniverseVault.sol`, `GasCoin.sol`,
`GCLPHelper.sol`, `GlobeAx.sol`, `GlobeCx.sol`, `GlobeDx.sol`, `GlobeMx.sol`,
`God2Coin.sol`, `GodCoin.sol`, `HeroVillainsCoin.sol`, `JasperCoin.sol`,
`KellyCoin.sol`, `KellymoreCoin.sol`, `MickeyDimensionCoin.sol`,
`MiracleCoin.sol`, `MiracleMultiplier.sol`, `ModernJesusCoin.sol`,
`PrincessCoin.sol`, `RepublicanCoin.sol`, `SeaGardensCoin.sol`, `SesameCoin.sol`,
`SoulCoin.sol`, `SwapCoin.sol`, `UniversalCoin.sol`, and `WavesOfAdventure.sol`.

File presence proves only that source files exist. Names/symbols, chain,
deployment, issuer, current supply, market value, redemption, and production
status must each be checked independently.

## Selected code observations and conflicts

| Source | Code observation | Not established by this source |
|---|---|---|
| `contracts/contracts/GodCoin.sol` | ERC-20 `GC`, 0 decimals; owner-only `mint` and `mintWithProof`; no supply cap in this contract. | BTC/ETH backing, global market uplift, stable value, reserves, or a production deployment. Event counters do not prove an external market moved. |
| `contracts/contracts/ModernJesusCoin.sol` | ERC-20 `MJC`, 0 decimals; owner-only unlimited `mint` and `mintFromGC`; `mintFromGC` increments `totalMinted` and emits source amount. | No transfer of GC or collateral verification appears in `mintFromGC`; price, backing, redemption, and unlimited reserve value are not enforced here. |
| `contracts/contracts/MiracleCoin.sol` | ERC-20 `MC`, 0 decimals; `MAX_SUPPLY = 7_365 * 10**18`; monthly claim mints one MC and calls SC mint for 1,000,000; claim window is timestamp divided by 30 days. | Dollar valuation and available supply in a live deployment. The contract symbol is `MC`, not proof it is `MCL`. |
| `contracts/contracts/SoulCoin.sol` | ERC-20 `SC`, 0 decimals; cap `777 * 10**18`; only owner/approved minters can mint; cap enforced. | USD peg, GC backing, or redemption. These are described in comments but not enforced by the shown mint path. |

These observations expose material naming/economics conflicts in the local
ecosystem master skill: it describes MCL and RC mechanics not established by
these inspected contracts; its RC bonding-curve statements require locating and
verifying the actual source before use. Do not treat that skill’s unsupported
values, addresses, URLs, roles, or deployment commands as current facts.

## Duplicate supplied protocol notes

Two files named
`attached_assets/Pasted-The-miracle-network-protocol-for-God-coin-Modern-Jesus-_1781285873219.txt`
and
`attached_assets/Pasted-The-miracle-network-protocol-for-God-coin-Modern-Jesus-_1781286401430.txt`
had the same SHA-256 during inspection:

`15949f153c42fc70a9b47c787c4a6a6de58164cc87c40ed3c20bc7313d5d5b04`

A third similarly named file had a different SHA-256:

`30dacb810166b6a4556e63e3a6982f93e693ef40b26a29c090b275b56c6bbaa7`

The files’ contents and provenance were not yet reconciled. Treat the matching
pair as duplicate bytes, not independent confirmation; inspect the differing
file before incorporating claims.

## Review coverage and open work

- Enumerated all local Solidity contract filenames and performed a static
  signature/metadata scan. Read core MC, MJC, GC, SC sources; other contract
  details remain a quick inventory, not a manual audit.
- Read local deployment registries as candidate records; did not query Polygon.
- Did not inspect every contract’s implementation, run the contract test suite,
  read all token deployment registries, query Polygon, inspect every project task,
  or validate the external master-skill claims.
- Build a complete ledger from all actual contract/API/schema/frontend sources,
  deployment candidates and read-only live state before calling the protocol
  catalog complete.
- Do not copy the local snapshot into another project as facts; regenerate it
  against that project’s sources.
