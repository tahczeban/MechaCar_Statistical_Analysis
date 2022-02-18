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
For this analysis the datasets of two csv files were considered; the MechaCar_mpg.csv and the Suspension_Coil.csv which were imported into RStudio (FIGURES: 1 through 3). The analytical components were then broken down into 4 Deliverables with the inclusion of their respective summaries.

<img width="1440" alt="D1-Import MechCar_mpg" src="https://user-images.githubusercontent.com/90135381/153728155-5b0769cf-fc04-4128-b140-0ecc401824cb.png">

                              FIGURE 1: Import CSV Files
                              
<img width="1440" alt="MechaCar_mpg" src="https://user-images.githubusercontent.com/90135381/153728216-93c379d7-29bc-4afe-b096-b0f62c143621.png">

                              FIGURE 2: MechaCar_mpg


<img width="1440" alt="Suspension_Coil" src="https://user-images.githubusercontent.com/90135381/153728226-46866c3f-60d7-452f-91d1-b0a85c050766.png">


                              FIGURE 3: Suspension_Coil
                              

## DELIVERABLE 1: Linear Regression to Predict MPG
The MechaCar_,mpg.csv dataset contained the test results for 50 prototype MechaCars and their performance in terms of vehicle length, weight, spoiler angle, drivetrain and ground clearance. Subsequently, a predictive linear model of regression analysis was composed to determine the mpg of the MechaCar prototypes via RScript and the utilization of the lm() and summary() functions, as depicted in FIGURES 4 and 5.



<img width="1440" alt="D1-linear regression with lm()" src="https://user-images.githubusercontent.com/90135381/153728164-3226317d-0f0a-4f7f-b4a3-e8c0ed95a316.png">

                              FIGURE 4: Linear regression 


<img width="1440" alt="D1-p-value:r squared" src="https://user-images.githubusercontent.com/90135381/153728175-b6a04224-2fe3-4f39-aad5-c574a5ffbed9.png">


                              FIGURE 5: p-value and r squared
                              
***SUMMARY***

1. The variables/coefficients which provided a non-random amount of variance to the mpg values in the dataset are: vehicle length and ground clearance significantly impact the MechaCar's mpg; however, weight, spoiler angle and AWD have p-values indicating random variance. There is a smaller probability coefficient(Pr(>|t|) for ground clearance and weight, while a larger probability coefficient and random variance are representative for AWD, spoiler angle and length, as depicted in FIGURES 4 and 5. 

2. The slope of the linear model is considered to be 'not zero', as the P-value = 5.35e-11, which is significantly less than the accepted norm of 0.05% confidence level. While some of the values are approximated to zero, there are no zero values; therefore, indicating a slope on the regression model.

3.The linear model does predict mpg of MechaCar ptototypes due to the fact that the r-squared is 0.7149, which indicates approximately 71% of predictions will be representative of the correlation of this statistical model.

## DELIVERABLE 2: Summary Statistics on Suspension Coils
This segment of the analysis addressed the Suspension_Coil.csv dataset and the results from multiple production lots, in terms of the consistency of weight capacities. As illustrated in FIGURES: 6 and 7, tables were created in R representing the statistical data for total and lot summaries for the suspension coil's continuity across manufacturing lots. The PSI metrics for each lot; mean, median, variance and standard deviation, were calculated in a dataframe with group_by() and summarize() and formulated to tables.

<img width="1440" alt="D2-total_summary" src="https://user-images.githubusercontent.com/90135381/153728186-db7bbd66-a867-411f-acf8-0fcdb085ae37.png">

                              FIGURE 6: total_summary


<img width="1440" alt="D2-lot_summary" src="https://user-images.githubusercontent.com/90135381/153728206-68af7332-402d-4936-9b52-20a5c12774fb.png">


                              FIGURE 7: lot_summary



***SUMMARY***

For this deliverable, consideration was taken to address the design specifications for the MechaCar suspension coils and their variance not exceeding 100PSI. The current manufacturing data does not meet this design specification for ALL lots in terms of total and individual lot summaries, as Lot#3 exceeds the value of 100 PSI, as summarized below: 

-total variance_PSI is 62.29 for the coils, which is less than 100PSI; therefore MEETS criteria
-lot 1(0.98) and 2(7.47) within 100 PSI; therefore, MEETS criteria
-lot 3 shows greater variance(170.29), which is significantly higher than 100 PSI; therefore, DOE NOT MEET criteria

## DELIVERABLE 3: T-Tests on Suspension Coils
T-Tests were then executed to determine if the total lots and the individual lots were statistically different from the population mean of 1,500 PSI. This was completed in RScript via the t.test() function with it's subset() argument.


<img width="1440" alt="D3-one sample t-test" src="https://user-images.githubusercontent.com/90135381/153728252-8c2595fe-6084-4025-98df-0a22332e86c0.png">


                            FIGURE 8:  sample t-test

<img width="1440" alt="Lots 1-3 with corrected population mean to 1500" src="https://user-images.githubusercontent.com/90135381/154585262-0c0bc7c2-7883-4d05-80d1-22779b6ccace.png">



                            FIGURE 9: lots 1-3 stats
                            
***SUMMARY of T-Tests on Suspension Coils***

The summarized t-test results indicate the following for the overall and individual manufacturung lots: 

- In FIGURE:8 the sample t-test was calculated and the following statistical data was compiled: mean of 1498.78 with a p-value of 0.06, which is greater than the significance level of 0.05. This means that the overall sample statistically approximates the population mean of 1500 PSI; therefore, the null hypothesis(Ho) should not be rejected.
- The remainder of the Lots and their respective analyses are illustrated in FIGURE 9:
lot 1 t-test: mean is 1500 the p-value of 1 indicates that the population and sample means of 1,500 PSI have no statistical difference between the two; therefore, the null hypothesis cannot be rejected. 

lot 2 t-test: mean 1500.02, p-value 0.61, dont reject Ho

lot 3 t-test:mean is 1496.14, p-value 0.04, less than 0.05, reject Ho, sample and pop mean are not stat difft

## DELIVERABLE 4: Study Design: MechaCar vs Competition
An additional statistical study was formulated to further compare the performance of the MechaCar vehicles against the performance of other manufacturer's vehicles. For a significant quantifiable analysis, it would be imperative that an adequate random sample size is chosen. A null(Ho) and alternative(Ha) hypothesis would then have to be generated and the appropriate analytical testing would be performed. Some of the additional metrics that would be of interest to both the manufacturer and the consumer are: cost, highway versus city fuel efficiency, horsepower and maintenance, to which a t-test could be executed for identifying the positive attributes for each, for comparison between manufacturer types. For the purpose of this study, however; safety rating can also be considered and emphasized and a t-test could be performed, as the statistics for this particular metric could be imperative to the mortality and morbidity rates of the users of the various types of vehicles. Due to the numerous components that could posssibly effect safety rating, one statistical investigation could include the integrity of the frame and it's materials/construction during collisions. The independent variable being the frame construction and the dependent variable being the safety rating, in terms of force of impact to test dummy driver with front and side impact tests.
In order to conduct the hypothesis testing, the mean, median, variance, standard deviation and respective p-values/confidence levels at 95% would be formulated, in conjunction with the null and alternative hypotheses:
1. H0(null hypothesis): There is no difference in safety rating (force of impact on test dummy driver) between the MechaCar and other vehicles' safety due to frame construction and materials.
2. Ha(alternative hypothesis): The MechaCar's safety rating is statistically and significantly greater than the mean of the competing manufacturer's vehicles, due to frame construction and materials.

***REFERENCES*** BSC, Google, GitHub, StackOverflow
