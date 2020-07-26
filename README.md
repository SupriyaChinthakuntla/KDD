## Team Members: 
1. Sai Supriya Chinthakuntla

2. Philip Thomas

3. Ganesh Vishwanathan 

4. Sucharita Mullapudi

5. Hailey Brown

# Project Introduction: 
CoronaVirus is an illness caused by a virus. Symptoms of this virus vary from mild to moderate respiratory illness. The virus is called COVID-19 and has spread from person to person. Older people, and those with underlying medical problems like cardiovascular disease, diabetes, chronic respiratory disease, and cancer are more likely to develop serious illness. At this time, there are no specific vaccines or treatments for COVID-19. However, there are many ongoing clinical trials evaluating potential treatments. Pandemic is spreading all over the world and it’s very important to understand about the spread.
In this project, we are going to analyze accumulated data of confirmed deaths and recovered cases.

# Data Sources:
Link to the dataset: https://github.com/CSSEGISandData/COVID-19
This is the data repository for the 2019 Novel Coronavirus Visual Dashboard operated by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE). Also, Supported by ESRI Living Atlas Team and the Johns Hopkins University Applied Physics Lab (JHU APL)

# Dataset:
time_series_covid19_confirmed_global.csv
https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv

time_series_covid19_deaths_global
https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv

Global Data
https://raw.githubusercontent.com/CSSEGISandData/COVID-19/web-data/data/cases_country.csv

# Technologies Used:

1)python

2)pandas, jupyter

3)Matplotlib

4)Numpy

5)Scikit-learn 

# Research Question: 
Going to predict the death rate of one country for the next week based on the available data.

# Relevant Domain Information:
https://www.weforum.org/agenda/2020/05/model-double-u-s-covid-19-death-forecast-restrictions/

https://www.nytimes.com/2020/05/04/us/coronavirus-live-updates.html

https://fox6now.com/2020/06/24/new-cdc-model-predicts-up-to-150000-american-covid-19-deaths-by-mid-july/

https://www.usnews.com/news/national-news/articles/2020-07-23/us-surpasses-4-million-coronavirus-cases-as-cdc-predicts-164-000-deaths-by-mid-august 

# Approach :
# Data understanding and EDA:

We collected and cleaned the Global Data set on COVID-19 data.  
Below are the basic EDA on Data set
# Visualization of Top 10 Countries Confirmed COVID cases

![alt text](/Images/Confirm.png "Images") 

# Visualization of Top 10 Countries Active COVID cases

![alt text](/Images/Active.png "Images")  

# Visualization of Top 10 Countries Death Count COVID cases
 
![alt text](/Images/death_rate.png "Images")  
                       
# Date Preparation: 
# Handling Missing Values:

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
