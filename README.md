# Data Analysis using Excel, SQL and Power Bi

![Dashboard for top UK Youtubers 2024](https://github.com/bollasrikanth48/Top_uk_youtubers/blob/main/Assets/images/powerbi.jpg)
# Table of Contents
-  [Objective](#Objective)
-  [Data_Source](#Data Source)
-  [Steps_involved](#Steps involved)
-  [Development_using_SQL](#Development using SQL)
  - [Data_Exploration](##Data Exploration)
  - [Data_Cleaning](##Data Cleaning)
  - [Create_SQL_view](##Create SQL view)
-  [Testing](#Testing)
-  [Visualization](#Visualization)
  - [Dax_Measures](##Dax Measures)
  - [Results](##Results)
-  [Findings](#Findings)
-  [Recomendation](#Recomendation)
-  [Conclusion](#Conclusion)


# Objective
The Content Strategist wants to identify the most influential YouTube channels in the travel and lifestyle niche to decide which creators would be most impactful for sponsorships and collaborations in 2024.

### Problem Statement
To develop a dashboard that provides actionable insights into the top travel and lifestyle YouTubers of 2024, including their:

1. Subscriber count
2. Total views
3. Video upload frequency
3. Engagement metrics (likes, comments, shares)

This dashboard will empower the content strategy team to make data-driven decisions about partnerships that align with the company’s branding and audience goals.

# Data Source
Data is sourced from kaggle: (#https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download)

# Steps involved
1. Development using SQL
2. Testing
3. Visualization using Power Bi
# Development using SQL
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
## Data Exploration
Dataset contains Top 100 youtubers based on the subscribers count in United Kingdom in 2024
SQL queries are used to explore the data and following is the code used
''' sql
SELECT TOP (1000) [Column_1]
      ,[NOMBRE]
      ,[SEGUIDORES]
      ,[TP]
      ,[PAÍS]
      ,[TEMA_DE_INFLUENCIA]
      ,[ALCANCE_POTENCIAL]
      ,[GUARDAR]
      ,[INVITAR_A_LA_CAMPAÑA]
      ,[channel_name]
      ,[total_subscribers]
      ,[total_views]
      ,[total_videos]
      ,[column14]
  FROM [youtube_db].[dbo].[youtube_data_new]
'''

## Data Cleaning
## Create SQL view
# Testing
# Visualization  using Power Bi
## Dax Measures
## Results
# Findings
# Recomendation
#Conclusion





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

