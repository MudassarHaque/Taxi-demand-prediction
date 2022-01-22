# NYC-Taxi-demand-prediction

Taxi demand precidiction based on previous pickup data.

## Data Information
Ge the data from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml (2016 data) The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)

2.1  Information on taxis:
Yellow Taxi: Yellow Medallion Taxicabs
These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. The number of taxicabs is limited by a finite number of medallions issued by the TLC. You access this mode of transportation by standing in the street and hailing an available taxi with your hand. The pickups are not pre-arranged.

For Hire Vehicles (FHVs) 
FHV transportation is accessed by a pre-arrangement with a dispatcher or limo company. These FHVs are not permitted to pick up passengers via street hails, as those rides are not considered pre-arranged.

Green Taxi: Street Hail Livery (SHL) 
The SHL program will allow livery vehicle owners to license and outfit their vehicles with green borough taxi branding, meters, credit card machines, and ultimately the right to accept street hails in addition to pre-arranged rides.

Credits: Quora

## Data Collection
We Have collected all yellow taxi trips data from jan-2015 to dec-2016(Will be using only 2015 data)

## ML Problem Formulation
Time-series forecasting and Regression


- To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.
To solve the above we would be using data collected in Jan - Mar 2015 to predict the pickups in Jan - Mar 2016.

## Performance metrics
We have chosen our error metric for comparison between models as MAPE (Mean Absolute Percentage Error) so that we can know that on an average how good is our model with predictions and MSE (Mean Squared Error) is also used so that we have a clearer understanding as to how well our forecasting model performs with outliers so that we make sure that there is not much of a error margin between our prediction and the actual value

Mean Absolute percentage error. 
Mean Squared error. 


## conclusion

Regions are divided by 2 miles pickup cluster using kmeans, The avg speed in Newyork speed is 12.45miles/hr, so a cab driver can travel 2 miles per 10min on avg therefore 10 min-interval is taken to predict the pickup rate for particular cluster/region for next 10 min interval


## results


|       Method      |      train_mape     |      test_mape      |
| :-: | :-: | :-: |
| Baseline model                   | 0.14005275878666593 | 0.13653125704827038 |
| Exponential Averages Forecasting |  0.13289968436017227 | 0.12936180420430524 |
| Linear_regression |  0.1332580544668445 | 0.12905387841231855 |
|   Random_forest   | 0.08487831185722436 |  0.1214220590315342 |
|        XGB        | 0.11932327268070465 | 0.11991759974616668 |



Footnote:
In the given notebook we are considering only the yellow taxis for the time period between Jan - Mar 2015 & Jan - Mar 2016
