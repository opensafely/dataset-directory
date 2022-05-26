<table>
<thead>
<tr>
<th>Name</th>
<th>Description</th>
<th>Default</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>from_dataset</code></td>
<td><p>string value; options are:
* '2019_prevalence' - a prevalence cohort of patients alive and on RRT in December 2019
* '2020_prevalence' - a prevalence cohort of patients alive and on RRT in December 2020
* '2021_prevalence' - a prevalence cohort of patients alive and on RRT in December 2021
* '2020_incidence' - an incidence cohort of patients who started RRT in 2020
* '2020_ckd' - a snapshot prevalence cohort of patient with Stage 4 or 5 CKD who were
reported to the UKRR to be under renal care in December 2020.</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>returning</code></td>
<td><p>string value; options are:
* "binary_flag"
* "renal_centre" - string indicating the code of the main renal centre a
patient is registered with
* "rrt_start_date" - the latest start date for renal replacement therapy
* "treatment_modality_start" - the treatment modality at <code>rrt_start_date</code> such as
ICHD, HHD, HD, PD, Tx
* "treatment_modality_prevalence" - the treatment modality from the prevalence data
* "latest_creatinine" - most recent creatinine held by UKRR
* "latest_egfr" - most recent eGFR held by UKRR</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>on_or_before</code></td>
<td><p>date of interest as a string with the format <code>YYYY-MM-DD</code>. Filters results to measurements
on or before the given date.</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>on_or_after</code></td>
<td><p>date of interest as a string with the format <code>YYYY-MM-DD</code>. Filters results to measurements
on or after the given date.</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>between</code></td>
<td><p>two dates of interest as a list with each date as a string with the format <code>YYYY-MM-DD</code>.
Filters results to measurements between the two dates provided (inclusive).
The two dates must be in chronological order.</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>date_format</code></td>
<td><p>a string detailing the format of dates to be returned.
It can be "YYYY-MM-DD", "YYYY-MM" or "YYYY" and wherever possible the least disclosive data should be
returned. i.e returning only year is less disclosive than a date with month and year.</p></td>
<td><code>None</code></td>
</tr>
<tr>
<td><code>return_expectations</code></td>
<td><p>as described elsewhere.</p></td>
<td><code>None</code></td>
</tr>
</tbody>
</table>