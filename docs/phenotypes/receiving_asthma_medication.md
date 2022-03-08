---
tags:
  - phenotype
  - respiratory
---

# receiving_asthma_medication()

## Introduction
This phenotype infers whether a patient has received a prescription for asthma-related medication in the preceeding three months from the provided date.

## Parameters
*on_or_after* - date after which determination of asthma status should be made
## Phenotype validation reports

## Opensafely studies
_(auto-populated via GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
patients.with_these_medications(asthma_inhaler_salbutamol_medication, on_or_after=(date - 3 months)) OR
patients.with_these_medications(asthma_inhaler_steroid_medication, on_or_after=(date - 3 months)) OR
patients.with_these_medications(asthma_oral_prednisolone_medication, on_or_after=(date - 3 months)) OR
```

## Codelists

* [Asthma Inhaler Salbutamol Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-salbutamol-medication/) ✅ _Signed-off_ | ❌ _Externally-verified_
* [Asthma Inhaler Steroid Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-steroid-medication/2020-04-15/) ✅ _Signed-off_ | ❌ _Externally-verified_
* [Asthma Oral Prednisolone Medication](https://www.opencodelists.org/codelist/opensafely/asthma-oral-prednisolone-medication/2020-04-27/) ✅ _Signed-off_ | ❌ _Externally-verified_

## Fields
*(Ideally these would link to data quality reports to each dataset/source/field)*

* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[MedicationIssue](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#MedicationIssue)/[MultilexDrug_ID]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_
* [TPP](https://docs.opensafely.org/dataset-systmone/)/[S1](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[MedicationDictionary](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#MedicationDictionary)/[DMD_ID]()  --  _[updated 2022-01-28 11:00:04.417](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_

## References

## Contributors
*(Those who have contributed to the phenotype AND the underlying codelists)*

* [Caroline Morton](https://github.com/CarolineMorton)
* [Brian MacKenna](https://github.com/brianmackenna)

## Sign-offs

## Tests

✅ Is excellent

✅ Is bloody marvellous

✅ Is fantastic

--8<-- "includes/abbreviations.md"