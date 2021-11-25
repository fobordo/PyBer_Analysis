# PyBer Analysis

## Overview of PyBer Analysis
The purpose of the PyBer Analysis was to analyze the correlation between two datasets containing four months of rideshare data on Rural, Suburban, and Urban cities, [city data](https://github.com/fobordo/PyBer_Analysis/blob/64873e609f3add2b33a784bcc7ed44bafcd6cae9/Resources/city_data.csv) and [ride data](https://github.com/fobordo/PyBer_Analysis/blob/64873e609f3add2b33a784bcc7ed44bafcd6cae9/Resources/ride_data.csv), through the creation of compelling visualizations in order to to help the company improve access to ride-sharing services and determine affordability for underserved neighborhoods. Python scripts were written using Pandas libraries, Jupyter Notebook, and Matplotlib to create a variety of charts that demonstrate the relationship between the type of city and the number of drivers and riders, as well as the percentage of total fares, riders, and drivers by type of city.

## Results:
To perform the analysis, the `city_data.csv` and `ride_data.csv` files were merged into a single DataFrame called `pyber_data_df`. From this DataFrame, a new DataFrame called `pyber_data_summary_df` was created consisting of the following calculatons:
1. Total Rides for each city type
2. Total Drivers for each city type
3. Total Fares for each city type
4. Average Fare per Ride for each city type
5. Average Fare per Driver for each city type

![pyber_summary_df](/analysis/pyber_summary_df.png)

Then, a multiple line plot was created to show the total weekly fares for each type of city.

![PyBer_fare_summary](/analysis/PyBer_fare_summary.png)

The `pyber_data_summary_df` DataFrame and `Total Fare by City Type` multiple line plot showcased various differences in ride-sharing data among the different city types.

### Differences in Ride-Sharing Data Among the Different City Types

#### 1. Total Rides
![pyber_summary_df_total_rides](/analysis/pyber_summary_df_total_rides.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had 125, 625, and 1625 total rides in four months, consecutively. We can assume that the total number of rides directly correlates to the population size of each city type. Since Urban cities have the largest population size, it makes sense that they also had the largest number of total rides of 1625. Since Surbuban cities have the second-largest population size among the three city types, they had the second-largest number of total rides of 625. Lastly, since Rural cities have the smallest population size among the three city types, they had the smallest number of total rides of 125.

#### 2. Total Fares
![pyber_summary_df_total_fares](/analysis/pyber_summary_df_total_fares.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had $4,327.93, $19,356.33, and $39,854.38 in total fares in four months, consecutively. Similar to the total rides for each city type, the total fares directly correlates to the population size of each city type. Since Urban cities have the largest population size, they also had the largest amount of total fares of $39,854.38. Since Surbuban cities have the second-largest population size among the three city types, they had the second-largest amount of total fares of $19,356.33. Lastly, since Rural cities have the smallest population size among the three city types, they had the smallest amount of total fares of $4,327.93.

#### 3. Total Drivers
![pyber_summary_df_total_drivers](/analysis/pyber_summary_df_total_drivers.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had 78, 490, and 2405 total drivers in four months, consecutively. Looking back at the total rides and total fares for each city type, we can observe the demand for drivers based on the city type and confirm that the total rides and total fares directly correlates to the number of drivers in each city type. Just as Urban cities had the highest number of total rides and total fares, Urban cities had the second-largest number of total rides and total fares, and Rural cities had the lowest number of total rides and total fares, it is the same for total drivers. 

#### 4. Average Fare per Ride
![pyber_summary_df_avg_fare_per_ride](/analysis/pyber_summary_df_avg_fare_per_ride.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had an average fare per ride of $34.62, $30.97, and $24.53 in four months, consecutively. As we have now observed from the total rides, total fares, and total drivers for each city type, we can see that the average fare per ride correlates directly to demand. Since Urban cities had the highest demand for rides, and by relation, drivers, they had the lowest average fare per ride of $24.53. We can conclude that the higher the demand, the lower the average fare per ride. Since Suburban cities had the second-highest demand for rides and drivers, they had the second-lowest average fare per ride of $30.97. And since Rural cities had the lowest demand for rides and drivers, they had the highest average fare per ride of $34.62. The lower the demand, the higher the average fare per ride.

#### 5. Average Fare per Driver
![pyber_summary_df_avg_fare_per_driver](/analysis/pyber_summary_df_avg_fare_per_driver.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had an average fare per driver of $55.49, $39.50, and $16.57 in four months, consecutively. Just as we observed in our analysis of the average fare per ride, we can see that the average fare per driver coincides with the average fare per ride, and by association, also correlates directly to demand. Since Urban cities had the highest demand and lowest average fare per ride, they had the lowest average fare per driver of $16.57. We can conclude that the higher the demand, the lower the average fare per ride and per driver. Since Suburban cities had the second-highest demand and second-lowest average fare per ride, they also had the second-lowest average fare per driver of $39.50. And since Rural cities had the lowest demand and highest average fare per ride, they had the highest average fare per driver of $55.49. The lower the demand, the higher the average fare per ride and per driver.

#### 6. Total Weekly Fares

![PyBer_fare_summary](/analysis/PyBer_fare_summary.png)

The `Total Fare by City Type` multiple line plot showed that the Rural, Suburban, and Urban cities had the lowest, second-highest, and highest total weekly fares from January to April 2019, consecutively. The total weekly fares for Rural cities were within the range of a little above $0 to $500 max. The total weekly fares for Suburban cities were within the range of about $550 to $1500 max. Finally, the total weekly fares for Urban cities were within the range of about $1600 to $2500 max. The lines for each city type fluctuate throughout each month, which demonstrates the fluctuation of demand throughout the four months. Just as we saw in the previous 5 metrics, we can assume that the total weekly fare for each city type correlates directly to demand and population size. The bigger the demand and population size, the higher the total weekly fare. Or conversely, the lower the demand and population size, the lower the total weekly fare.

## Summary:
Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.

There is a statement summarizing three business recommendations to the CEO for addressing any disparities among the city types

Based on the results we observed from the `pyber_data_summary_df` DataFrame and `Total Fare by City Type` multiple line plot, we would suggest the following business recommendations to address any disparities among the city types.

### 1. Increase Total Drivers in Rural Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Rural cities was as follows 125:78.

The demand for rides in Rural cities was higher than the total number of drivers available to accomodate those rides, suggesting that more drivers are needed to meet the need for rides. We suggest increasing the number of total drivers in Rural cities to get the ratio of total rides to total drivers to a more evenly distributed measure. If more drivers are available to provide more rides, and the number of rides increases due to the availability of more drivers, the total fares would increase as well, bringing in more revenue for the company, while also decreasing the average fare per ride and driver, making ride-sharing more affordable in these cities with smaller populations.

### 2. Increase Total Drivers in Suburban Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Suburban cities was 125:98. 

Similarly to Rural cities, the demand for rides in Suburban cities was higher than the total number of drivers available to accomodate those rides, suggesting that more drivers are needed to meet the need for rides. Just as we suggested for Rural cities, we suggest increasing the number of total drivers in Suburban cities to get the ratio of total rides to total drivers to a more evenly distributed measure. Again, the more drivers avaialble, the more rides that are able to be completed, which could potentially increase demand as well as total fares, bringing in more revenue for the company, while also decreasing the average fare per ride and driver, making ride-sharing more affordable in these cities with smaller populations.

### 3. Decrease Total Drivers in Urban Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Urban cities was 25:37. 

Conversely to Rural and Suburban cities, the demand for rides in Urban cities was lower than the total number of drivers, suggesting that there is an oversaturation of drivers in Urban cities. We suggest decreasing the number of total drivers in Urban cities to get the ratio of total rides to total drivers to a more evenly distributed measure.