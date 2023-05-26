# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring climate data of Singapore

### Project Objective
The EMA (Energy Market Authority) would like to know if there is any impact of weather conditions in Singapore on household electricity consumption.

Given that the weather is set to become more extreme (eg. heat waves, more rainy days, large storms) due to climate change, insights into such trends can help EMA anticipate any unexpected over/under-demand scenarios which will help optimize operations.


### Datasets Used:
* [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022
* [`rainfall-monthly-highest-daily-total.csv`](./data/rainfall-monthly-highest-daily-total.csv): Daily highest rainfall by month recorded in mm(millimeters) from 1982 to 2022
* [`relative-humidity-monthly-mean.csv`](./data/relative-humidity-monthly-mean.csv): Mean monthly humidity recorded in % from 1982 to 2022
* [`sunshine-duration-monthly-mean-daily-duration.csv`](./sunshine-duration-monthly-mean-daily-duration.csv): Mean daily sunshine hours by month from 1982 to 2022
* [`surface-air-temperature-monthly-mean.csv`](./data/surface-air-temperature-monthly-mean.csv): Mean monthly temperature in deg Celsius from 1982 to 2022
* [`wet-bulb-temperature-hourly.csv`](./data/wet-bulb-temperature-hourly.csv): Wet bulb temperature taken hourly in deg Celsius from 1982 to 2022
* [`changi-public-private-energy.csv`](./data/changi-public-private-energy.csv): Monthly demand for public and private households in Changi in kWh from 2005 to 2022


### Data Dictionary
|Feature|Type|Dataset|Description|
|:---|:---|:---|:---|
| maximum_rainfall_in_a_day | float | rainfall-monthly-highest-daily-total | Maximum rainfall for the month in mm |
| no_of_rainy_days | int | rainfall-monthly-number-of-rain-days | No of rainy days for the month |
| total_rainfall | float | rainfall-monthly-total | Total rainfall for the month in mm | 
| mean_rh | float | relative-humidity-monthly-mean | Mean relative humidity for the month in % |
| mean_sunshine_hrs | float | sunshine-duration-monthly-mean-daily-duration | Mean daily sunshine duration for the month in hours |
| mean_temp | float | surface-air-temperature-monthly-mean | Mean temperature for the month in degree Celsius |
| wet_bulb_temperature | float | wet-bulb-temperature-hourly | Mean wet bulb temperature for the month in degree Celsius |
| changi_public_housing | float | changi-public-private-energy | Monthly energy demand in kWh of public housing in Changi |
| changi_private_housing | float | changi-public-private-energy| Monthly demand in kWh of private housing in Changi |



### Key Takeaways
* There are some trends showing that there is increased energy usage during months with low mean total rainfall and low mean no of rainy days 

* Some correlations such as:
  - As wet bulb temp ↑ , energy consumption for Changi private housing ↑ 
  - As mean temp ↑, energy consumption for Changi public housing ↑ 



### Recommendations:
It would benefit EMA to include reviews of weather forecasts during energy demand forecasting in order to prepare for an increase in household energy usage during periods of:
* Low total rainfall by month
* Low number of rainy days in a month
* High wet bulb temperature
* High mean temp

