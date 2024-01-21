# NBA 2022-23 Season Project - Part I (using Tableau)

**Project Description** <br>
I have a friend who spends a lot of time with the NBA (by his own admission). So I was very interested to ‘nothing but net’ this NBA project and share it with him.

I used NBA data from basketball-reference.com to gather some insights into the 2022-23 season. This is Part I of my analysis. Part II is coming soon!

<img src="images/Black & White Modern Basketball LinkedIn Banner.png?raw=true" height = 200/>

**Project Summary and Action Items**
- 
<br>
- Joel Embiid was the player with the highest number of MVP votes. Why?
- 
<br>
**Questions and Insights**
<br>
<br>
***Total Points, Assists, and Rebounds by Position*** <br>
A Bubble plot allows us to see lots of information at once. I used total points and total assists as the X and Y axes, respectively. The size of the bubble represents rebounds and the color of the bubble show the player's position. Jayson Tatum had the most total points. He had more assists than Joel Embiid but Embiid had more rebounds (670 vs. 649).
<br>

<img src="images/NBA bubble pts assists rebounds.png?raw=true" height=400/>

Yet, **Embiid was the 2022-23 MVP**. Why?

**Embiid had the most average points per game** and had an excellent playoff run in addition to his stellar regular season. He was the runaway choice for MVP with 73 first-place votes to Nikola Jokic's 15 first place votes. The graph below shows average points per game instead of total. 
<br>
<img src="images/NBA Bubble avg ppg.png?raw=true" height=400/>￼

<br> ***Team Total Points*** <br>
The Scramento Kings scored the most points overall as a team in 2022-23. They made the playoffs but were knocked out by Golden State in the first round. The Kings also had the most players with 1,000 points or more. But, in the end, it matters in which games you score all those points! 

<img src="images/NBA team by season total points.png?raw=true" height=500/>￼
<br>
<img src="images/NBA players with more than 1000 pts.png?raw=true" height=400/>
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
