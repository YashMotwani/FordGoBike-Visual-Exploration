# FordGoBike Data Visualization
## by Yash Motwani


## Introduction

Bay Wheels(FordGoBike) is a regional public bicycle sharing system in the San Francisco Bay Area, California. Beginning operation in August 2013 as Bay Area Bike Share, the Bay Wheels system currently has over 2,600 bicycles in 262 stations across San Francisco, East Bay and San Jose.  The system is operated by Motivate in a partnership with the Metropolitan Transportation Commission and the Bay Area Air Quality Management District. Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States.

Bay Wheels is a public bicycle system, or bike-share scheme, in which bicycles are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" and return it at another dock belonging to the same system. Docks are special bike racks that lock the bike, and only release it by computer control. The user enters payment information, and the computer unlocks a bike. The user returns the bike by placing it in the dock, which locks it in place. Other systems are dockless. For many systems, smartphone mapping apps show nearby available bikes and open docks.

Here we wrangle and explore Baywheel's trip data which it makes available for public use. Baywheel's trip data is anonymized and includes:

- Trip Duration (seconds)
- Start Time and Date
- End Time and Date
- Start Station ID
- Start Station Name
- Start Station Latitude
- Start Station Longitude
- End Station ID
- End Station Name
- End Station Latitude
- End Station Longitude
- Bike ID
- User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
- Member Year of Birth
- Member Gender

## Dataset Overview

In this project we will explain Baywheels(FordGoBike) Trip Data. In the dataset, there are total 16 columns for referring to 16 different variables and 1,861,220 rows referring to observations. Following are the further details about variables: 
1. 3 columns referring to 3 categorical variables.

    a. `member_gender` - with 3 categories - Male, Female, Other
    
    b. `bike_share_for_all_trip` - with 2 categories referring to member's interest - yes, no
    
    c. `user_type` - with 2 categories - customer, subscriber
    
    
2. 10 columns referring to postion, name, id, date and time of the starting and ending stations


3. 1 column for bike information(`bike_id`), 1 column for `member_birth_year` and 1 column for trip duration(`duration_sec`)

## Summary of Findings

- When we related duration with weekdays, we saw that people are likely to go for long rides on weekends although most bikes get rented on weekdays.

- When we related duration with months, we saw that people have liked to go out on long rides and enjoy in summers from April till July. But after september, whenwinter starts people again start taking shorter rides.

- When we related duration with hours, we saw that there was an interesting pattern. During the early morning hours form 1a.m. to 4 a.m., people have less liked to rent bikes and also the ones who rented were also for short duration. While most number of bikes around 2 p.m. were rented for high duration of around 600 seconds.

So, when we were exploring user information variables with other variables, we saw they relate to one another in an interesting way.
- Males are very much likely to follow adults group in terms of for what duration the bikes have been rented. And similarly, females are very much likely to follow the youth and others are likely to follow seniors.
- Similar trend as above was observed in terms how many bikes have been rented in a weekday or in terms of how many bikes have been rented in an hour

- Males and Adults show much similarity in duration for using bike when compared over the weekdays and months

- we mainly explored genders within each age group for comparison on duration and other time variables like month, weekday and hour. Here, we saw that youth and adults age groups show much similarity in terms of how many bikes were rented by eavh. Although the adults have always rented more bikes than youth but the preference in renting the number of bikes according to weekdays and hours were almost the same.


## Key Insights for Presentation

In this project, we investigated and understood the relation of member's age group and gender with their bike usage in terms of duration, weekdays, months and hours and found the following insights:

- Most number of times bike have been rented by adults, followed by youth and at the last the seniors
- With respect to genders, males have rented the bikes most of the times followed by females and others. 
- In terms of number of bike rents on a given weekday, adults and young age groups follow a similar trend.
- In terms of number of bike rents on a given weekday, males are likely to follow adults, and females are likely to follow young age groups.
- In terms of number of bike rents in a given month, females are likely to follow youth trend.
- 8 a.m. and 5 p.m. are the most busy hours in general
- For all the age groups, weekdays are for short rides and weekends are for long rides
- In terms of genders, males prefer rides for shorter duration while females prefer rides for high duration
- Seniors prefer renting bikes for long rides in summers and short rides during winters

**Note:** After creating the slide deck with jupyter, to make use of a public, online version of `reveal.js`, to start up a server, and to immediately open a tab simultaneously in the web browser with the slide deck ready to navigate, use the following code on the command line, with `output_toggle.tpl` saved in the directory where the slide deck is present and command is being run:

```
jupyter nbconvert presentation.ipynb --to slides --template output-toggle.tpl
--post serve
```

## RESOURCES
1. [Matplotlib Documentation](https://matplotlib.org/)


2. [Plots using FacetGrid Object](https://seaborn.pydata.org/generated/seaborn.FacetGrid.html)


3. [Pointplots](https://seaborn.pydata.org/generated/seaborn.pointplot.html)


4. [Countplots](https://seaborn.pydata.org/generated/seaborn.countplot.html)


5. [FordGoBike Data](https://s3.amazonaws.com/baywheels-data/index.html)
