# Upgrades Statemine and Westmint to Polkadot to v0.9.10

⚠️  This is a **pre-release** provided to allow everyone to test and report issues.

## ❗️Important Changes

+ New host functions: paritytech/substrate#9391
  + THIS REQUIRES COLLATORS TO UPGRADE THEIR NODES BEFORE THE 0.9.10 RUNTIME UPGRADE HITS THE RELAY CHAIN
+ Transaction Version changed (1 -> 2)
  + `pallet-xcm` extrinsics have changed and require different encoding.

## Notable Changes
+ Support XCM v1

## Native runtimes:

- Statemine: 4 (spec_version), 2 (transaction_version)
- Westmint: 4 (spec_version), 2 (transaction_version)

This release was tested against the following versions of `rustc`. Other versions may work.

- rustc 1.53.0 (53cb7b09b 2021-06-17)

NOTE: The WASM runtimes built with [srtool](https://github.com/paritytech/srtool) using `rustc 1.53.0 (53cb7b09b 2021-06-17)`.

## Runtime Hashes

The following hashes are the encoded call hashes for a `parachainSystem.authorizeUpgrade` call over XCM for the **compressed** runtimes:
- Statemine: `0x3834af2fe18d33138365ae309cd9f4e4ba273be9beb087ec88b6dd6c8ac840ae`
- Westmint: `0xbe74abb3a98e2a4a1f4bc3d37902e48b58888188484b28e17baf3a4245de894b`

Those hashes can be checked using (example for statemine):
`subwasm --json info statemine_runtime.compact.compressed.wasm | jq -r .parachain_authorize_upgrade_hash`


{{ CHANGELOG }}
