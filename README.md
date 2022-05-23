# Cyclistic Case Study: Can We Convert Casual Riders Into Members?

<h2>Introduction</h2>
This case study is a capstone project for the completion of the Google Data Analytics Professional Certificate.

<h3>Background</h3>
Cyclistic is a fictional bike-share company located in Chicago, Illinois. Since its founding in 2016, Cyclistic has grown its fleet to 5,824 geotracked bicycles that dock into 692 Cyclistic stations across the city. Users can undock bikes from a station and return it to any other dock in the Cyclistic network anytime. 
<br><br>
Historically, Cyclistic's marketing strategy has relied on appealing to broad consumer segments with general awareness and flexibility in its pricing plans. Currently, users may choose to purchase single-ride passes, full-day passes, or annual memberships. For the purposes of this analysis, customers who purchase single-ride or full-day passes will be considered casual riders. Customers who purchase annual memberships are Cyclistic members. <br><br>

![cyclistic logo](https://user-images.githubusercontent.com/92185928/169714535-a6594daa-73ca-491b-ab30-ecdd16d82906.png)

<h3>Stakeholder Goals</h3>
The financial team at Cyclistic has recently concluded that annual members are far more profitable to the company than are casual riders. Subsequently, the marketing team has identified maximizing the number of annual memberships as a key goal for the company's success. They want to design a new marketing strategy to convert casual riders into annual members since individuals in this demographic are already aware of the Cyclistic program and have chosen it at some point for their transportation needs in the past. 
<br><br>
In order to do this, the marketing team first wants to understand how these different customer types are currently using Cyclistic bikes. They have identified the following questions to guide the future of their marketing program:<br><br>
<b>1. How do annual members and casual riders use Cyclistic differently?<br>
2. Why would casual riders buy Cyclistic annual memberships?<br>
3. How can Cyclistic use digital media to influence casual riders to become members?<br></b>
  
<h2>Data</h2>
The dataset for this case study was collected internally by Cyclistic and provided to the marketing team for the purposes of determining how different customer types are using Cyclistic bikes. The company has provided one year of data between the months of April 2021 and March 2022 in .csv format. These data include information about each individual bike ride including the ride ID, type of bike, start and end time, start and end station, and start and end longitude and latitude, as well as the type of consumer (member or casual rider) renting the bike.

<h3>Limitations</h3>
One limitation to this case study is that Cyclistic's user privacy policy prevents analysis of some individual user data, including whether a user has purchased multiple single-use passes or whether they live locally to a Cyclistic station. The implications of this limitation are that the data team cannot make recommendations for Cyclistic's marketing plan based on geographic or frequency of use data, nor send specific offers directly to consumers based on their consumer history with the company. Thus, the data team needs to work with a more general picture of useage trends of Cyclistic bikes across Chicago.

<h3>Data Preparation</h3>
First, each .csv file was loaded into RStudio, aggregated, and examined with the tidyverse package. Since locational data for individual users is unavailable for analysis, geographic data (latitude and longitude) is unnecessary; this was dropped from the dataset. Additionally, Cyclistic often undocks its bikes for quality control or maintainance; to account for this, any rides less than 3 minutes in length were also dropped from the dataset. This removed 3.39% of the dataset. The dataset was edited to calculate a field for ride length and day of week for each ride using R functions. 
<br><br>
Data was subsequently cleaned for nulls and duplicates, which were dropped from the dataset to avoid calculation errors during analysis. This dataset was nearly 6 million rows, and included enough incomplete data that just over 1 million rows containing null values were removed. The remaining data consists of 4,463,485 complete observations.

<h2>Analysis</h2>

According to data collected since April 2021, the Cyclistic rider pool is dominated by Cyclistic members, with 2,464,757 members versus only 1,998,728 casual riders active in the last year. Analysis of daily ridership reveals inverse useage patterns between Cyclistic members and casual riders. Members appear to have higher average ridership on weekdays, with peak rides occuring on Wednesdays. Conversely, casual riders appear to have a higher average ridership on weekends, with peak rides occurring on Saturdays. 

![Av Daily Rides 3](https://user-images.githubusercontent.com/92185928/169889617-e43f13e1-bb7f-4a91-9bf4-923f869b059f.png)

These useage patterns might indicate that Cylistic members tend to use bikes on a daily basis as part of their work and errand commutes wheareas casual riders may be more interested in using bikes for recreational purposes on weekend days. In addition, casual riders tend to spend more time on average riding the bikes then do Cyclistic members, suggesting that members use bikes primarily for point-to-point transportation and less for leisure or exploration. The average trip taken by a casual rider lasts 1778 seconds, or about 30 minutes, whereas the average trip taken by a Cyclistic member lasts 814 seconds, or about 14 minutes.

![Av Ride Length 2](https://user-images.githubusercontent.com/92185928/169889692-413787e3-b324-460c-9c0f-86b797956d10.png)

The above chart of daily ridership patterns for trip duration (in seconds) reflects that members tend to use Cyclistic bikes very intentionally, perhaps with high awareness of where Cyclistic docks are located as well as existing directional knowledge of the city layout for short ride times. In addition to the likelihood of casual riders looking to bike on the weekends for leisure, it is possible that some casual riders are visiting from outside of Chicago and lack native locational knowledge. 

Observations of ridership trends throughout the year indicate a seasonal pattern in Cyclistic bike useage. It is more common for both members and casual riders to choose to ride in the summer months, when the weather is nice and the days are long. 

![Monthly Trends 3](https://user-images.githubusercontent.com/92185928/169889193-2fcffe57-69c7-47db-a711-a60a2d5b427a.png)

In fact, summertime riding is so popular that during the months of June, July, and August there are actually more casual riders using Cyclistic bikes than there are members using the bikes, indicating that June through August is an ideal time to convert casual riders to members. 

<h2>Discussion</h2>

Insights from the analysis phase can help the marketing team answer the questions they have identified as the core of their program going forward. The data team can now provide an answer to the first question, "How do annual members and casual riders use Cyclistic differently?":
- Members are more likely to ride on weekdays, whereas casual riders are more likely to ride on weekends
- Members demonstrate peak useage overall on Wednesdays, and casual riders demonstrate peak useage on Saturdays
- Casual riders are more likely to take long-duration rides; members average about half the ride length of casual riders overall
- Both members and casual riders are more likely to ride in the summer months, with July being the most popular time to use a Cyclistic bike
- Ridership in both categories is dramatically lower in January and February, when there is likely to be snow on the ground in Chicago

While the data team did not explicitly investigate the question of "Why would casual riders buy Cyclistic annual memberships?", we can offer some insights based on the analysis here as well:
- Casual riders might choose an annual membership if it were more convenient for them to choose this option for daily use
- Perhaps a casual rider might be enticed by a money-back guarantee that start stations will always have a bike available to them
- It might be helpful to continue building the fleet and advertise that Cyclistic is expanding

Additionally, seasonal ridership data can help the marketing team understand "How can Cyclistic use digital media to influence casual riders to become members?":
- Riders clearly enjoy being outside during Chicago summers, as these are peak ridership months for Cyclistic riders
- Making membership more attractive in the months when riders are most likely to choose to use a Cyclistic bike could help convert casual riders to members

<h2>Recommendations</h2>

Based on this analysis, the data team would recommend to the marketing team the following, for the purposes of encouraging casual riders to become Cyclistic members:
1. Offer occasional weekend membership discounts to casual riders, especially during peak times for this demographic in June, July, and August
2. Run fun, outdoors-centered digital media campaigns in the summer to remind riders that biking is fun, healthy, and environmentally friendly
3. Run a marketing campaign to tout the wellness benefits and cost efficiency of biking to work, especially in a recession economy where gas is expensive
