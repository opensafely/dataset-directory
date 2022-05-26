<table>
  <tr>
   <td>
   </td>
   <td><strong>Input</strong>
   </td>
   <td><strong>Details</strong>
   </td>
  </tr>
  <tr>
   <td rowspan="7" >Returning options
   </td>
   <td>binary_flag
   </td>
   <td>
<ul>

<li>Patient ID present in dataset or not.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>date
   </td>
   <td>
<ul>

<li><em>TreatmentStartDate</em>
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>therapeutic
   </td>
   <td>
<ul>

<li>Comma-separated string from <em>Intervention</em> (removing " and ") 
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>risk group
   </td>
   <td>
<ul>

<li>Comma-separated string, from union of individual risk group fields (removing " <em>and</em> " and "<em>Patients with a </em>"). 

<li>Does not remove duplicates (e.g. "<em>cancer,cancer</em>" can be returned) 
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>region
   </td>
   <td>
<ul>

<li><em>Region</em>
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>number_of_matches_in_period
   </td>
   <td>
<ul>

<li>Number of times patient ID present in dataset.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>number_of_episodes
   </td>
   <td>
<ul>

<li>Number of times patient ID present in dataset, with at least the specified period of time between each <em>TreatmentStartDate</em> (e.g. “14 days”)
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="3" >Filter options
   </td>
   <td>with_these_statuses
   </td>
   <td>
<ul>

<li>Filters on <em>CurrentStatus</em>. 

<li>Should be one or more of 'Approved', 'Treatment Complete', 'Treatment Not Started', 'Treatment Stopped'. 

<li>Case insensitive.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>	with_these_therapeutics
   </td>
   <td>
<ul>

<li>Filters on <em>Intervention</em>. 

<li>case insensitive.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>with_these_indications
   </td>
   <td>
<ul>

<li>Filters on <em>COVID_indication</em>. 

<li>Should be one or more of 'non-hospitalised', 'hospital_onset', 'hospitalised_with'. 
</li>
</ul>
   </td>
  </tr>
</table>

