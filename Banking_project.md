## Banking Grants and Loans Project

**Project Description** I was asked to look at data from the World Bank International Development Association (IDA) grants and loans program. This dataset contains historical information about loans and grants given by the IDA, including region of the world, country, purpose of the loan/grant, original amount given, the service charge rate, payments, and the amount still due. The dataset is live and is updated frequently. The data I used was from 2023-11-29. 

<img src="images/World Bank IDA logo.png?raw=true"/>

**The Big Reveal**
- Ukraine is the country that currently owes the most money to the IDA - over $1 billion.
- The South Asia region has the highest total amount currently due to the IDA - over $8.6 trillion.
- Some of the data is not tidy. The regions "Western and Central Africa" and "Eastern and Southern Africa" are in the dataset twice, once all capitalized and once as shown in this sentence.

**The Data**
<br>
I used SQL to extract and analyze data from [this dataset](https://finances.worldbank.org/Loans-and-Credits/IDA-Statement-Of-Credits-and-Grants-Historical-Dat/tdwh-3krx).
<br>  
**Some other interesting information about this dataset**
<br>  - The earliest date of a loan or grant in this dataset is 2011-04-30. (The IDA was founded in 1960. I wonder how they kept track of grants and loans before they set up this database.)
<br>  - The latest date in this data is 2023-10-31.
<br>  - 40% of the loans ever made are paid off.
<br>  - The IDA divides the world into 11 regions (given that the errors noted above are caused by data entry errors).
<br>  <img src="images/DAA Bank regions.png?raw=true"/>


