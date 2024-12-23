# Data Portfolio

This is my portfolio website

#  header
##  Subheader
###  Subheader(header)

# Table of Contents
-  [Objective](#Objective)


![Figure name](filepath in github)

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

