# Vetting checksets

This folder holds project-specific vetting checkset specs, consumed by the
[`vetting-adapter`](https://github.com/i2amparis/vetting-adapter) package
(specifically `vetting_adapter.core.spec.build_check_from_spec`). It plays the
same role for vetting checks that `definitions/` and `mappings/` play for
name validation and region mapping: it is referenced from this project's
profile manifest in `nomenclature-adapter` (`profiles/transience.yaml`, under
the `vetting:` key), and cloned/read on demand.

Each `*.yaml` file here is one checkset spec. See the comments in
`gdp_pop_harmonization.yaml` for the schema and for the current status of
that particular checkset (added to exercise the mechanism end to end, not
(yet) real TRANSIENCE reference data).

General-purpose checks that aren't specific to any one project, such as the
IPCC AR6 vetting checks, do not need an entry here -- `vetting-adapter`
includes those automatically for every profile.
