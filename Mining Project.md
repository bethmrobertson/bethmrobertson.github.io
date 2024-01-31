# Mining Project (using Python)

**Project Description** <br>
For this project, I was assigned the role of a data analyst for a mining company. The company wants some information about their flotation process for beneficiation (cleaning and separation) of the iron ore. At the end of the process, they want to have iron ore that is of the quality that it can be smelted, and a small amount of silica concentrate, which is the undesired mineral in this process.

<img src="images/ext-froth-flotation.png.jpeg?raw=true" height = 200/>

**Project Summary**

- There are 24 parts of this continuous process that are monitored. Some are monitored every 20 seconds and some are monitored every hour.
-  Iron Concentrate and Silica Concentrate are the products of the phyical process.
-  % Iron Concentrate and % Silica Concentrate are actually values calculated by an on-site lab and later inserted into the data. They are not calculated during the process.
-  None of the measures captured were statistically significant with the % Iron Concentrate nor the % Silica Concentrate.
<br>
<br>
**The Data and the Process**
<br>
I used Pandas and Python to read the data from a .csv file. This dataset used the European format for decimal numbers, having a comma where in the U.S. we would expect to see a decimal point, so I added, decimal = ‘,’ to the read statement. The date had to be changed to a datetime value using pd.to_datetime, because, by default, Pandas reads dates as a string unless you tell it to parse the dates and give it a  format in your read statement. 

Here are all the columns in the dataset:

![Pasted Graphic 1](https://github.com/bethmrobertson/bethmrobertson.github.io/assets/144495411/03b60e72-ede5-4f80-8b94-ebb825221605)
<br>

<img src="images/NBA bubble pts assists rebounds.png?raw=true" height=500/>

Yet, **Embiid was the 2022-23 MVP**. Why?

**Embiid had the most average points per game** and had an excellent playoff run in addition to his stellar regular season. He was the runaway choice for MVP with 73 first-place votes to Nikola Jokic's 15 first place votes. The graph below shows average points per game instead of total. 
<br>
<img src="images/NBA Bubble avg ppg.png?raw=true" height=500/>￼

<br> ***Team Total Points*** <br>
The Scramento Kings scored the most points overall as a team in 2022-23. They made the playoffs but were knocked out by Golden State in the first round. The Kings also had five players with 1,000 points or more. Only two other teams had that same number. But, in the end, it matters in which games you score all those points! 

<img src="images/NBA team by season total points.png?raw=true" height=500/>￼
<br>
<img src="images/NBA players with more than 1000 pts.png?raw=true" height=500/>
<br>

<br>***Assists by Position***<br>
Which positions provide the most assists? **Point guards** lead the way in that category. But if you are listing leaders, you also have to include centers Jokic and Sabonis, who are assist machines.

<img src="images/NBA assists by position.png?raw=true" height=500/>
<br>

***Who shoots the most threes?***
<br>
If you want to know which positions shoot the most three pointers for each team, here's a table for you. This would make an excellent pocket card to keep nearby for every game!
<br>￼
<img src="images/NBA table plot 3 pt pct.png?raw=true" width=400/>
<br>
In 2022-23, teams had to watch out for Boston center, Al Horford (44.6%), and Memphis shooting guard, Luke Kennard (49.4%). They were the most accurate 3 point shooters in the league. In 2023-2024 so far, the Suns Grayson Allen is leading the way with 48.1% accuracy.

Stay tuned to this channel for the second part of my NBA study, in which I try to provide some answers to specific questions from the biggest NBA fan I know! Let me know what else **you** would like to know! 

I am looking for a full-time data analyst position, so if you know of an opportunity, please contact me. 

Thanks for reading!
