# DSND-DataScienceBlog
Data Science Nanodegree P1 - Write a data science blog 

## Introduction
The purpose of this project was to pose three questions in relation to a data set, and then to apply the CRISP-DM process along with data analytics techniques to answer those questions. I chose to analyze the [Seattle AirBnB data set](http://www.insideairbnb.com/get-the-data.html), principally that listed for the upcoming year. The overall results are presented in a blog post that can be found [here](https://medium.com/@jaalfordii/the-where-when-and-how-much-of-airbnb-in-seattle-b2184b51700b).

The three questions I decided to tackle were:

1) For the upcoming year where will be the most/least expensive AirBnB listings in Seattle and how will prices change throughout the year?

2) For the average renter, will it pay to book early?

3) What are the other leading factors that determine price for an AirBnB rental?

## CRISP-DM Process
Pre-deploymet, the cross-industry standard process for data mining breaks down the applied data analytics process into five major phases.


  *  Business Understanding
  *  Data Understanding
  *  Data Preparation
  *  Modeling
  *  Evaluation

###  Business Understanding

Airbnb, Inc. is an online marketplace for arranging temporary lodging, primarily homestays, and tourism experiences.
The three questions above, all related to the price of AirBnB rentals, can be useful to hosts, to help determine when or when not to offer discounts for example, and renters alike. The data used to answer these questions would also be useful to the AirBnB business, to examine for instance profitability and growth of rentals among various neighborhoods over time.

### Data Understanding

[insideairbnb.com](http://www.insideairbnb.com/get-the-data.html) provides snapshots of data from the AirBnB website at different times for various cities. 
The three types of files provided are

  * listings.csv -- Contains characteristics of each listing, e.g. type of rental, neighborhood, gis info, number of beds and bath, number of review per month etc... Each row contains unique listing.
  * calendar.csv -- Contains individual date availability and price going forward for a year for each listing.
  * reviews.csv  -- Contains reviews for each listing.
  
For question 2 above we made use of calendars posted at different times. In our python code, we tagged each calendar file with the month and year of the snapshot (scrape). 

  * [calendar_01_19.csv](http://data.insideairbnb.com/united-states/wa/seattle/2019-01-17/data/calendar.csv.gz) -- data.insideairbnb.com/united-states/wa/seattle/2019-01-17/data/calendar.csv.gz 
  * [calendar_05_19.csv](http://data.insideairbnb.com/united-states/wa/seattle/2019-05-18/data/calendar.csv.gz) -- data.insideairbnb.com/united-states/wa/seattle/2019-05-18/data/calendar.csv.gz
  * [calendar_06_19.csv](http://data.insideairbnb.com/united-states/wa/seattle/2019-06-13/data/calendar.csv.gz) -- data.insideairbnb.com/united-states/wa/seattle/2019-06-13/data/calendar.csv.gz 
  * [calendar_07_19.csv](http://data.insideairbnb.com/united-states/wa/seattle/2019-07-14/data/calendar.csv.gz) -- data.insideairbnb.com/united-states/wa/seattle/2019-07-14/data/calendar.csv.gz
  * [calendar_08_19.csv](http://data.insideairbnb.com/united-states/wa/seattle/2019-08-18/data/calendar.csv.gz) -- data.insideairbnb.com/united-states/wa/seattle/2019-08-18/data/calendar.csv.gz
  

### Modeling and Evaluation 

Questions 1 and 2 were addressed by the usual sorting, subsetting, grouping, and differencing of the data. We identified
the Queen Anne district and Seward Park area of Seattle as generally being the most expensive places to rent, whereas listings in Northgate are very affordable. We found that Summer is the most expensive time of year for offerings close to the average price, but not so for properties at higher/lower ends of the price spectrum. For the average renter, we didn't find a general trend indicating an advantage to booking early. Using a Random Forest Regressor, we also determined that guest suites, private rooms, and hosts with verified id are indicators of a highly valued AirBnB property. 


