# Hiring-Process-Analytics

- [Project Description](#project-description)
- [Problem](#problem)
- [Approach](#approach)
- [Dataset](#dataset)
- [Data Cleaning](#data-cleaning)
- [Finding Outliers](#finding-outliers)
    - [IQR (Interquartile Range) Method](#iqr-interquartile-range-method)
- [Insights](#insights)
    - [Hiring Analysis](#hiring-analysis)
    - [Salary Analysis](#salary-analysis)
    - [Salary Distribution](#salary-distribution)
    - [Departmental Analysis](#departmental-analysis)
    - [Position Tier Analysis](#position-tier-analysis)
- [Conclusion](#conclusion)


### Project Description
<p>In this project, as a data analyst at Google, the goal is to leverage the available hiring process data to extract valuable insights that can lead to improvements in the company's hiring procedures. The hiring process is a crucial aspect of maintaining a talented workforce, and understanding trends within this process can significantly impact its efficiency and effectiveness. By thoroughly analyzing historical hiring data, we aim to identify patterns, pain points, and areas of opportunity that will guide the hiring department in making informed decisions.
</p>

### Problem
<p>The primary objective of this project is to optimize Google's hiring process by addressing the following key challenges:
</p>
<ol>
  <li>Hiring Analysis</li>
  <li>Salary Analysis</li>
  <li>Salary Distribution</li>
  <li>Departmental Analysis
</li>
  <li>Position Tier Analysis</li>
</ol>

### Approach
<p>For the given dataset of a company where the details about people who registered for a particular post in a department of this company. I used the knowledge in statistics and different formulas in excel and drew necessary conclusions about the company.</p>

### Dataset

[Raw Dataset](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=0)
<br>

### Data Cleaning
<p>Before proceeding to get the insights, in order to get the correct insights the 1st step is data cleaning.</p>

[Cleaned Dataset](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=649437829)
<br>
<p>Remove duplicates, handle missing values, and ensure data consistency.
These are the some changes I did in the dataset.
</p>
<ul>
  <li>Event_type → “-” to “Don’t want to say"</li>
  <br>
  <p><i>Reason : </i>Replacing the "-" values with "Don’t want to say" in the "event_name" column is a valid approach, because I believe that the "-" values are intended to represent instances where individuals chose not to disclose their gender. This replacement will help make the data more coherent and meaningful, allowing you to analyze and interpret it more accurately.</p>
  <li>Post name → “-” to "Not specified”
</li>
  <li>Salary → 47734.63
</li>
  <br>
  <p><i>Reason :</i> As the dataset includes job types, so calculating the average salary for each job type and imputing  the missing salary based on the job type of the particular row.</p>
</ul>

### Finding Outliers
<p>Finding outliers in a dataset involves identifying data points that are significantly different from the rest of the data. Outliers can distort statistical analyses and models, so it's important to detect and handle them appropriately. 
</p>

#### IQR (Interquartile Range) Method
<p>Calculate the IQR, which is the range between the first quartile (25th percentile) and the third quartile (75th percentile). Data points that fall below <b>Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR</b> are potential outliers.
</p>
Outlier  → in salary column → 200000
<p>Hence i found only 1 oulier it is better to keep as is it is in dataset for the analysis.</p>

### Insights
#### Hiring Analysis
<p>I have conducted an analysis to understand the gender distribution within the hiring process. The dataset revealed that a total of <b>2563 males and 1856 females</b> were hired across different positions and departments within the company. This analysis provides valuable insights into the company's efforts to maintain a diverse workforce. The visualization below displays the distribution of hires based on gender.</p>

[click here to see Analysis](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=269852243)

<br>

![1 1](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/294db206-cb7d-4c4c-83fb-1d9d6d1f164a)

<br>

![1 2](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/06721595-d48c-45ae-a4f1-cd1c8e7f640f)

#### Salary Analysis
<p>Turning our attention to the financial aspect of the hiring process, I analyzed the offered salaries across various positions and departments within the company. The data revealed an <b>important metric:</b> the <b>average salary </b>offered by the company is approximately <b> $49,982.72.</b> This figure serves as a valuable benchmark, reflecting the company's compensation practices and the value placed on attracting top-tier talent.
</p>

<p>Understanding the average salary provides a foundation for further investigation into potential variations based on factors such as position, department, or experience level. This analysis underscores the company's commitment to competitive compensation and fair hiring practices. By delving deeper into the nuances of salary distribution, we can gain insights that contribute to both internal decision-making and external perceptions of the company's employment offerings.
</p>

[click here to see Analysis](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=930750584)

<br>

![2](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/7365cde0-9784-44ed-b51d-63db700ed11d)

<br>

#### Salary Distribution
<p>Creating class intervals for salary distribution is a crucial step in understanding the distribution patterns of offered salaries within the company. Class intervals help organize the salary data into meaningful ranges, making it easier to visualize and analyze the distribution. </p>

<p>Here's how the approach for creating class intervals:</p>
<ol>
  <li><i>Determine Data Range:</i></li>
    
 ![3 1](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/797135ad-a48a-4a80-a32d-a57c48d9c4d2)

  <li><i>Decide on Number of Intervals:</i> 10
</li>
  <li><i>Calculate Interval Width:</i> by dividing the range of salaries by the chosen number of intervals i.e.,39990
</li>
  <li><i>Create Intervals:</i> Start with the minimum salary as the starting point for the first interval. Then, add the interval width to create subsequent intervals.
</li>
  <li><i>Present Intervals:</i></li>
  
![3 2](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/72640995-e875-4da9-be8f-a842c13462fb)

</ol>

[click here to see the Analysis](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=1563834555)

#### Departmental Analysis
<p>By conducting a thorough examination of the workforce distribution across departments, I uncovered valuable insights that shed light on the company's organizational structure. Notably, our analysis reveals that the <b>Operations Department</b> boasts the highest representation, with a significant <b>39.2%</b> of the total workforce.
</p>

![4](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/cd2c0bc2-09f4-4872-a7cc-c2acb8402bea)

<br>

[click here to see the Analysis](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=586570988)

#### Position Tier Analysis
<p>The different position tiers within the company, This will help us to understand the distribution of positions across different tiers.</p>

![5 1](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/f33bf35a-8aa7-4d1b-b336-0dbc64d1629c)

<br>

![5 2](https://github.com/SushmaRaasi/Hiring-Process-Analytics/assets/79751402/adaa4997-150f-4a30-b200-4ecc1ddfa0fc)

<br>

[click here to see the Analysis](https://docs.google.com/spreadsheets/d/1UwhgNZaB-htAHYSA_ethlQzCJArCw6c6Lt6QiWyL3vk/edit#gid=1099816181)

### Conclusion
<p>I learned EXCEL and descriptive Statistics, new terms and methods and many of the new functions. Getting proper insights from the problem statement solving real-world problems. All the concepts have helped me get a deep insight into the problem statement.
This project has helped me to gain confidence in analyzing a problem and eventually to learn the practical use of the concepts taught in the training.</p>
