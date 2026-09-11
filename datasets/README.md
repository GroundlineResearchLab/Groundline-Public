# Groundline-Public Datasets

**Project:** Groundline Research Lab

**Repository:** Groundline-Public

**Section:** Public Datasets

**Framework:** DGCP™

## Purpose

The `datasets/` directory contains datasets that Groundline Research Lab has approved for public release.

Public datasets should support verification, research literacy, reproducibility, and public understanding of data systems.

A dataset should not be published merely because the underlying information is publicly accessible.

Publication requires sufficient provenance, context, documentation, and rights review.

## Dataset Standard

Each published dataset should clearly identify:

1. Dataset title.
2. Dataset identifier where applicable.
3. Publication date.
4. Data period or observation period.
5. Source or sources.
6. Retrieval date where relevant.
7. Geographic or system scope.
8. Unit of observation.
9. Field definitions.
10. Transformation methods.
11. Known limitations.
12. Missing data conditions.
13. Licensing or source restrictions.
14. Version or update status.

## Required Documentation

Each dataset should include documentation sufficient for another reader to understand what the data represents.

Recommended structure:

```text
dataset-name/
├── README.md
├── data/
├── sources/
└── methodology/
```

The exact structure may vary according to the dataset.

## Dataset README

A dataset level `README.md` should describe:

### Dataset Purpose

Why the dataset exists and what research question or public understanding objective it supports.

### Scope

The geographic, temporal, institutional, technical, or analytical boundaries of the dataset.

### Sources

The original sources used to construct the dataset.

Primary sources should be identified separately from secondary sources where relevant.

### Fields

Each field should have a clear definition.

Field names should not require undocumented assumptions.

### Method

Any cleaning, normalization, aggregation, categorization, matching, calculation, or transformation should be documented.

### Limitations

Known gaps, exclusions, source limitations, methodological constraints, and uncertainty should be stated.

### Update Status

The dataset should state whether it is:

• Static.
• Periodically updated.
• Continuously maintained.
• Superseded.
• Archived.

## Raw and Derived Data

Raw source material and derived data should be distinguished.

### Raw Data

Material reproduced directly from an original source without substantive analytical transformation.

Raw data may still undergo technical formatting changes where documented.

### Derived Data

Material created through processing, calculation, aggregation, classification, normalization, or combination of source data.

Derived data should identify the transformations used to create it.

## Source Preservation

Where redistribution rights permit, supporting source material may be preserved with the dataset.

Where redistribution is restricted, the dataset documentation should preserve references sufficient to locate or verify the original source.

A source should not be copied into this repository solely for convenience when redistribution rights are unclear.

## Data Transformation

Transformations should be reproducible where practical.

Examples include:

• Date normalization.
• Unit conversion.
• Currency normalization.
• Geographic matching.
• Category mapping.
• Duplicate removal.
• Missing value treatment.
• Aggregation.
• Derived calculations.

Transformations that materially affect interpretation should be documented explicitly.

## Missing Data

Missing data must not be silently converted into zero unless zero is the verified meaning.

Missing values may represent different states, including:

• Not reported.
• Not available.
• Not applicable.
• Not observed.
• Suppressed.
• Unknown.

Where these distinctions matter, they should be preserved.

## Data Quality

Dataset quality should be assessed relative to the source and intended use.

Quality considerations may include:

• Completeness.
• Consistency.
• Accuracy.
• Timeliness.
• Source authority.
• Field stability.
• Measurement method.
• Coverage.
• Duplicate risk.
• Transformation risk.

Publication does not imply that a dataset is complete or error free.

## Provenance

Every public dataset should preserve enough provenance to reconstruct its origin.

Where relevant, provenance may include:

• Source URL.
• Document title.
• Publishing institution.
• Publication date.
• Retrieval date.
• Dataset identifier.
• API endpoint.
• File version.
• Archive reference.
• Transformation history.

## Versioning

Material changes to a dataset should be traceable.

A new version may be appropriate when:

• Source data changes materially.
• Fields are added or removed.
• Methodology changes.
• Errors are corrected.
• Classification changes.
• Coverage expands.
• Historical data is revised by the source.

Earlier versions should not be silently overwritten where preserving them is necessary for research traceability.

## Corrections

Dataset corrections should identify:

1. The affected dataset or version.
2. The affected field or records where practical.
3. The nature of the error.
4. The correction applied.
5. The correction date.
6. Whether downstream analysis may be affected.

## External Rights

Third party data remains subject to the rights and terms of its original provider.

Groundline Research Lab does not grant rights to external data that it does not own.

A public Groundline dataset may therefore contain:

• Original Groundline data.
• Derived data.
• Referenced external data.
• Data subject to additional source conditions.

Any additional restrictions should be stated in the dataset documentation.

## Public Use

Groundline-Public datasets are intended to support:

• Public understanding.
• Research literacy.
• Independent verification.
• Educational use.
• Reproducible analysis.
• Evidence based discussion.

Users should evaluate the dataset within its documented scope and limitations.

## Relationship to Research Records

A dataset may support one or more Groundline research records.

Where a dataset is directly associated with an article, brief, explainer, or research record, that relationship should be documented.

The dataset itself should remain distinguishable from interpretations derived from it.

## Governance

All datasets published in this directory are subject to:

`governance/README.md`

and the repository level:

`LICENSE.md`

---

**Groundline Research Lab**
Research • Evidence • Data • Provenance • Understanding

Under the DGCP™ Framework
