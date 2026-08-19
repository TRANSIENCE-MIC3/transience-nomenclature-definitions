# TRANSIENCE nomenclature definitions

Nomenclature definitions for the TRANSIENCE project (additions or overrides to common-definitions)

## Purpose and connection with other repositories

This repository contains codelists for the TRANSIENCE project that are
compatible with the `nomenclature-iamc` Python package. It is used by the
packages [`nomenclature-adapter`](https://github.com/i2amparis/nomenclature-adapter)
and [`validation-ui`](https://github.com/i2amparis/validation-ui) for
validating model, scenario, variable and region names and units, and for
defining aggregation mappings between regions, via the `transience` validation
profile (see `nomenclature-adapter`'s `profiles/transience.yaml`, which
specifies which branch/ref of this repository, and which ref of
`common-definitions`, are currently in use).

Definitions of variables in this repository come in addition to or override
ones given in the official
[`common-definitions`](https://github.com/IAMconsortium/common-definitions)
repository maintained by the IAMconsortium. `profiles/transience.yaml` pins a
specific commit of `common-definitions` (rather than tracking a branch), so
that this profile does not silently break if upstream makes incompatible
changes.

## Organization

Codelist definitions are stored in the `/definitions/` folder, and region
mappings in the `/mappings/` folder, like for any `nomenclature` definitions
repository.

Each of these folders contain a subfolder named `common-definitions-overrides`,
which contains definitions that override existing definitions in
`common-definitions`. These subfolders generally mirror the subfolder structures
and file names in the `common-definitions` repository. Files and subfolders
outside of `common-definitions-overrides` are additional definitions that are
not present in `common-definitions`.

The `main` branch of this repository is the master version of the recommended
names and mappings for use in TRANSIENCE. The GUI validation app/web app (at
[https://github.com/i2amparis/validation-ui](https://github.com/i2amparis/validation-ui))
uses definitions from whichever branch/ref `nomenclature-adapter`'s
`profiles/transience.yaml` currently points the `transience-defs` repository
at, which may differ from or be delayed relative to `main` -- e.g. during
active development, or in the case of technical issues arising from newly
added definitions.
