# Code for the Hospital Data Analysis Project using MySQL

**Project Description** <br>
This page shows the code I used for the different steps of this project.

***Number of Days*** 
<br>
I used a bar chart to show the number of patients who stayed a certain number of days to understand if most patients in the study stayed fewer than 7 days in the hospital.
<br>
<img src="images/Code Days of stay.png?raw=true" height=300/>￼

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
The Hospital Administrator wants to highlight some of the biggest success stories of the hospital. They are looking for opportunities when patients came into the hospital with an emergency (admission_type_id of 1) but stayed less than the average length of time in the hospital, 4.4 days.

Partial result:<br><br>
<img src="images/Results partial stays less than avg.png?raw=true" height=200/>￼

**Action Item: investigate the story behind these successful hospital stays and find the causes of the stronger than average outcome.

<br>***Readmission Summary***<br>
Our boss has asked us to write a summary for the top 50 medication patients, break any ties with the number of lab procedures  (highest at the top). But they want a written summary of the format like this:
"Patient 2383 was Caucasian and was readmitted. They had 21 medications and 32 lab procedures."

Partial result:
<br> 
<img src="images/Results partial readmitted w num meds lab procs.png?raw=true" height=200/>
