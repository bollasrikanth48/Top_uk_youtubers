# Data Analysis using Excel, SQL and Power Bi

![Dashboard for top UK Youtubers 2024](https://github.com/bollasrikanth48/Top_uk_youtubers/blob/main/Assets/images/powerbi.jpg)
# Table of Contents
-  [Objective](#Objective)
-  [Data Source](#Data Source)
-  [Steps involved](#Steps involved)
-  [Development using SQL](#Development using SQL)
  - [Data Exploration](#Data Exploration)
  - [Data Cleaning](#Data Cleaning)
  - [Create SQL view](#Create SQL view)
-  [Testing](#Testing)
-  [Visualization](#Visualization)
  - [Dax Measures](#Dax Measures)
  - [Results](#Results)
-  [Findings](#Findings)
-  [Recomendation](#Recomendation)
-  [Conclusion](#Conclusion)


# Objective
# Data Source
# Steps involved
# Development using SQL
## Data Exploration
## Data Cleaning
## Create SQL view
# Testing
# Visualization
## Dax Measures
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

