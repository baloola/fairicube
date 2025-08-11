# FAIRiCUB Extension Specification

- **Title:** FAIRiCUBE
- **Identifier:** <https://stac-extensions.github.io/fairicube/v1.0.0/schema.json>
- **Field Name Prefix:** template
- **Scope:** Item, links
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @baloola

This document explains the Template Extension to the [SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.
This is the place to add a short introduction.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [ ] Catalogs
- [ ] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [x] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [x] Links
- [x] Bands

| Field Name           | Type                      | Description                                  |
| -------------------- | ------------------------- | -------------------------------------------- |
| fairicube:use_case   | string                    | Describe the required field...               |
| fairicube:quality_measures         | string | The applied quality measures on data (standardised calibration, repeated samples or measurements, data capture, data entry validation, peer review of data, or representation with controlled vocabularies)                        |
| fairicube:definition   | string                | A semantic definition (or link) for the supplied dataset (what measurements are represented eg. velocity)                        |
| fairicube:comment   | string                  | Any helpful comments about the dataset e.g. processing details for processors and producers                        |
| fairicube:interpolation   | string                  | DThe method which has been applied for Interpolation / aggragation (NA, nearest, spline, etc.)                        |


### Additional Field Information



## Relation types

The following types should be used as applicable `rel` types in the
[Link Object](https://github.com/radiantearth/stac-spec/tree/master/item-spec/item-spec.md#link-object).

| Type           | Description                           |
| -------------- | ------------------------------------- |
| measurement_method | A URL to a workflow, protocol, plan, algorithm, or computational method specifying how create a value. |

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid.
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
