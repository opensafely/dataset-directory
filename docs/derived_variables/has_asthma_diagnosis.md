---
tags:
  - phenotype
  - respiratory
---

# has_asthma_diagnosis()

## Introduction
This phenotype infers whether a patient has asthma an asthma diagnosis recorded in their primary care EHR.

## Parameters
*on_or_after* - date after which determination of asthma status should be made
## Phenotype validation reports

## Opensafely studies
_(auto-populated via GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
patients.with_these_clinical_events(asthma_diagnosis, on_or_after=date) OR
```

## Codelists
* [Asthma Diagnosis](https://www.opencodelists.org/codelist/opensafely/asthma-diagnosis-snomed/) ❓ _Signed-off_ | ✅ _Externally-verified_

## Fields
*(Ideally these would link to data quality reports to each dataset/source/field)*

* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[CodedEvent](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#CodedEvent)/[CTV3Code]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_

## References

## Contributors
* [Caroline Morton](https://github.com/CarolineMorton)

## Sign-offs

## Tests

✅ Is excellent

✅ Is bloody marvellous

✅ Is fantastic

--8<-- "includes/abbreviations.md"