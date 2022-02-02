# Surfs Up Challenge
Overview

In this analysis, we gathered Summary statistics data for the temperature in Oahu for the months of June and December to determine if opening a Surf and Ice cream shop business in Oahu is sustainable throughout the year.  In the first deliverable, we created query that filters the date column from the Measurement table to retrieve all the temperatures for the month of June, converted the June temperatures to a list, created a DataFrame and generated the summary statistics for the June temperature.

In the second deliverable, we followed the same steps used in the first deliverable but changed the month from June to December and generated the summary statistics for the December temperatures. 

Results

In the generated Summary Statistics for both June and December, the list includes the count, mean, standard deviation, Minimum, 25%, 50%, 75% and Maximum temperatures. For the month of June, the total count was 1700, the minimum temperature was 64 degrees and maximum temperature was 85 degrees.

<img width="331" alt="Summary Statistics for June " src="https://user-images.githubusercontent.com/85265504/152091577-49c317d6-7c05-4ad8-96dd-e1fff860db86.png">

For the December Summary statistics, the total count was 1517, the minimum temperature was 56 degrees and maximum temperature was 83 degrees. 

<img width="331" alt="Summary Statistics for December" src="https://user-images.githubusercontent.com/85265504/152091608-c50c6014-dd77-4e5e-a5a0-13bdcfa0b684.png">

The main differences between the temperature for both months are: 

	The average temperature for June is 75 degrees while the average temperature for December is 71 degrees

	The minimum temperature for June is 64 degrees while the minimum temperature for December is 56 degrees


	The maximum temperature for June is 85 degrees while the maximum temperature for December is 83 degrees.

Summary

Based on the data gathered, temperatures in June ranged from 64 degrees to 85 degrees while temperatures in December ranged from 56 degrees to 83 degrees. Based on this information, we can conclude that opening an Ice cream and Surf shop business will be sustainable year-long. 

We can extract the total precipitation levels for the months of June and December by running the following code: 
session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
