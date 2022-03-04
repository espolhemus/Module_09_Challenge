# Module_09_Challenge
Module 09 - Surf's Up Challenge

## Overview of Project
This project involves using Jupyter Notebooks, SQLite, pandas, numpy, and SQLite to analyze weather-related data drawn from various weather stations on the island of Oahu. 

### Purpose
The purpose of this challenge is to take an SQLite database containing weather observations from multiple reporting stations spanning a number of years, execute SQL queries to parse the data, and present the underlying data in a manner that will allow for informed business decisions to be made regarding the viability of opening a Surf Shop in the area.  

## Results
The results of our analysis are as follows:

- The following tables of Summary Statistics compare the Temperature Observations between June and December:

    -- June Temperature Findings:
    
![June Statistics](/Images/June_statistics.png)

    -- December Temperature Findings:
  
![December Statistics](/Images/december_statistics.png)

Based on these temperature observations, we would draw your attention to these key differences:

- The average (mean) temperate in June is 74.9 degrees, versus 71.0 degrees in December - a relatively modest difference of less than 4 degrees.

- The median temperature in June is 75.0 degrees, while the median temperature in December is 71.0 degrees - again, a relatively modest difference of 4 degrees.

- While the difference in minimum temperature is potentially material (64.0 degrees in June versus 56.0 degrees in December), when looking at the top 3 quartiles, 75% of days in December have a temperature at or above 69.0 degrees, with a full 50 percent of days in December being 71.0 degrees or warmer.

## Summary of Analysis
Based on the weather-related data included in the SQLite database, it appears that the location under consideration would be very suitable for a Surf Shop, with temperatures remaining relatively consistent throughout the year.  In addition to the temperature-related analysis, the following additional queries may be instructive in informing the decision making process: 

### Comparison of Precipitation Statistics between June and December

- - The following tables of Summary Statistics compare the Precipitation Observations between June and December:

    -- June Precipitation Findings:
    
![June Statistics](/Images/june_precipitation.png)

    -- December Precipitation Findings:
  
![December Statistics](/Images/december_precipitation.png)

### Precipitation-Free Days

- Furthermore, by constructing a query similar to the example below, and plotting the results, we can get a better sense as to how many precipitation-free days there, and we can gain a better understanding of the amount of precipitation that falls on those days where there is measurable precipitation, which will help us determine whether or not the number of days with significant rainfall would be material to the success of our proposed Surf Shop
 
    -- results = session.query(Measurement.prcp, (func.count(Measurement.date))).group_by(Measurement.prcp).all()
    
    -- Precipitation Histogram:
  
![Precipitation Histogram](/Images/precipitation_histogram.png)
    
    
