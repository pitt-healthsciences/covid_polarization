This page contains data and materials for The political polarization of COVID-19 treatments among physicians and laypeople in the United States. The data files are unaltered exports of the survey instruments that we administered to our participants. 

## Codebook and data description

The dataset is in long format, with each row representing a measure. 

### Variables

- `doc_id` and `lay_id` are anonymized identifiers that identify individual respondents.
- `respondent` indicates whether the participant is a layperson or a physician.
- `type` indicates the measure:
  - `choice` is a treatment choice (made by physicians only)
  - `effective` is a belief about effectiveness
  - `mandate` is a preference for vaccine mandates
  - `evidence` is a belief about the quality of clinical evidence
  - `peerbeliefs` is a prediction about the number of peers who answered a given question similarly.
  - `type` starting with `exp` indicates responses to experimental measures
- `treatment` indicates which treatment is in question
- `time` indicates when the measure was collected (`t1` = Phase 1; ...)
- `response` is the raw value for the reported measure
- `std_response` is the response value after standardization, which is done by subtracting the value from `mean_response_moderate` and dividing by the response's standard deviation (`sd_response`).
- `politics` is a measure of political ideology. For participants who responded to this question at multiple timepoints, we take the average of the two, as described in the supplementary materials.
- `female` is a dummy variable that takes a value `1` when the participant identified their gender as 'female', `0` otherwise.
- `education` captures laypeoples' level of education:
   - `1`: Less than high school 
   - `2`: High school or equivalent
   - `3`: Some college 
   - `4`: 2 year degree 
   - `5`: 4 year degree 
   - `6`: Graduate or professional degree 
   - `7`: Doctorate 
- `white` is a dummy variable that takes a value `1` when the participant identified as white, `0` otherwise.
- `density` is the population density (persons per square mile) in the participant's zip code. To preserve participant anonymity, this is rounded to the nearest thousand.
- `metropolitan` is a dummy value that takes a value of `1` if the participant lived in a census tract that was designated as 'metropolitan', `0` otherwise.
- `republican_voteprop_pres_2016` is the proportion of voters who voted for the republican presedential candidate in the participant's county in 2016. To preserve participant anonymity, this is rounded to the nearest .1. 
- `fox` is a dummy variable that takes a value of `1` if the participant indicated that they preferred Fox News to other cable news outlets, `0` otherwise.
- `clinical_time` describes the proportion of time that the participant reported working in a clinical capacity.
- `specialty` describes the participant's base clinical specialty.
- `practice_setting` describes the participant's primary practice setting.
- `research_engagement_scale` is a count variable of the number of ways that physicians engaged with clinical research. If we have responses at multiple timepoints, we take the average of the two.
- `evidence_skepticism_scale` is an composite of three items assessing (physicians') skepticism of published scientific research.
- `exp_condition` indicates the name of the drug shown to participants in the evidence evaluation experiment. 

### Coarsening for privacy

Several of the variables in this dataset have been coarsened or rounded to preserve participant anonymity (noted above). This is necessary because (e.g.) some US zip codes are uniquely identifiable based on their population density. For physicians in particular, combining zip code with demographic and professional characteristics could break anonymity. We carefully considered which variables to round or coarsen. If you believe that this coarsening limits your ability to learn from this dataset, please [contact us](mailto:joelmlevin@gmail.com) to discuss solutions.
