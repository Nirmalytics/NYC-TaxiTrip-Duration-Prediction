# NYC-TaxiTrip-Duration-Prediction
 
### Problem Statement:
The NYC Taxi Company wants to predict the duration of each trip at the point when the trip starts

### Data Sources

Trip Info
Traffic & Geographic info
Weather


### Description of all the variables / features available in the dataset.

**id** - a unique identifier for each trip

**vendor_id** - a code indicating the provider associated with the trip record

**pickup_datetime** - date and time when the meter was engaged

**dropoff_datetime** - date and time when the meter was disengaged

**passenger_count** - the number of passengers in the vehicle (driver entered value)

**pickup_longitude** - the longitude where the meter was engaged

**pickup_latitude** - the latitude where the meter was engaged

**dropoff_longitude** - the longitude where the meter was disengaged

**dropoff_latitude** - the latitude where the meter was disengaged

**store_and_fwd_flag** - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server (Y=store and forward; N=not a store and forward trip)

**trip_duration** - (target) duration of the trip in seconds

-------
## Summary – EDA

### Summary of Target variable:
The maximum value (Extreme outlier) is 1.9 million seconds ie 22.45064815 days.
Trip duration of 22.45064815 exists only once and we can safely remove this row as it’s an error.
The minimum value is 1 second which is most probably error

### Summary of Passenger count:
There are 33 zero passengers which might be error
Most passengers lies between 1 & 2
Passengers above 6 is rare
Passenger count Maximum 9 needs more exploration

### Summary of day of week:
Most passengers is on Friday and Saturday
Monday has least passengers followed by Sunday
Inference of Distance, Speed and Duration on Weekdays Sunday:

Distance (top)
Speed (top)
Duration (low)
### Monday:

Distance (high)
Duration (low)
### Tuesday:

Distance (least)
### Wednesday:

Distance (low)
### Thursday:

Speed (least)
Duration (top)
### Friday:

Speed (low)
Duration (high)
### Saturday:

Distance (low)

### Summary of distance:
Distance 1240.910000 likely to be an error, have to be removed.
3927 trips with zero distance, which is an error
Distance remains almost same for vendor 1 and 2
store_and_fwd_flag is stored mainly for short distance trips
Distance is more on Sunday and Monday and takes the least on Tuesday, Saturday, Wednesday
Distance is more on May, June months and least on February and January
Distance is more on Noon and Evening and least on Night

### Summary of Speed:

Speed 5640.500000 likely to be an error
There are 3927 Zero speed entries
Speed remains same for vendor 1 and 2
store_and_fwd_flag is stored mainly for short Speed trips
Speed is more on Sunday and takes the least on Thursday and Friday
Speed is almost same for all months
Speed is more at Night and least on Noon

### Summary of Vendor:

vendor 2 has more trips
Speed & Distance remains almost same for vendor 1 and 2
Short trip duration usually happens for vendor 1

### Summary of Climate:

Climate variable, store_and_fwd_flag is mostly non operational
Store_and_fwd_flag is stored mainly for short distance, short duration, and short speed trips

### Summary of Time Zone & Month:

Evening & Noon Timezone has more trips, Morning the least
There is not much difference in the number of trips across months.

### Inference of Distance, Speed and Duration on Months

Jan: Duration (low), Distance (low)
Feb: Duration (least), Distance (least)
May: Duration (top), Distance (top)
June: Duration (high), Distance (high)

### Inference of Distance, Speed and Duration on Time Zone

Morning: Duration (least), Speed (least)
Noon: Duration (Top), Distance (Top),
Evening: Duration (high), Distance (high),
Night: Distance (least), Speed (more)
Distance and trip Duration have correlation and also causally connected
Distance have correlation with Speed

-----------------

## Installation

NYC taxi trip duration was predicted using Linear Regression Alogorithm.

Training Mean Absolute Error 0.014390202205253897
Test Mean Absolute Error     0.014374795788467263

--------
