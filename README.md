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

Although COVID-19 related data is available at the national, state, county or even city level, people are very interested in knowing what’s happening around their neighborhood, the grocery store, the pharmacy, or retail store they typically go to, and whether the place they are thinking of going to is in a viral hotspot or not.
That broader query can be broken out into three related questions: 

a)Given a street address can we find out the most recent (near real-time) death rate and confirmed cases in the surrounding area? 


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

![alt text](/Images/Images/heatmap.PNG "Images") 

Showing heat map as red zone if the predicted confirmed cases are less than 95 per in a day.

![alt text](/Images/Images/scatter.PNG "Images") 

Showing heat map as orange zone if the predicted confirmed cases are less than 75 per in a day.

![alt text](/Images/Images/scatter1.PNG "Images") 

Showing heat map as green zone if the predicted confirmed cases are less than 55 per in a day.

![alt text](/Images/Images/scatter2.PNG "Images") 

## The MSE analysis for the model to figure out the perfect number of neighbours to get accurate results:

![alt text](/Images/Images/KNN.PNG "Images")

## Visualization of Top 10 Counties Active COVID cases in USA
In the chart below, you can see that New York City is the county with the highest number of active cases, over 200,000. 

![alt text](/Images/Images/active1.PNG "Images") 

## Visualization of Top 10 Counties Death cases of COVID in USA
Once again, New York City is the top county in the United States for the death count. 

![alt text](/Images/Images/death1.PNG "Images")  

## Visualization of Top 10 Counties Active COVID cases in North Carolina:
In the state of North Carolina, Mecklenburg county is the worst county for the number of active covid cases. Mecklenburg county has a little over 20,000 cases. 

![alt text](/Images/Images/Active-N.PNG "Images")  

## Visualization of Top 10 Countries Death cases of COVID in North Carolina:
Then again, Mecklenburg county is the top county in North Carolina for covid related death count. We saw before that death count and confirmed cases are correlated. These two graphs of active cases and death count, show this as well. 
 
![alt text](/Images/Images/death-N.PNG "Images")  

## Plot of balanced dataset :

![alt text](/Images/Images/plot_active.PNG "Images")  


## AutoCorrelation and Partial AutoCorrelation plots:

![alt text](/Images/Images/correlation.PNG "Images")  
                       
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
