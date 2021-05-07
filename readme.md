# (Ford GoBike System Data)
### by (Youssef Hussein Ahmed)

## Dataset Overview

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area.

### To clean dataset:
- change the dtype of "start_time" and "end_time" variables to be datetime64.
- "bike_id" variable has "int64" type but should not treat as so.. it should be casted into string type.

## Summary of Findings

### A- Univariate Exploration

#### 1- Distribution of Trips Durations:
- Duration is mostly centered on values that less than 2000 sec.
- Trips number increases starting from around 1000 trip to 8500 trip in duration values up to 400 sec but then starts to decrease to less than 1000 trip in duration values that under 1300 sec.
- Distribution in normal scale seemed to be a little right skewed but in log10 scale seemed to be normally distributed.

#### 2- Distribution of "start_time" and "end_time"
- The largest percentage of trips are made during weekdays rather than weekends.
- It seems the largest percentage of trips starts at evening and also end through it.
- During early morning, morning and noon, There's close percentage of trips that start and end through them.
- The least percentage of trips are made through night.

#### 3- Distribution of 'user_type'
- The largest percentage of trips are by subscribers.

#### 4- Distribution of 'member_birth_year'
- Most of trips are by the people who were born during late 80's and early 90's.
- Number of trips grows starting from 70's borns up to 90's (more than 4k trip) but then starts to fall.

#### 5- Distribution of 'member_gender'
- The largest percentages of trips are by males.

#### 6- Distribution of 'bike_share_for_all_trip'
- The largest percentage of trips have no bike share option.

### B- Bivariate Exploration

#### 1- Relationship between 'duration_sec' and 'user_type'
- We know from univariate exploration that the largest percentage of riders are subscribers.
- The median value of subscribers trips duration are about 500 sec while of customers are about 850.
- There's a big number of outliers here but the most interesting is that customers trips are usually longer than subscribers.
- Customer trips durations are usually about 500 to 1200 sec while the subscribers trips duration are usully about 300 to 750 sec.

#### 2- Relationship between 'member_birth_year' and 'user_type'
- There's a positive relationship between 'member_birth_year' and 'duration_sec'.
- Starting from 40's borns to 2000's borns the durations increase from 500 sec up to more than 4k sec.

### C- Check relationships between features and each other
There's a strong correlations between some features such as:
- start_station_latitude vs start_station_longitude (-0.678105)
- start_station_latitude vs end_station_latitude (0.990130)
- start_station_longitude vs end_station_latitude (-0.682598)
- start_station_longitude vs end_station_longitude (-0.685085)
These relationships worth to draw but unfortunately none of these features affect the duration

### D- Multivariate Exploration
Relationship between 'member_birth_year' & 'duration_sec' encoding 'user_type' (nominal) using color
- This is most intresting plot I could found.
- Duration is increase as member birth year grows.
- There's 2 types of users: Customer or Subscribers.
- Most of trips are made by subscribers while the longest trips are made by customers.
