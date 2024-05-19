# Covid_19-Analysis-Visualization-Tableau

### Dashboard Link : https://public.tableau.com/app/profile/vaibhav.kumar5478/viz/CovidDashboard1_17157104641410/Dashboard5

## Problem Statement

This dashboard helps to understand the Cases, Recoveries and Death in Different countries. It helps to know which country is highly affected with covid-19 cases and which country is less affected. Through different visuals, we get to know the relation between the death and active cases, recovered and active cases, death and recovery, population and active cases of top highly affected countries. It also lets us know the month in which covid-19 cases is in peak and in downfall and also we let know in which upcoming month the cases is going to be in peak so that we can take precautions and work effectively, thus since by using this dashboard we have identified this problem, we can further work on handling the covid-19 cases.


### Steps Followed 
- Step 1 : Download the dataset from kaggle.
- Step 2 : Perform Data Cleaning, Modification using Jupyter.
- Step 3 : Use Panda Library by Python Code for data cleaning.
- Step 4 : Open Tableau Public Dekstop and Select the cleaned Dataset of Covid-19.
- Step 5 : Drag and make the Relationship between different cleaned csv files of covid-19 by making common field among them.
- Step 6 : Since by default, profile will be opened only for 100 rows.
- Step 7 : Now using the data make the different visuals using bar chart, area chart, scatter plot, line chart, etc.
- Step 8 : Use the Categories - Death, Active, Recovery for making interactive Dashboards.
- Step 9 : Filters the countries to top 10 and bottom 10 for better View and understand.
- Step 10 : Now using these worksheets make the interactive Dashboards.
           
          
### NOTE :-
In our dataset:
- Some Missing Data were assigned text "Missing" and in numeric columns were assigned value 0.
- Date column converted to standard date system.

### FILES :-
- country_wise_latest
- covid_19_clean_complete
- day_wise
- full_grouped
- usa_county_wise
- worldometer_data

## Codes used for Cleaning the files:-

# 1. covid_19_clean_complete

import pandas as pd
df = pd.read_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\covid_19_clean_complete.csv")
dt = df.dtypes
nv = df.isnull().sum()
print(df)
print("# Data Types")
print(dt)
print("# Null Values")
print(nv)
print("# info")
print(df.info())
print("# Describe")
print(df.describe())
df.fillna("Missing",inplace= True)
print("# first 5 rows")
print(df.head())
print("# last 5 rows")
print(df.tail())
print("# Duplicate Values")
print(df.duplicated)
print("# column duplicated")
df.to_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\covid_19_clean_complete.csv",index=False)

![Screenshot 2024-05-19 172608](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/30d7964c-a9c6-4ee1-b9db-4ec7d7ee9362)

# 2. usa_county_wise

import pandas as pd
df = pd.read_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\usa_county_wise.csv")
dt = df.dtypes
nv = df.isnull().sum()
print(df)
print("# Data Types")
print(dt)
print("# Null Values")
print(nv)
print("# info")
print(df.info())
print("# Describe")
print(df.describe())
df.fillna("Missing",inplace= True)
print("# first 5 rows")
print(df.head())
print("# last 5 rows")
print(df.tail())
print(df)
df.to_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\usa_county_wise.csv",index=False)

![Screenshot 2024-05-19 172759](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/727649d8-6ccc-473c-b160-7440d853fc33)

# 3. worldometer_data

import pandas as pd
df = pd.read_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\worldometer_data.csv")
dt = df.dtypes
nv = df.isnull().sum()
print(df)
print("# Data Types")
print(dt)
print("# Null Values")
print(nv)
print("# info")
print(df.info())
print("# Describe")
print(df.describe())
df.fillna("Missing",inplace= True)
print("# first 5 rows")
print(df.head())
print("# last 5 rows")
print(df.tail())
print(df.fillna(0,inplace=True))
df["WHO Region"].replace(0,"Missing",inplace=True)
print(df.tail())
df.to_csv("C:\\Users\\vaibh\\OneDrive\\Desktop\\DSEU\\covid\\worldometer_data.csv",index=False)

![Screenshot 2024-05-19 172859](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/fa3bacb7-4307-42d6-b899-68043236c889)

# Snapshot of Dashboard (Tableau_Public)

# 1. Death 

 ![Screenshot (692)](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/31f4d000-b572-4c89-8b10-59a7409147a7)

# 2. Active
 
 ![Screenshot (691)](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/a3d923fb-c71c-4687-89a6-43f2655558db)

# 3. Recovery

![Screenshot (690)](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/88530e48-e3aa-423a-8b85-c72dd19bc2f3)

# 4. Miscellaneous

![Screenshot (693)](https://github.com/Vaib2004/Covid_19---Analysis---Visualization---Tableau/assets/169991554/598540a7-e9cc-4513-829e-376754dea2b5)

# N0TE: In Visuals only Top and Bottom countries are Focused.

# INSIGHTS 

A single page report was created on Tableau Public Desktop & it was then published to tableau Service.
Following inferences can be drawn from the dashboards;

- According to Analysis:
   + Highest Active Cases was in the month of June and Least Active Cases in the monnth of january.
   + highest recovery is in the month of june.
   + April is the month in which there is the highest number of death rate.
- According to Analytics:
   + Highest active cases will be in the month of september.
   + Recovery rate in upcoming months is in stable.
   + Death rate in upcoming months is in stable.
- US is the country having highest number of cases
   + Total No. of cases: 28,16,444.
- India is on the 3rd number having highest number of active cases
   + Total number of cases: 4,95,499
- Country with Highest Recovery Rate is Brazil
   + Average Recovery: 18,46,641
- India is on the 3rd number in recovery rate.
   + Average Recovery: 9,51,166
- Brazil is the country in which recovery rate is high in compare to cases
   + Cases: 3000k
   + Recovered: 2200k
- US is the country having highest death rate in the world
   + Total death - 1,48,011
- India is on the 6th number in death rate
   + Total death - 33,408
- According to Active Cases there is highest deaths in the Brazil Country
   + Active - 508,116
   + Death - 87,618
- In the month of july there is a highest no. of cases and there is highest no. of recovery also.
- Countries in which people are dying more instead of recovery : France, Italy, Mexico, Spain, UK, US.
- Countries in which people are recovering more instead of death: Brazil, India, Iran, Peru.
  






