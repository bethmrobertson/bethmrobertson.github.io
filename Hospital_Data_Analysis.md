# Hospital Data Analysis Project using MySQL

**Project Description** <br>
This analysis is from a dataset of 70,000 clinical database records used in a study conducted in 2014.
Several different department administrators at the hospital want insights into specific parts of the data. I used MySQL to access, clean, and analyze the data. 

<img src="images/?raw=true"/>

**The Big Reveal**
- 

**The Data**
<br>**Questions and Insights** <br>
<br>  ***Number of Days*** <br>
Our health care data analyst manager wants to know what the distribution of time spent in the hospital looks like.

A histogram is a way to show the number of occurrences using grouping. I used a histogram here, grouped by number of days in the hospital stay, to show the number of patients who stayed each number of days.

We can see that 80,617 of the 98,066 (82%) of patients stayed less than 7 days.
<br>
<img src="images/Hospital bar chart days of stay.png?raw=true"/>￼
Each * = 200 patients

<br> ***Specialities*** <br>
There is a brand new Hospital Director who wants to know what medical specialties are doing the most number of procedures on average. 

There are 73 medical specialties practiced at the hospitals in the study.

This table show the specialties with an average of more than 2.5 procedures and at least 50 patients.
￼
**Action Item: The possible duplication of specialties (Radiologist / Radiology) indicates that the data needs to be thoroughly reviewed with the aim of establishing the correct way to enter this specialty into the system. The new procedure will need to be developed with those who know whether these two specialties should be combined and communicated to the people who are entering the data. 

**Action item: There are some patients who appear to have multiple procedures performed by the same specialty. Are there other questions that need to be asked about these patients, like: Were those procedures performed during the same hospital stay? During the same specialty encounter? Which patients are having many repeat procedures? This could potentially provide some insights into ways to better manage patient health and satisfaction, as well as reduce costs.

<br>***Lab procedures by race***<br>
The Chief of Nursing wants to know if the hospital seems to be treating patients of different races differently, specifically regarding the number of lab procedures done.

According to our analysis, the average number of lab procedures does not vary significantly by race.

**Action Item: Figure out why there are so many patient records with no race or “other” recorded. Do some hospitals in the study not collect race data? Do some hospitals need to have additional race categories to choose from? What about people who are mixed race?

<br>***Average length of stay related to number of lab procedures***<br>
Many = 66 or more lab procedures
Average = 33 to 66 lab procedures
Few = fewer than 33 lab procedures

￼
There seems to be a correlation between number of lab procedures and length of stay. 

**Action Item: Which of these is causing the other? More labs because of a longer stay? A longer stay because of the need for more labs?

<br>***“Up” for metformin***<br>

You just got an email from a co-worker in research. They want to do a medical test with anyone who is African American or had an "Up" for metformin. 

This table shows a partial result of African American patients and those with an “Up” for metformin. There are 20,059 results.
￼

<br>***Hospital stays less than average stay length***<br>
The Hospital Administrator wants to highlight some of the biggest success stories of the hospital. They are looking for opportunities when patients came into the hospital with an emergency (admission_type_id of 1) but stayed less than the average time in the hospital.

Partial result:
￼

**Action Item: investigate the story behind these successful hospital stays and find the causes of the stronger than average outcome.

Readmission Summary
Our boss has asked us to write a summary for the top 50 medication patients, break any ties with the number of lab procedures  (highest at the top). But they want a written summary of the format like this:
"Patient 2383 was Caucasian and was readmitted. They had 21 medications and 32 lab procedures."

<br> 
