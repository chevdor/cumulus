
# Cumulus releases

This repository contains 2 types of releases:
- cumulus crates
- parachains: binary + runtimes

## Naming conventions

The release workflows start when they recognize specific patterns as described below.

### Cumulus crates

Triggers on: **TAG** named `polakdot-vX.Y.Z`

Cumulus crates are released based on a given Polkadot version. When releasing a new Cumulus version matching Polkadot v1.2.3, you should:
- ensure that your substrate dependency is `polkadot-v1.2.3`
- ensure that your polkadot dependency is `release-v1.2.3`
- create a new tag named `polkadot-v1.2.3`

### Parachains

Triggers on: **TAG** named `parachains-vX.Y.Z`

The `parachains` releases contain the `polkadot-collator` binary as well as the various parachains runtime.
