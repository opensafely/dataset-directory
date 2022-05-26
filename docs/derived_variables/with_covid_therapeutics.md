---
tags:
  - COVID-19
  - antiviral
  - MAB
  - nMAB
  - monoclonal
  - antibodies
  - Molnupiravir
  - Sotrovimab
  - Casirivimab
  - Imdevimab
  - Therapeutics
---

# with_covid_therapeutics()

This function may be used to derive variables indicating the prescription(s) of a [COVID-19 Therapeutic](../derived_data/covid-19_therapeutics.md) for a patient, the start date of this prescription, the therapeutic(s) prescribed, the patient's risk group and region.

## Usage
Detailed documentation on the usage of the with_covid_therapeutics() function may be found within the [OpenSAFELY documentation](https://docs.opensafely.org/study-def-variables/#cohortextractor.patients.with_covid_therapeutics)

```py
with_covid_therapeutics(with_these_statuses=None, with_these_therapeutics=None, with_these_indications=None, on_or_before=None, on_or_after=None, between=None, returning='binary_flag', date_format=None, find_first_match_in_period=None, find_last_match_in_period=None, include_date_of_match=False, episode_defined_as=None, return_expectations=None)
```

### Parameters
{
    include-markdown "../../includes/tables/covid-19_therapeutics/with_covid_therapeutics_parameters.md"
}