---
tags:
  - phenotype
  - respiratory
---

# has_asthma()

## Introduction
This phenotype infers whether a patient has asthma based on four other phenotypes:

* [has_asthma_diagnosis](./has_asthma_diagnosis.md) - primary care diagnosis code
* [receiving_asthma_medication](./receiving_asthma_medication.md) - patient has active prescription for asthma medication
* [hospitalised_with_asthma](./hospitalised_with_asthma.md) - admission to hospital with an asthma diagnosis code
* [asthma_resolved](./asthma_resolved.md) - NOT asthma resolved

## Parameters
*on_or_after* - date after which determination of asthma status should be made
## Phenotype validation reports

## Opensafely studies
_(auto-populated via GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
NOT asthma_resolved(date) AND (
  has_asthma_diagnosis(date) OR
  receiving_asthma_medication(date) OR
  hospitalised_with_asthma(date)
)
```

## Codelists
* [Asthma resolved codes](https://www.opencodelists.org/builder/132f9e70/) ❌ _Signed-off_ | ❗ _Draft_
* [Asthma Admission Codes](https://www.opencodelists.org/codelist/primis-covid19-vacc-uptake/astadm/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Diagnosis](https://www.opencodelists.org/codelist/opensafely/asthma-diagnosis-snomed/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Inhaler Salbutamol Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-salbutamol-medication/) ✅ _Signed-off_ | ❌ _Externally-verified_
* [Asthma Inhaler Steroid Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-steroid-medication/2020-04-15/) ✅ _Signed-off_ | ❌ _Externally-verified_
* [Asthma Oral Prednisolone Medication](https://www.opencodelists.org/codelist/opensafely/asthma-oral-prednisolone-medication/2020-04-27/) ✅ _Signed-off_ | ❌ _Externally-verified_

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