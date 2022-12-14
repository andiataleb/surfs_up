# surfs_up

## Overview
In this project I am performing an analysis to help W.Avy, an investor decide on the feasibility of opening a Surf and Shake shop in Hawaii.
In this repository, some information about the weather temperatures in the months of June and December can be found. 

## Results
Based on the tables below we can see that:
- There are 1700 temperature data points for the month of June and 1517 data points for the month of December. 
- The average temperature for June is 74.9 F compared to December which is 71 F. The standard deviation is also pretty similar in both months. This shows the average temperature doesn't change much between June and December and changes only about 1 standard deviation. 
- The minimum temperature is 8 F lower in December compared to June and the maximum temperature is close to each other. 

![](Images/june.png)
![](Images/dec.png)


## Summary
There is not much difference between the months of June and December in the temperature studies based on the current dataset that we have and the weather with regards to temperature seems to be suitable for "Surf and Shake".
However, the temperature is not the only factor in surfing. Therefore, I recommend running the following queries to retrieve precipitation information for the months of June and December.

`june_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()`


`dec_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()`
