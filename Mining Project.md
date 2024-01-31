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
I used Pandas and Python to read the data from a .csv file. This dataset used the European format for decimal numbers, having a comma where in the U.S. we would expect to see a decimal point, so I added, decimal = ‘,’ to the read statement. The date had to be changed to a datetime value using pd.to_datetime, because, by default, Pandas reads dates as a string unless you tell it to parse the dates and give it a format in your read statement. 

Here are all the columns in the dataset:

![Pasted Graphic 1](https://github.com/bethmrobertson/bethmrobertson.github.io/assets/144495411/03b60e72-ede5-4f80-8b94-ebb825221605)
<br>

I used the **.shape property** and the **.describe() method** to learn more about the dataset. Then I started reading about the actual process to understand more about where the data comes from and the business goal. (See references below.) 

Some of the measurements in the dataset are taken every twenty seconds and some every hour, which, to me, makes it difficult to really understand what is happening. **% Iron Concentrate and % Silica Concentrate are actually values calculated by an on-site lab** and later inserted into the data. They are not calculated during the process. 
<br>￼

<br> ***More Research*** <br>
Once I read more information about the process, I became interested in what this dataset was originally intended to do. It turns out that what the plant hopes to do is actually predict the % Iron Concentrate and the % Silica Concentrate ahead of time instead of waiting for measurements from the lab. According to a ‘mineral processing engineer and amateur data scientist’ in the comments section for this dataset, here is a description of these two variables[^1]:

>% Iron Concentrate, % Silica Concentrate = These are our product. Concentrate goes to the blast furnaces after enrichment. Metallurgists demand certain concentration grades from us for smelting. If the demanded value is not achieved, the quality of the metallurgical process decreases. Our main goal is to achieve these values in concentrate. Generally, these values for iron reverse cationic flotation are:
                Fe = 67% 68%
                SiO2 = 1.6% -1.7%
<br>

<br>***Describe for % Iron Concentrate and % Silica Concentrate***<br>
I ran **.describe()** so I could see just the values for the intended products, % Iron Concentrate and % Silica Concentrate.

![65 05006799](https://github.com/bethmrobertson/bethmrobertson.github.io/assets/144495411/0b390194-d317-4be2-a62b-f4b871a824ed)

Our dataset summary:
<br>
<img width="646" alt="Concentrato" src="https://github.com/bethmrobertson/bethmrobertson.github.io/assets/144495411/1d849f26-ed69-4bba-840c-18a93dd73e47">
<br>
Therefore, according to our ‘expert’, this mine is actually not producing in the way it should be producing.
<br>￼
<br>***Correlation***<br>

I used the correlation method, **.corr()**, to see what the correlation was between the variables for a date given by the plant manager. There was very little correlation between any of the variables. 

<img width="237" alt="CORRELATION TABLE" src="https://github.com/bethmrobertson/bethmrobertson.github.io/assets/144495411/5595afc1-1672-4aec-a1de-b7752665c797">

Also, according to our 'expert', there are actually more data that are needed to be able to use machine learning to predict the % concentrates at the end, including:
* Feeding tons
* Plant flow chart (is there an enrichment unit before flotation? Usually magnetic separator for Fe)
* Grinding parameters
* Concentrate tons
* Ph regulator.
* Tailing grades
* Tailing tons

***Conclusion***

In this project, I looked at data from a mining operation. I got to practice some **Python skills** and also learned some information about iron ore processing. It was interesting to read about the processes and to learn from actual metallurgical engineers. Even though I couldn’t accurately predict % Iron Concentrate or % Silica Concentrate with this data, the project was valuable.

Please get in touch with any questions you have. I am looking for a full-time data analyst position and would love to connect with anyone who has a position open or who knows of one.

Thanks for reading!
<br>
***References*** 
[Froth Flotation and Its Application to Concentration of Low Grade Iron Ores](https://core.ac.uk/download/pdf/297714789.pdf)
<br>
[An Overview of the Beneficiation of Iron Ores via Reverse Cationic Flotation](https://www.sciencedirect.com/science/article/abs/pii/S0301751614000155)

[^1]: [Discussion of the original dataset on Kaggle](https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process/discussion/182482)

