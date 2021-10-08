# Parachain release: {{ env.RELEASE_VERSION }} ({{env.SHORT_SHA}})

{%- if env.PRE_RELEASE == "true" %}
⚠️  This is a **pre-release** provided to allow everyone to test and report issues.
   This is not a production version. Ensure appropriate backups allowing to revert.
{% endif %}

## ❗️Important Changes

👉 _FILL_IF_ANY_

## Runtimes:

- Statemine:
  - spec_version: 4
  - transaction_version: 2
- Westmint:
  - spec_version: 4
  - transaction_version: 2

This release was tested against the following versions of `rustc`.
Other versions may work as well.

- rustc 1.53.0 (53cb7b09b 2021-06-17)

NOTE: The WASM runtimes built with [srtool](https://github.com/paritytech/srtool) using `rustc 1.53.0 (53cb7b09b 2021-06-17)`.

### Runtime Hashes

The following hashes are the encoded call hashes for a `parachainSystem.authorizeUpgrade` call over XCM for the **compressed** runtimes:
- Statemine: `👉 _FILL_THAT_UP_`
- Westmint: `👉 _FILL_THAT_UP_`

Those hashes can be checked using (example for statemine):
`subwasm --json info statemine_runtime.compact.compressed.wasm | jq -r .parachain_authorize_upgrade_hash`

{{ env.CHANGELOG }}
