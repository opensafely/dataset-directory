---
tags:
  - phenotype
  - respiratory
---

# asthma_resolved()

## Introduction
This phenotype infers whether a patient's asthma has resolved by the given date.

## Parameters
*on_or_after* - date after which determination of asthma status should be made

## Phenotype validation reports

## Opensafely studies
_(auto-populated via GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
patients.with_these_clinical_events(asthma_resolved_codes, on_or_after=date)
```

## Codelists
* [Asthma resolved codes](https://www.opencodelists.org/builder/132f9e70/) ❌ _Signed-off_ | ❗ _Draft_

## Fields
*(Ideally these would link to data quality reports to each dataset/source/field)*

* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[CodedEvent](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#CodedEvent)/[CTV3Code]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_
* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[MedicationIssue](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#MedicationIssue)/[MultilexDrug_ID]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_
* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[MedicationDictionary](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#MedicationDictionary)/[DMD_ID]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_
* [SUS](https://docs.opensafely.org/dataset-apc/)/[APCS](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[Der_Diagnosis_All]()  --  _[updated 2022-02-07 09:47:31.867](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_

## References

## Contributors

## Sign-offs

## Tests

✅ Is excellent

✅ Is bloody marvellous

✅ Is fantastic

--8<-- "includes/abbreviations.md"