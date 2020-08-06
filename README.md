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

# Instructions to use to notebook :

Open the jupyter notebook

Step 1: Address search is a static field. Enter address of interest here to find covid prediction like below.
addressSearch = "9309 Kittansett Dr NC 28262"

Step 2: Now run all the cells and view results at the end which shows covid predictions for the next 10 days based on the address given.

Step 3: View your predicted results. Below is an result for the given address

Given address is:  9309 Kittansett Dr NC 28262
Your state is :  North Carolina
Todays covid active index based on your location is -  4062.0
Todays covid deaths index based on your location is -  50.0
You are in  Red Zone
The future 10 day active COVID predictions for ur location based on your state trend is:

![alt text](/Images/Images/prediction.PNG "Images") 

# Research Question: 

Although COVID-19 related data is available at the national, state, county or even city level, people are very interested in knowing what’s happening in their local area, around their neighborhood, the grocery store, the pharmacy, or retail store they typically go to, and whether the place they are thinking of going to is in a hotspot or not. That specific inquiry was the focus of our research and can be summed up in this question: When given a street address can you find the most recent (updated daily) death rate and confirmed cases in the surrounding area, show whether it’s a high risk area or not, and predict what those values will be for the next 10 days so as to decide whether to go to that specific location or not? 


# Relevant Domain Information:

https://www.weforum.org/agenda/2020/05/model-double-u-s-covid-19-death-forecast-restrictions/

https://www.nytimes.com/2020/05/04/us/coronavirus-live-updates.html

https://fox6now.com/2020/06/24/new-cdc-model-predicts-up-to-150000-american-covid-19-deaths-by-mid-july/

https://www.usnews.com/news/national-news/articles/2020-07-23/us-surpasses-4-million-coronavirus-cases-as-cdc-predicts-164-000-deaths-by-mid-august 

# Approach :

Exploratory Data Analysis, Supervised Learning(KNN Model), Time-series Analysis and Prediction(Arima Model)

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

Below scatter plot shows as red zone if the predicted confirmed cases are less than 95 per in a day.

![alt text](/Images/Images/scatter.PNG "Images") 

Below scatter plot shows as orange zone if the predicted confirmed cases are less than 75 per in a day.

![alt text](/Images/Images/scatter1.PNG "Images") 

Below scatter plot shows as green zone if the predicted confirmed cases are less than 55 per in a day.

![alt text](/Images/Images/scatter2.PNG "Images") 

## The MSE analysis for the model to figure out the perfect number of neighbours to get accurate results:

Creating a model by using K nearest neighbour algorithm to find the mean covid indexes for a given geographic location.

![alt text](/Images/Images/KNN.PNG "Images")

We have cleaned the county level dataset by filling the missing values and below are the visualizations based on active and death count with respect to county information:

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

## Linear Regression graph:

Below is the graph plotted for North Carolina state prediction of Covid cases.

![alt text](/Images/Images/scatter_init.PNG "Images")  

## Plot of balanced dataset :

Below is the plot showing active cases plot in Mecklenburg county in North Carolina.The graph changes accordingly based on the county and state information.

![alt text](/Images/Images/plot_active.PNG "Images")  


## AutoCorrelation and Partial AutoCorrelation plots:

We have taken p,d,q values from the autocorrelation and partial autocorrelation plots below.

![alt text](/Images/Images/correlation.PNG "Images")  
                       
# Date Preparation: 

## Handling Missing Values:

Covid Live API Dataset: Checked for null values and replaced with 0 for columns dead and recovered using fillna method.

County And State COVID Dataset:  Checked for null values and replaced with 0 for fips column.

Original dataset has some missing values in Lat,Long_ and Recovered which will be handled using fillna and if else looping techniques.
Converted date column from string to datetime column. 
In the dataset we have a cumulative sum for deaths and cases column. We transformed each row to its individual value.



# Machine Learning:

We used a classification method called K-nearest neighbor (KNN) algorithm to predict the impact of a virus given any geographical location based on its nearest neighbours as covid spreads more on contact and in a localized manner for current date. KNN is a classification technique which works when we have a set of data points and we know the correct class labels. We have given a range which varies from 1-50 and k-nearest value is picked randomly. By visualizing the graph MSE vs k-nearest value, we picked k-nearest value as 9 since it has the least MSE and high accuracy.
Linear regression is a linear approach to find the relationship between a dependent variable and one or more independent variables.Used Linear Regression technique to predict the death cases based on active cases at county level.Since, data has exponential relationship, linear regression didn’t give accurate results.
We have used Auto Regressive Integrated Moving Average (ARIMA) model which uses time series data to predict future data. Here,we have applied the arima model to our balanced dataset which resulted in future active cases count based on the existing data.We have predicted next 10 days active cases count of the county.The county information was extracted based on the geo location.


# Evaluation: 

Picking up the dynamic daily dump of COVID data based on geo location from www.trackcorona.live api and reading it into a data frame. This dataset contains lat, long, recovered, death as columns. 
Generated heat maps and scatter plots to visualize the relationship between geo location and covid concentration. We found covid high locations are highly clustered. We found covid index at a place based on localized data for the particular geo location.
Using KNN for predicting covid based on location by zoning the address. 
Picking up another dataset https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv in which we have county level data.This dataset consists of state name,county name,active (cummulative count),cummulative death count and date as columns.Used diff function and created an active_count column which is used for further analysis.
Generated autocorrelation and partial autocorrelation plots based on active_count column for the dataset to determine p,d and q for inputs to arima model.
Used the Arima model to predict the future dates covid-19 active cases based on the county information is taken from the address entered at the begining. 

 
# Known Issues:

One main problem that we found was that it is hard to accurately predict for a location based on county level data. If we had more narrowed down data, such as towns/cities or even household data, we could give more accurate results for the prediction. Having county level data made it difficult, because there is a big jump in the number of cases from county to county. For example, Mecklenburg county has over 20,000 cases but Cabarrus county only has a little over 2,000. Though, this is important information, because people travel from county to county or even state to state on a daily basis. 

# Enhancements: 

We would like to perform thorough cleanup of data like checking for outliers and removing columns which are not necessary for the model.

->Increase model’s efficiency by training model with more county data.

->Increase model efficiency by tuning the model for better accuracy.

->Finding more appropriate household/granular data for better predictions.

->We would like to create a UI and API for people to access the tool.


# Output:

## ARIMA model superimposed on the existing data to check its performance:

![alt text](/Images/Images/check.PNG "Images")  

## Final results of arima model displaying future dates data :

![alt text](/Images/Images/final.PNG "Images")  

# Conclusion: 

By performing EDA, we were able to get a better understanding of the datasets that we were working with. We were able to find the relationship between geo location and covid concentrations. Then based on location we were able to take an address and use KNN to predict covid cases. We also did time series predictions, to predict the future active cases at the address of interest, based on the trend in state. By completing all of this, we were able to see that there is a correlation between deaths and confirmed cases. Also, we were able to see what covid cases might be like for the next 10 days based on the location. We found that the number of active cases will continue to increase and decrease for Mecklenburg county. 
