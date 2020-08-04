## Team Members: 
1. Sai Supriya Chinthakuntla

2. Philip Thomas

3. Ganesh Vishwanathan 

4. Sucharita Mullapudi

5. Hailey Brown

# Project Introduction: 
CoronaVirus is an illness caused by a virus. Symptoms of this virus vary from mild to moderate respiratory illness. The virus is called COVID-19 and has spread from person to person. Older people, and those with underlying medical problems like cardiovascular disease, diabetes, chronic respiratory disease, and cancer are more likely to develop serious illness. At this time, there are no specific vaccines or treatments for COVID-19. However, there are many ongoing clinical trials evaluating potential treatments. Pandemic is spreading all over the world and it’s very important to understand about the spread.
In this project, we are going to analyze accumulated data of confirmed deaths and recovered cases.

# Data Sources and Datasets:
Link to the live API: https://www.trackcorona.live/api in which data is updated for every 20mins.
Link to the county level dataset of USA : https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv


# Technologies Used:

1)Python (Programming Language)

2)Jupyter Notebook(IDE)

3)Libraries used in python :

a)Pandas

b)Matplotlib

c)Numpy

d)Scikit-learn 

e)seaborn

f)sklearn

g)json

h)requests

i)statsmodels

# Research Question: 
What is the ability to predict the count of future active cases and the number of reported cases in particular location, based on address provided in the USA?


# Relevant Domain Information:
https://www.weforum.org/agenda/2020/05/model-double-u-s-covid-19-death-forecast-restrictions/

https://www.nytimes.com/2020/05/04/us/coronavirus-live-updates.html

https://fox6now.com/2020/06/24/new-cdc-model-predicts-up-to-150000-american-covid-19-deaths-by-mid-july/

https://www.usnews.com/news/national-news/articles/2020-07-23/us-surpasses-4-million-coronavirus-cases-as-cdc-predicts-164-000-deaths-by-mid-august 

# Approach :

# Methods Used:

1)Exploratory Data Analysis
2)Data Preprocessing
3)Machine Learning
4)Predictive Modeling
5)Linear regression
6)KNeighborsRegression
7)ARIMA Model

# Data understanding and EDA:

We collected and cleaned a live global dataset of COVID19.
Visualization of confirmed, dead and  recovered cases all over the world as of today. Using live API for today’s dataset.
Also based on the address given we bin the location into Red, Yellow and green zones. This can be specifically helpful for people to understand their level of isolation required to be safe.
Performing a heat map to find the correlation between various columns here we find active and dead are related to recovered which makes logical sense.

# Visualization of Top 10 Countries Confirmed COVID cases

![alt text](/Images/Confim.PNG "Images") 

# Visualization of Top 10 Countries Active COVID cases

![alt text](/Images/Active.PNG "Images")  

# Visualization of Top 10 Countries Death Count COVID cases
 
![alt text](/Images/death_rate.PNG "Images")  
                       
# Date Preparation: 
## Handling Missing Values:

Dataset1:(Confirmed_cases)
Original dataset has Province/State column as it is not required for further analysis; we have removed that column.

Dataset2:(Death_cases)
Original dataset has Province/State column as it is not required for further analysis; we have removed that column.

Dataset3:(Global_Death)
Original dataset has People_Tested,People_Hospitalized,UID,ISO3 and Mortality_Rate columns as it is not required for further analysis; we have removed that column.
Original dataset has some missing values in Lat,Long_ and Recovered which will be handled using fillna and if else looping techniques.

# Machine Learning: 
We are assuming we can use Supervised Learning and Linear Regression techniques to predict the model. 

# Evaluation: 
In Progress
 
# Known Issues
(problems with predictors, reporting, bias, etc.) - this will develop over time : Will update further
 
# Conclusion: 
Not yet concluded
