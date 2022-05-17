# Cyclistic Case Study: Can We Convert Casual Riders Into Members?

<h2>Introduction</h2>
This case study is a capstone project for the completion of the Google Data Analytics Professional Certificate.

<h3>Background</h3>
Cyclistic is a fictional bike-share company located in Chicago, Illinois. Since its founding in 2016, Cyclistic has grown its fleet to 5,824 geotracked bicycles that dock into 692 Cyclistic stations across the city. Users can undock bikes from a station and return it to any other dock in the Cyclistic network anytime. 
<br><br>
Historically, Cyclistic's marketing strategy has relied on appealing to broad consumer segments with general awareness and flexibility in its pricing plans. Currently, users may choose to purchase single-ride passes, full-day passes, and annual memberships. For the purposes of this analysis, customers who purchase single-ride or full-day passes will be considered casual riders. Customers who purchase annual membership are Cyclistic members. 

<h3>Stakeholder Goals</h3>
The financial team at Cyclistic has recently concluded that annual members are far more profitable to the company than are casual riders. Subsequently, the marketing team has identified maximizing the number of annual memberships as a key goal for the company's success. They want to design a new marketing strategy to convert casual riders, who are already aware of the Cyclistic program and have chosen it at some point for their past transportation needs, into annual members. 
<br><br>
In order to do this, the marketing team first wants to understand how these different customer types are currently using Cyclistic bikes. They have identified the following questions to guide the future of their marketing program:<br><br>
<b>1. How do annual members and casual riders use Cyclistic differently?<br>
2. Why would casual riders buy Cyclistic annual memberships?<br>
3. How can Cyclistic use digital media to influence casual riders to become members?<br></b>
  
<h2>Data</h2>
The dataset for this case study was collected internally by Cyclistic and provided to the marketing team for the purposes of determining how different customer types are using Cyclistic bikes. The company has provided one year of data between the months of April 2021 and March 2022 in .csv format. These data include information about each individual bike ride including the ride ID, type of bike, start and end time, start and end station, and start and end longitude and lattitude, as well as the type of consumer (member or casual rider) renting the bike.

<h3>Limitations</h3>
One limitation to this case study is that Cyclistic's user privacy policy prevents analysis of some individual user data, including whether a user has purchased multiple single-use passes or whether they live locally to a Cyclistic station. The implications of this limitation are that Cyclistic cannot make recommendations for its marketing plan based on geographic or frequency of use data, nor send specific offers directly to consumers based on their consumer history with the company. Thus, the data team needs to work with a more general picture of useage trends of Cyclistic bikes across Chicago.

<h3>Data Preparation</h3>
First, each .csv file was edited in Excel to calculate a field for ride length (end time - start time) and day of week for each ride using the WEEKDAY function. Then, the files were loaded into RStudio and examined with the tidyverse package in R for nulls and duplicates, which were dropped from the dataset. This dataset is well over 5 million rows, so statistical analysis is not affected by the removal of these data points.

<h2>Analysis</h2>
[summary of analysis]

<h2>Discussion</h2>
[supporting visualizations & key findings]

<h2>Recommendations</h2>
[top 3 recommendations based on analysis]
