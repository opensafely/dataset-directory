---
tags:
  - phenotype
  - respiratory
---

# hospitalised_with_asthma()

## Introduction
This phenotype infers whether a patient has an admission to hospital with an asthma diagnosis code on or after the supplied date.

## Parameters
*on_or_after* - date after which determination of asthma status should be made

## Phenotype validation reports

## Opensafely studies
_(auto-populated via GitHub API)_

* [NHS Service Restoration Observatory - Asthma](https://github.com/opensafely/asthma_sro)

## Implementation

```py
patients.admitted_to_hospital(asthma_admission_codes, on_or_after=date)
```

## Codelists
* [Asthma Admission Codes](https://www.opencodelists.org/codelist/primis-covid19-vacc-uptake/astadm/) ❓ _Signed-off_ | ✅ _Externally-verified_

## Fields
*(Ideally these would link to data quality reports to each dataset/source/field)*

* [SUS](https://docs.opensafely.org/dataset-apc/)/[APCS](https://reports.opensafely.org/reports/opensafely-tpp-database-schema/#Data-sources)/[Der_Diagnosis_All]()  --  _[updated 2022-02-07 09:47:31.867](https://reports.opensafely.org/reports/opensafely-tpp-database-builds/#Import-dates-and-date-coverage-for-OpenSAFELY-TPP-data-sources)_

## References

## Contributors
*(Those who have contributed to the phenotype AND the underlying codelists)*

## Sign-offs

## Tests

✅ Is excellent

✅ Is bloody marvellous

✅ Is fantastic

--8<-- "includes/abbreviations.md"