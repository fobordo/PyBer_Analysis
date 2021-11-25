# PyBer Analysis

## Overview of PyBer Analysis
The purpose of the PyBer Analysis was to analyze the correlation between two datasets containing four months of rideshare data on Rural, Suburban, and Urban cities, [city data](https://github.com/fobordo/PyBer_Analysis/blob/64873e609f3add2b33a784bcc7ed44bafcd6cae9/Resources/city_data.csv) and [ride data](https://github.com/fobordo/PyBer_Analysis/blob/64873e609f3add2b33a784bcc7ed44bafcd6cae9/Resources/ride_data.csv), through the creation of compelling visualizations in order to help the company improve access to ride-sharing services and determine affordability for underserved neighborhoods. Python scripts were written using Pandas libraries, Jupyter Notebook, and Matplotlib to create a variety of charts that demonstrate the relationship between the type of city and the number of drivers and riders, as well as the percentage of total fares, riders, and drivers by type of city.

## Results:
To perform the analysis, the `city_data.csv` and `ride_data.csv` files were merged into a single DataFrame called `pyber_data_df`. From this DataFrame, a new DataFrame called `pyber_data_summary_df` was created consisting of the following calculations:
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

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had 125, 625, and 1625 total rides in four months, consecutively. We can assume that the total number of rides directly correlates to the population size of each city type, and by association, ride demand. We observed the following:
* Urban cities had the largest number of total rides of 1625. We can assume that this is due to the fact that Urban cities have the largest population size among the three city types, therefore also have the highest ride demand. 
* Since Suburban cities have the second-largest population size and ride demand, they had the second-largest number of total rides of 625. 
* Since Rural cities have the smallest population size and ride demand, they had the smallest number of total rides of 125.

#### 2. Total Fares
![pyber_summary_df_total_fares](/analysis/pyber_summary_df_total_fares.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had $4,327.93, $19,356.33, and $39,854.38 in total fares in four months, consecutively. The total fares directly correlate to the total rides of each city type. We observed the following:
* Since Urban cities had the highest total rides among the three city types, they also had the largest amount of total fares of $39,854.38. 
* Since Suburban cities had the second-highest total rides, they had the second-largest amount of total fares of $19,356.33. 
* Since Rural cities had the lowest total rides, they had the smallest amount of total fares of $4,327.93.

#### 3. Total Drivers
![pyber_summary_df_total_drivers](/analysis/pyber_summary_df_total_drivers.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had 78, 490, and 2405 total drivers in four months, consecutively. Similar to the total rides, we can assume that the total number of drivers directly correlates to the population size and ride demand of each city type. We observed the following:
* Since Urban cities have the largest population size and highest ride demand among the three city types, they had the largest number of total drivers of 2405. 
* Since Suburban cities have the second-largest population size and ride demand, they had the second-largest number of total drivers of 625. 
* Since Rural cities have the smallest population size and ride demand, they had the smallest number of total drivers of 125.

#### 4. Average Fare per Ride
![pyber_summary_df_avg_fare_per_ride](/analysis/pyber_summary_df_avg_fare_per_ride.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had an average fare per ride of $34.62, $30.97, and $24.53 in four months, consecutively. The average fares per ride were caculated by dividing the total fares by total rides for each type. We observed the following:
* Since Urban cities had highest amount of total fares and number of total rides, they had the lowest average fare per ride of $24.53.
* Since Suburban cities had the second-highest amount of total fares and number of total rides, they had the second-lowest average fare per ride of $30.97.
* Since Rural cities had the lowest number of total fares and rides, they had the highest average fare per ride of $34.62. 

We can conclude that the higher the amount of total fares and number of total rides, the lower the average fare per ride. Conversely, the lower the amount of total fares and number of total rides, the higher the average fare per ride.

#### 5. Average Fare per Driver
![pyber_summary_df_avg_fare_per_driver](/analysis/pyber_summary_df_avg_fare_per_driver.png)

The `pyber_summary_df` DataFrame showed that Rural, Suburban, and Urban cities had an average fare per driver of $55.49, $39.50, and $16.57 in four months, consecutively. The average fares per driver were caculated by dividing the total fares by total drivers for each type. We observed the following:
* Since Urban cities had the highest amount of total fares and number of total drivers, they had the lowest average fare per driver of $16.57.
* Since Suburban cities had the second-highest amount of total fares and number of total drivers, they also had the second-lowest average fare per driver of $39.50.
* Since Rural cities had the lowest amount of total fares and number of total drivers, they had the highest average fare per driver of $55.49. 

We can conclude that the higher the amount of total fares and number of total drivers, the lower the average fare per driver. Conversely, the lower the amount of total fares and number of total drivers, the higher the average fare per driver.

#### 6. Total Weekly Fares

![PyBer_fare_summary](/analysis/PyBer_fare_summary.png)

The `Total Fare by City Type` multiple line plot showed that the Rural, Suburban, and Urban cities had the lowest, second highest, and highest total weekly fares from January to April 2019, consecutively. We observed the following: 
* The total weekly fares for Rural cities were within the range of $0 to $500. 
* The total weekly fares for Suburban cities were within the range of $550 to $1500.
* The total weekly fares for Urban cities were within the range of $1600 to $2500. 
* The lines for each city type fluctuate throughout each month, which demonstrates the fluctuation of demand throughout the four months. 

## Summary:
Based on the results we observed from the `pyber_data_summary_df` DataFrame and `Total Fare by City Type` multiple line plot, we would suggest the following business recommendations to address any disparities among the city types.

### 1. Increase Total Drivers in Rural Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Rural cities was as follows 125:78.

The ride demand in Rural cities was higher than the total number of drivers available to accommodate those rides, suggesting that more drivers are needed to meet the need for ride demand. We suggest increasing the number of total drivers in Rural cities to get the ratio of total rides to total drivers to a more evenly distributed measure. If more drivers are available to provide more rides, the ride demand would increase, inevitably increasing total fares as well and bringing in more revenue for the company, while also decreasing the average fare per ride and driver, making ride-sharing more affordable in these cities with smaller populations.

### 2. Increase Total Drivers in Suburban Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Suburban cities was 125:98. 

Similarly to Rural cities, the ride demand in Suburban cities was higher than the total number of drivers available to accommodate those rides, suggesting that more drivers are needed to meet the need for rides. Just as we suggested for Rural cities, we suggest increasing the number of total drivers in Suburban cities to get the ratio of total rides to total drivers to a more evenly distributed measure. Again, the more drivers available, the more rides that can be completed, which could potentially increase demand as well as total fares, bringing in more revenue for the company, while also decreasing the average fare per ride and driver, making ride-sharing more affordable in these cities with smaller populations.

### 3. Decrease Total Drivers in Urban Cities
From the `pyber_data_summary_df` DataFrame, we saw that the ratio of total rides to total drivers (Total Rides : Total Drivers) in Urban cities was 25:37. 

Conversely to Rural and Suburban cities, the ride demand in Urban cities was lower than the total number of drivers, suggesting that there is an oversaturation of drivers in Urban cities. We suggest decreasing the number of total drivers in Urban cities to get the ratio of total rides to total drivers to a more evenly distributed measure.