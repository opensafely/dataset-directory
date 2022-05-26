---
tags:
  - raw dataset
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
---
# COVID-19 Therapeutics Data

[GitHub Repository for this raw dataset evaluation](https://github.com/opensafely/covid-therapeutics-notebook), performed by [Helen Curtis](https://github.com/HelenCEBM)


## Source
A patient-level dataset on antivirals and nMABs treatments (Molnupiravir, Sotrovimab, Casirivimab, and Imdevimab), the COVID-19 “Therapeutics” dataset, has been provided by NHS England. 
It largely consists of data from BlueTeq, the system in which assessment forms are completed and submitted to the NHS, and was first received on 27th Jan 2022. 

## Linkage
In line with OpenSAFELY standards on privacy and security, the Therapeutics dataset was linked to primary care records in the secure data warehouse of TPP using hashed NHS numbers, and fields pertaining to Trust, Trust ODS code and CCG name were not made available within OpenSAFELY-TPP. 


## Schema
The _COVID-19 Therapeutics Data_ dataset consists of only one table, henceforce referred to as the _Therapeutics_ table. 

### Therapeutics

The initial COVID-19 Therapeutics dataset in OpenSAFELY-TPP contained 18 columns. Below is a brief description of the field type and specification.

{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_schema.md"
%}

## Inclusion/Exclusion Criteria
Assessment forms held in the BlueTeq system but not approved, e.g. those not yet submitted to the NHS or where treatment was decided against, were not included; included Statuses are shown in Table 1. 
{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_inclusion.md"
%}

## Data Quality
**Summary of the COVID-19 Therapeutics dataset in OpenSAFELY-TPP. The number of distinct values and missing values is shown for each column of data, both overall and filtered to rows with COVID_indication = 'non_hospitalised’. Counts of missing values are rounded to the nearest 10 and small numbers shown as “1-5”. _**
{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_quality.md"
%}

### Completeness
Completeness of most fields was 100%. 
Exceptions were TreatmentStartDate (between 1-5 missing) and fields relating to symptom onset and risk cohorts for Molnupiravir, Sotrovimab and Casirivimab/imdevimab: these fields were assessed for completeness for the relevant treatments only, and were always complete save for 1-5 rows for molnupriavir

### Key fields
Two fields were key for identifying the setting and type of treatment: COVID_indication and Intervention. COVID_indication had three possible values: ‘hospitalised_with’, ‘non_hospitalised’, and ‘hospital_onset’, reflecting the setting in which the patient was being considered for treatment (which determines the range of treatments available at the time). The Intervention field had six possible values, ‘Remdesivir’, ‘Tocilizumab’, ‘sarilumab’, ‘Casirivimab and imdevimab ’, ‘Molnupiravir’, and ‘Sotrovimab’. Only the latter three were present for non-hospitalised patients. 

### Date fields
There were two fields in datetime format related to when treatment took place: Received and TreatmentStartDate. The Received date is generated when the form is submitted. TreatmentStartDate is entered by the clinician and may be in the future as the planned start date, or in the past by the time the form is submitted. The Received date was largely later than the TreatmentStartDate (61.1% of rows) but in 36.9% of rows, both were the same date. There were 20 TreatmentStartDates which were more than one month beyond the latest Received date, suggesting that TreatmentStartDates may occasionally be supplied incorrectly, e.g. a date too far in the future. 

_Comparison of the values of ‘Received’ and ‘TreatmentStartDate’ fields in the COVID-19 Therapeutics data in OpenSafely, both overall and filtered to rows with COVID_indication='non_hospitalised’. _
{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_date_comparison.md"
%}

A further three fields were supplied in date-like format but recorded as free text: MOL1_onset_of_symptoms, SOT02_onset_of_symptoms, and CASIM05_date_of_symptom_onset. Each of these reflect the date of COVID-19 symptom onset reported by the patient, corresponding to the particular intervention under consideration i.e. MOL1_onset_of_symptoms for Molnupiravir. In addition to the large number of missing values in these fields, many different formats were used, e.g. ‘dd-mm-yy’, ‘dd Month yyyy’, ‘yyyy-mm-dd‘. There was occasionally some free text describing specific symptoms. There were 28 values which were not date-like or which contained only a partial date: entirely numeric (n=10), largely or entirely non-numeric (n≤5), starting and/or ending non-numeric (n=10) and no valid year (n=10). 

### Other fields
Region appeared to be a automatically generated field based upon the location of the CMDU submitting the form, and corresponding to the seven NHS England regions: ‘East of England’, ‘London’, ‘Midlands’, ‘North East and Yorkshire’, ‘North West’, ‘South East’, and ‘South West’.

Three text fields reflected the high-risk group(s) to which the patient was considered to belong, each corresponding to the particular intervention under consideration: MOL1_high_risk_cohort (molnupiravir), SOT02_risk_cohorts (sotrovimab) and CASIM05_risk_cohort (Casirivimab/imdevimab). These were derived from tick-boxes on the corresponding form. In total there were 13 distinct risk groups available for selection (Table 4). Where a clinician checked multiple boxes, risk groups were joined by the word ‘and’. For each intervention there were 29, 27 and 15 distinct combinations of risk groups, respectively. 

_Equivalent risk groups which were labelled differently depending on which form was being completed are indicated by “OR”._
{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_risk_groups.md"
%}

### Duplication
For non-hospitalised patients, there were 4460 distinct patient IDs present in the data. Of these, 4410 appeared once and 50 appeared twice or more. Patients with multiple records most commonly had different values for Intervention, TreatmentStartDate, Received, or both Intervention and one of the date fields.

_Patients appearing more than once in the COVID-19 Therapeutics dataset, both overall and filtered to rows with COVID_indication='non_hospitalised’._
{%
    include-markdown "../../includes/tables/covid-19_therapeutics/raw_duplicates.md"
%}