# Covid_19-Analysis-Visualization-Tableau

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

This dashboard helps to understand the Cases, Recoveries and Death in Different countries. It helps to know which country is highly affected with covid-19 cases and which country is less affected. Through different visuals, we get to know the relation between the death and active cases, recovered and active cases, death and recovery, population and active cases of top highly affected countries. It also lets us know the month in which covid-19 cases is in peak and in downfall and also we let know in which upcoming month the cases is going to be in peak so that we can take precautions and work effectively, thus since by using this dashboard we have identified this problem, we can further work on handling the covid-19 cases.


### Steps followed 
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

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;






