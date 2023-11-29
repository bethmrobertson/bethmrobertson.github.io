## Banking Grants and Loans Project

**Project Description** I was asked to look at data from the World Bank International Development Association (IDA) grants and loans program. This dataset contains historical information about loans and grants given by the IDA, including region of the world, country, purpose of the loan/grant, original amount given, the service charge rate, payments, and the amount still due. The dataset is live and is updated frequently. The data I used was from 2023-11-29. 

<img src="images/World Bank IDA logo.png?raw=true"/>

**The Big Reveal**
- Ukraine is the country that currently owes the most money to the IDA - over $1 billion.
- The South Asia region has the highest total amount currently due to the IDA - over $8.6 trillion.
- Some of the data is not tidy. The regions "Western and Central Africa" and "Eastern and Southern Africa" are in the dataset twice, once all capitalized and once as shown in this sentence.

**The Data**
I used SQL to extract and analyze data from [this dataset](https://finances.worldbank.org/Loans-and-Credits/IDA-Statement-Of-Credits-and-Grants-Historical-Dat/tdwh-3krx).
<br>  Some other interesting information about this dataset:
<br>  - The earliest date of a loan or grant in this dataset is 2011-04-30. (The IDA was founded in 1960. I wonder how they kept track of grants and loans before they set up this database.)
<br>  - The latest date in this data is 2023-10-31.
<br>  - 40% of the loans ever made are paid off.
<br>  - The IDA divides the world into 11 regions (given that the note above are caused by data entry errors.
<br>

**Collecting the Data**
The first thing I did was compare electricity costs between Houston and Elgin. It turns out that we are paying almost the exact same amount per kWh in both locations. So that wasn't a factor.

Next, I gathered our electricity usage info from the ComEd site and entered it into an Excel spreadsheet.
Then I pulled our personal temperature data, captured by our weather station and synced on the Ambient Weather Network. This left a gap in the temperature information of a few months when N lived there and we didn’t have the weather station. So I pulled temperature data from O’Hare airport (which is not too far away) through the NOAA Center for Environmental Information.
It turned out that getting all of the temperature information into Excel was going to be a tedious exercise since the timeframes from O’Hare and ComEd weren’t the same. So I changed to from Excel to Python to build the final dataset that contained all three inputs.

**Cleaning and Analyzing the Data**
I pulled the date and cost from the ComEd data, and the min, max, and mean of the O’Hare and Ambient temperature datasets. Once I fixed the names of the columns, I combined all three datasets by date using an outer merge in Python. Then, using Seaborn, I plotted a few different combinations until I settled on the average temperature vs. the average usage by day. This told me that the electricity usage was definitely tied to the temperature. But what about the other questions - did human or dog guests impact usage significantly?
I mapped dog symbols onto the graph to show where N had client dog boarding and letter symbols for when he had human guests (R is his sister, P is for parents).

**Conclusion**
The final conclusion was that the biggest factor for electricity usage was only the temperature. Human or dog guests didn’t raise the usage in any noticeable way. So at least we know!

**P.S.**
What about the question of the age of the system? We don’t know yet what impact that has on the costs. We know the current system is about 20 years old and only has one zone, so we suspect that a new system, with multiple zones, would be more efficient and might lower our electricity costs. But that’s a different project!!
