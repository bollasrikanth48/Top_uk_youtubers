# Data Analysis using Excel, SQL and Power Bi

<div align="center">
  <img src="Assets/images/powerbi.jpg" alt="Dashboard for top UK Youtubers 2024" style="max-width: 100%; height: auto;">
  <p><strong>Dashboard for top UK Youtubers 2024</strong></p>
</div>



# Table of Contents
-  [Objective](#Objective)
-  [Data_Source](#Data_Source)
-  [Steps_involved](#Steps_involved)
-  [Development_using_SQL](#Development_using_SQL)
  - [Data_Exploration](##Data_Exploration)
  - [Data_Cleaning](##Data_Cleaning)
  - [Create_SQL_view](##Create_SQL_view)
-  [Testing](#Testing)
-  [Visualization](#Visualization)
  - [Dax_Measures](##Dax_Measures)
  - [Results](##Results)
-  [Findings](#Findings)
-  [Recomendation](#Recomendation)
-  [Conclusion](#Conclusion)


# Objective
The Content Strategist wants to identify the most influential YouTube channels in the travel and lifestyle niche to decide which creators would be most impactful for sponsorships and collaborations in 2024.

### Problem Statement

who is the most reliable YouTuber for a company to invest in for effective marketing campaigns?

# Data_Source
Data is sourced from kaggle: (#https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download)

# Steps_involved
1. Development using SQL
2. Testing
3. Visualization using Power Bi
# Development_using_SQL
General approach used as follows
1. Get the data
2. Explore the data in Excel
3. Load the data into SQL Server
4. Clean the data with SQL
5. Test the data with SQL and Excel
6. Visualize the data in Power BI
7. Generate the findings based on the insights
8. Write the documentation + commentary
9. Publish the data to GitHub Pages
## Data_Exploration
Dataset contains Top 100 youtubers based on the subscribers count in United Kingdom in 2024
SQL queries are used to explore the data and following is the code used

![Display all columns using SQL](Assets/images/data.png)

Data consists of 13 columns and 100 rows 
required columns are channel_name, total_subscribers, total_views, total_videos

## Data Output

![Data Output](Assets/images/data output.png)


## Data_Cleaning

Channel name included name@channel id, data is cleaned in sql to extract only channel id

## Data Cleaning

![Data Cleaning](Assets/images/data cleaning.png)

## Create_SQL_view
Feature engineering is done by selecting only selected columns and created a SQL view to connect it with PowerBi


## SQL View

![SQL View](Assets/images/create view.png)


# Testing

following are the data quality checks conducted
- Row count check
- Column count check
- Data Type check
- Duplicate count check


# Visualization _using_PowerBi
## Dax_Measures

# DAX Measures

### 1. Total Subscribers (M)


```dax
Total Subscribers (M) =
VAR million = 1000000
VAR sumOfSubscribers = SUM(view_uk_youtubers_2024[total_subscribers])
VAR totalSubscribers = DIVIDE(sumOfSubscribers, million)

RETURN totalSubscribers



## Results
# Findings
# Recomendation
# Conclusion





'''sql
CREATE VIEW view_uk_youtubers_2024 AS

SELECT 
	CAST(SUBSTRING(NOMBRE, 1, CHARINDEX('@', NOMBRE) -1) AS VARCHAR(100)) AS channel_name,
	total_subscribers,
	total_views,
	total_videos
FROM
	youtube_data_new
'''

