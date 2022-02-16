# MechaCar_Statistical_Analysis

***RESOURCES***
Software:R, RStudio, dplyr library
Data Sources: MechaCar_mpg.csv, Suspension_Coil.csv

***OVERVIEW***
The purpose of this challenge was to assist Jeremy with the new protoyype MechaCar production troubles at AutosRUs. The analytical components addressed were as follows:
- multiple linear regression analysis to predict the mpg (miles per gallon) for the MechaCar prototypes
- perform summary statistics on the PSI (pounds per square inch) of the manufactured lots of suspension coils
- perform t-tests to determine if the manufactured lots are stastically different from the mean
- design a statistical study that compares the MechaCar's performance to that of other vehicles
- perform a summary interpretation for each of the aforementioned statistical analyses


***RESULTS***
For this analysis the datasets of two csv files were considered; the MechaCar_mpg.csv and the Suspension_Coil.csv. The analytical components were then broken down into 4 Deliverables with the inclusion of their respective summaries.

## DELIVERABLE 1: Linear Regression to Predict MPG
The MechaCar_,mpg.csv dataset contained the test results for 50 prototype MechaCars and their performance in terms of vehicle length, weight, spoiler angle, drivetrain and ground clearance. Subsequently, a predictive linear model of regression analysis was composed to determine the mpg of the MechaCar prototypes via RScript and the utilization of the lm() and summary() functions, as depicted in FIGURES 1 through 3.

<img width="1440" alt="D1-Import MechCar_mpg" src="https://user-images.githubusercontent.com/90135381/153728155-5b0769cf-fc04-4128-b140-0ecc401824cb.png">

                              FIGURE 1: Import MechCar-mpg


<img width="1440" alt="D1-linear regression with lm()" src="https://user-images.githubusercontent.com/90135381/153728164-3226317d-0f0a-4f7f-b4a3-e8c0ed95a316.png">

                              FIGURE 2: Linear regression 


<img width="1440" alt="D1-p-value:r squared" src="https://user-images.githubusercontent.com/90135381/153728175-b6a04224-2fe3-4f39-aad5-c574a5ffbed9.png">


                              FIGURE 3: p-value and r squared
                              
***SUMMARY***

The variables/coefficients which provided a non-random amount of variance to the mpg values in the dataset are:

The slope of the linear model is considered to be:

The linear model does/not predict mpg of MecharCar ptototypes because:

## DELIVERABLE 2: Summary Statistics on Suspension Coils
This segment of the analysis addressed the Suspension_Coil.csv dataset and the results from multiple production lots, in terms of the consistency of weight capacities. As illustrated in FIGURES: 4 through 7, tables were created in R representing the statistical data for total and lot summaries for the suspension coil's continuity across manufacturing lots. The PSI metrics for each lot; mean, median, variance and standard deviation, were calculated in a dataframe with group_by() and summarize() and formulated to tables.

<img width="1440" alt="D2-total_summary" src="https://user-images.githubusercontent.com/90135381/153728186-db7bbd66-a867-411f-acf8-0fcdb085ae37.png">

                              FIGURE 4: total_summary


<img width="1440" alt="D2-lot_summary" src="https://user-images.githubusercontent.com/90135381/153728206-68af7332-402d-4936-9b52-20a5c12774fb.png">


                              FIGURE 5: lot_summary

<img width="1440" alt="MechaCar_mpg" src="https://user-images.githubusercontent.com/90135381/153728216-93c379d7-29bc-4afe-b096-b0f62c143621.png">


                              FIGURE 6: MechaCar_mpg


<img width="1440" alt="Suspension_Coil" src="https://user-images.githubusercontent.com/90135381/153728226-46866c3f-60d7-452f-91d1-b0a85c050766.png">


                              FIGURE 7: Suspension_Coil
                              
***SUMMARY***

For this deliverable, consideration was taken to address the design specifications for the MechaCar suspension coils and their variance not exceeding 100PSI. The current manufacturing data does/not meet this design specification for all lots in total and each lot individually because;


## DELIVERABLE 3: T-Tests on Suspension Coils
T-Tests were then executed to determine if the total lots and the individual lots were statistically different from the population mean of 1,500 PSI. This was completed in RScript via the t.test() function with it's subset() argument.


<img width="1440" alt="D3-one sample t-test" src="https://user-images.githubusercontent.com/90135381/153728252-8c2595fe-6084-4025-98df-0a22332e86c0.png">


                            FIGURE 8:  sample t-test


<img width="1440" alt="D3- lots 1-3  stats" src="https://user-images.githubusercontent.com/90135381/153728263-25b83cf4-1b13-4094-b41d-98bd10ba7e1f.png">


                            FIGURE 9: lots 1-3 stats
                            
***SUMMARY of T-Tests on Suspension Coils***

The t-test results indicate the following: 
sample t-test:

lot 1 t-test:

lot 2 t-test:

lot 3 t-test:

## DELIVERABLE 4: Study Design: MechaCar vs Competition
A ststistical study was formulated to compare the performance of the MechaCar vehicles against the performance of other manufacturers.
The MechaCar performs against the competition.... the metrics that would be of interest to the consumer are:

-cost:
-fuel efficiency:
-horsepower:
-maintenance:
-safety:

Metrics to test:
Ho/Ha 
tests to address hypothesis
data required to run the statistical test




***REFERENCES*** BSC, Google, GitHub, StackOverflow
