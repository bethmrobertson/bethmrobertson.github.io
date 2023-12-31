# Hospital Data Analysis Project using MySQL

**Project Description** <br>
This analysis is from a dataset of 70,000 clinical database records used in a study conducted in 2014.
Several different department administrators at the hospital want insights into specific parts of the data. I used MySQL to access, clean, and analyze the data. This page contains the questions asked, the results of the queries, and the action items. If you want to see the code behind all of this, click [here](Hospital_project_code.md).

<img src="images/Hospital Data Analysis Project banner.png?raw=true" height = 200/>

**Project Summary and Action Items**
- 82% of patients stay in the hospital fewer than 7 days.
- Some patients are seeing the same specialty for multiple procedures over multiple encounters. These patients should be investigated to determine if there are ways to prevent multiple visits and thus lower costs. Options might include case worker followups, better initial diagnoses, and more clear post-procedure medication instructions.
- Ensure all personnel are entering specialty information from a curated list.
- 2280 patients have no race information listed while 1524 have 'other' listed as their race. Does the range of possibilities for race need to be expanded?
- Ensure race information is collected upon admission.
- The average number of lab procedures performed does not vary significantly by race.
- There is a correlation between the number of lab procedures and the length of the hospital stay. Determine if one is causal of the other.
- Investigate emergency admissions that stayed less than the average number of days to find possible improvements for the future.
<br>

**Questions and Insights**
<br>
***Number of Days*** <br>
Our health care data analyst manager wants to know what the **distribution of time spent in the hospital** looks like.

A histogram is a way to show the number of occurrences using grouping. I used a histogram here, grouped by number of days in the hospital stay, to show the number of patients who stayed each number of days.

We can see that 80,617 of the 98,066 **(82%) of patients stayed less than 7 days**.
<br>
<img src="images/Hospital bar chart days of stay.png?raw=true" height=200/>￼

Each * = 200 patients

<br> ***Specialities*** <br>
There is a brand new Hospital Director who wants to know **which medical specialties are doing the most procedures**, on average. 

There are 73 medical specialties practiced at the hospitals in the study.

This table show the specialties with an average of more than 2.5 procedures and at least 50 patients.
<img src="images/Specialties w most procedures.png?raw=true" height=200/>￼
<br>
**Action Item:** The possible **duplication of specialties** (Radiologist / Radiology) indicates that the data needs to be thoroughly reviewed with the aim of establishing the correct way to enter this specialty into the system. The new procedure will need to be developed with those who know whether these two specialties should be combined and communicated to the people who are entering the data. 

**Action item:** There are some patients who appear to have **multiple procedures performed by the same specialty**. Are there other questions that need to be asked about these patients, like: Were those procedures performed during the same hospital stay? During the same specialty encounter? Which patients are having many repeat procedures? This could potentially provide some insights into ways to better manage patient health and satisfaction, as well as reduce costs.
<br>
<br>***Lab procedures by race***<br>
The Chief of Nursing wants to know if the hospital seems to be **treating patients of different races differently**, specifically regarding the number of lab procedures done.

<img src="images/Results Lab procs by race.png?raw=true" height=200/>

According to our analysis, **the average number of lab procedures does not vary significantly by race.**
<br>
<br>
**Action Item:** Figure out why there are so many **patient records with no race or “other”** recorded. Do some hospitals in the study not collect race data? Do some hospitals need to have additional race categories to choose from? What about people who are mixed race?

<br>***Average length of stay related to number of lab procedures***<br>
Many = 66 or more lab procedures<br>
Average = 33 to 66 lab procedures<br>
Few = fewer than 33 lab procedures<br>
<br>￼
<img src="images/Results avg stay time vs lab procs.png?raw=true" height=100/>
<br>
There seems to be a **correlation between number of lab procedures and length of stay**. 
<br>
**Action Item:** **Which of these is causing the other?** More labs because of a longer stay? A longer stay because of the need for more labs?

<br>***Up for Metformin***<br>

You just got an email from a co-worker in research. They want to do a medical test with anyone who is African American or had an "Up" for metformin. 

This table shows a partial result of African American patients and those with an “Up” for metformin. There are 20,059 results.
<br>￼<br>
<img src="images/Results partial Af Am or Up for metformin.png?raw=true" height=200/>

<br>***Hospital stays less than average stay length***<br>
The Hospital Administrator wants to highlight some of the biggest success stories of the hospital. They are looking for opportunities when patients **came into the hospital with an emergency** (admission_type_id of 1) **but stayed less than the average length of time in the hospital, 4.4 days**.

Partial result:<br><br>
<img src="images/Results partial stays less than avg.png?raw=true" height=200/>￼

**Action Item: investigate the story behind these successful hospital stays and find the causes of the stronger than average outcome.

<br>***Readmission Summary***<br>
Our boss has asked us to write a summary for the top 50 medication patients, break any ties with the number of lab procedures  (highest at the top). But they want a written summary of the format like this:
"Patient 2383 was Caucasian and was readmitted. They had 21 medications and 32 lab procedures."

Partial result:
<br> 
<img src="images/Results partial readmitted w num meds lab procs.png?raw=true" height=200/>
