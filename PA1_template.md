# Reproducible Research: Peer Assessment 1

```r
library(knitr)
library(ggplot2)
opts_chunk$set(echo = FALSE, fig.path = "figure/")
```

## Loading and preprocessing the data
Load the activity monitoring data into a data frame:



## What is mean total number of steps taken per day?
Compute the sum of steps by date and draw a histogram:
![](figure/histogram-1.png) 

Calculate the mean and the median, omitting days which have no data available:


The **mean** of total number of steps taken each day (rounded to two decimals)
is **10766.19**.

The **median** of total number of steps taken each day is **10765**.


## What is the average daily activity pattern?
Compute the mean of steps by 5-minute interval and draw a time series plot:
![](figure/timeseries-1.png) 

Find the 5-min interval containing the highest number of steps on average:


5-minute interval **835** contains the maximum number
(~ 206) of steps on average.


## Imputing missing values
Calculate and report the total number of missing values in the
dataset (i.e. the total number of rows with NAs):

Number of missing values in the activity data set is **2304**.

Create a new dataset that is equal to the original dataset but with the
missing data filled in, using the 5-min interval averages:


Compute the sum of steps by date for the imputed data set and draw a histogram:
![](figure/histogram_imputed-1.png) 

Calculate the mean and the median for the imputed data set:


The **mean** of total number of steps taken each day (rounded to two decimals)
for the imputed data set is **10766.19**.

The **median** of total number of steps taken each day (rounded to two decimals)
for the imputed data set is **10766.19**.

Imputing missing values using the 5-min interval averages does not affect
the mean total number of steps taken per day. Imputing has a slight effect
on the median.


## Are there differences in activity patterns between weekdays and weekends?
Create a new factor variable in the imputed dataset with two levels,
"weekday" and "weekend", indicating whether a given date is a weekday
or a weekend day:


Compute the mean of steps by 5-minute interval for both weekdays and weekends.
Make a panel plot containing a time series plot of the 5-minute interval
(x-axis) and the average number of steps taken, averaged across all weekday
days or weekend days (y-axis):

![](figure/timeseries_per_daytype-1.png) 
