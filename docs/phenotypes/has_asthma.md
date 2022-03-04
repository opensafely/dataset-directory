---
tags:
  - phenotype
  - respiratory
---

# has_asthma()

## Introduction
This phenotype infers whether a patient has asthma based on three factors:

* primary care diagnosis code
* prescription of salbutamol inhaler
* admission to hospital with an asthma diagnosis code

## Parameters
*on_or_after* - date after which determination of asthma status should be made
## Short data reports

## Opensafely studies
_(auto-populated from GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
patients.with_these_clinical_events(asthma_diagnosis, on_or_after=date) OR
patients.with_these_medications(asthma_inhaler_salbutamol_medication, on_or_after=date) OR
patients.admitted_to_hospital(asthma_admission_codes, on_or_after=date)
```

## Codelists
* [Asthma Admission Codes](https://www.opencodelists.org/codelist/primis-covid19-vacc-uptake/astadm/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Diagnosis](https://www.opencodelists.org/codelist/opensafely/asthma-diagnosis-snomed/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Inhaler Salbutamol Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-salbutamol-medication/) ✅ _Signed-off_ | ❌ _Externally-verified_

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