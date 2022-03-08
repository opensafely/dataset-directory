---
tags:
  - clinical concept
  - respiratory
  - QOF
---
# Athsma

## Introduction
_(idea: populate using NHS API)_

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

## Methodological Notes
There are a number of means by which one may ascerain a patient having asthma. Those supported within OpenSAFELY are excplicit coding on an asthma diagnosis, prescription of asthma medication, and record of hospitalisation with asthma; represented as phenotypes [has_asthma_diagnosis](../phenotypes/has_asthma.md), [receiving_asthma_medication](../phenotypes/has_asthma.md), and [hospitalised_with_asthma](../phenotypes/has_asthma.md). Of these, [has_asthma_diagnosis](../phenotypes/has_asthma.md) is generally considered the most reliable, but consideration must also be given to resolved cases of (usually childhood) asthma. A combined phenotype of [has_asthma](../phenotypes/has_asthma.md) is provided which takes these into account and should suffice for most purposes.

## Phenotypes
* [has_asthma](../phenotypes/has_asthma.md)
* [receiving_asthma_medication](../phenotypes/receiving_asthma_medication.md)
* [has_asthma_diagnosis](../phenotypes/has_asthma_diagnosis.md)
* [hospitalised_with_asthma](../phenotypes/hospitalised_with_asthma.md)
* [asthma_resolved](../phenotypes/asthma_resolved.md)

## Codelists
* [Asthma Admission Codes](https://www.opencodelists.org/codelist/primis-covid19-vacc-uptake/astadm/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Diagnosis](https://www.opencodelists.org/codelist/opensafely/asthma-diagnosis-snomed/) ❓ _Signed-off_ | ✅ _Externally-verified_
* [Asthma Inhaler Salbutamol Medication](https://www.opencodelists.org/codelist/opensafely/asthma-inhaler-salbutamol-medication/) ✅ _Signed-off_ | ❌ _Externally-verified_
* [Current Asmtha](https://www.opencodelists.org/codelist/opensafely/current-asthma/2020-05-06/)
* [Asthma annual review QOF](https://www.opencodelists.org/codelist/opensafely/asthma-annual-review-qof/33eeb7da/)
* [Peak expiratory flow rate (PEFR) codes](https://www.opencodelists.org/codelist/opensafely/peak-expiratory-flow-rate-pefr-codes/6110b805/)
* [Asthma resolved codes](https://www.opencodelists.org/builder/132f9e70/) ❌ _Signed-off_ | ❌ _Draft_

## Quality Outcomes Framework Indicators
QOF indicators pertaining to Asthma are defined by NICE as follows:

* [AST001](https://cks.nice.org.uk/topics/asthma/goals-outcome-measures/qof-indicators/)
>The contractor establishes and maintains a register of patients with asthma, excluding patients with asthma who have been prescribed no asthma-related drugs in the preceding 12 months
* [AST002](https://cks.nice.org.uk/topics/asthma/goals-outcome-measures/qof-indicators/)
>The percentage of patients aged 8 or over with asthma (diagnosed on or after 1 April 2006), on the register, with measures of variability or reversibility recorded between 3 months before and anytime after diagnosis
* [AST003](https://cks.nice.org.uk/topics/asthma/goals-outcome-measures/qof-indicators/)
>The percentage of patients with asthma, on the register, who have had an asthma review in the preceding 12 months that includes an assessment of asthma control using the 3 RCP questions
* [AST004](https://cks.nice.org.uk/topics/asthma/goals-outcome-measures/qof-indicators/)
>The percentage of patients with asthma aged 14 or over who have not attained the age of 20, on the register, in whom there is a record of smoking status in the preceding 12 months


Measurement of these indicators within OpenSAFELY has been performed in [this study]()

## Existing OpenSAFELY Studies
### Inhaled corticosteroids and risk of COVID-19 death
  * [GitHub Repository](https://github.com/opensafely/ics-research)
  * Paper - [Schultze A, Walker AJ, MacKenna B, Morton CE, Bhaskaran K, Brown JP, Rentsch CT, Williamson E, Drysdale H, Croker R, Bacon S. Risk of COVID-19-related death among patients with chronic obstructive pulmonary disease or asthma prescribed inhaled corticosteroids: an observational cohort study using the OpenSAFELY platform. The Lancet Respiratory Medicine. 2020 Nov 1;8(11):1106-20.](https://doi.org/10.1016/S2213-2600(20)30415-X)

## References
* [https://www.nhs.uk/conditions/asthma/]()
* [https://cks.nice.org.uk/topics/asthma]()

## Related Concepts
* [Smoking](./smoking.md)
* [COPD](./copd.md)


--8<-- "includes/abbreviations.md"