# Code for the Hospital Data Analysis Project using MySQL

**Project Description** <br>
This page shows the code I used for the different steps of this project.

***Number of Days*** 
<br>
I used a bar chart to show the number of patients who stayed a certain number of days to understand if most patients in the study stayed fewer than 7 days in the hospital.
<br>
<img src="images/Code Days of stay.png?raw=true" height=300/>￼

<br> ***Specialities*** <br>
To answer the question of which specialities are performing the most procedures, on average, I created a table. I limited the data to show an average of 2.5 procedures per visit per patient, with at least 50 patients. 

<img src="images/Code Specialties with largest avg number of procedures.png?raw=true" height=300/>￼
<br>
<br>***Lab procedures by race***<br>
I found out the the number of lab procedures doesn't not vary significantly by race. I grouped by race and ordered by the count of the average number of lab procedures.
<br>
<img src="images/Code Lab procs by race.png?raw=true" height=300/>

<br>***Average length of stay related to number of lab procedures***
A 'Case When' statement allowed me to group the number of lab procedures into Many (>66),￼ Average (33 - 66), and Few (<33) groups and then to look at days of stay for each of those groups.
<br>
<img src="images/Code Stay time vs number of lab procedures.png?raw=true" height=300/>
<br>

<br>***Up for Metformin***<br>
I was able to create a list of patient numbers that have a race of African American or a result of "Up" for Metformin by joining the Health and Demographics tables.
<br>
<img src="images/Code African American or Up for Metformin.png?raw=true" height=200/>

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
