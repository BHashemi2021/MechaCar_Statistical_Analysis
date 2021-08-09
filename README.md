# MechaCar Statistical Analysis
An Analysis Employing R Statistical Package

## Background
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this analysis, we will help Jeremy and the data analytics team by performing the following tasks:
  1-	Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
  2-	Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
  3-	Run t-tests to determine if the manufacturing lots are statistically different from the mean population
  4-	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 

 
## Linear Regression to Predict MPG
In this analysis we used MechaCar_mpg.csv dataset containing MPG test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. The six variables of MechaCar_mpg.csv file are shown in Figure 1.

#### Figure 1: MechaCar_mpg.csv dataset and its variables at a glance

------------------------------
![1.1.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/1.1.png)

------------------------------
Having satisfied the assumptions for a linear regression analysis we set the study hypothesis as follows:
H0: The slope of the linear model is zero (m = 0) and no significant linear relationship exists between MPG and any of study variables.

Using R linear regression function ln(), we called the variables into th formula and calculated coefficient for each variable as shown in Figure 2.

#### Figure 2: The Calculated coefficient for each variable in the proposed linear regression model

------------------------------
![1.3.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/1.3.png)

------------------------------

•	Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    By significantly low p-values, vehicle_length (p-value=2.60e-12), and ground_clearance (p-value=5.21e-08) could provide nonrandom amount of variance to the mpg in this study.

• Is the slope of the linear model considered to be zero? Why or why not?
    Considering the significant p-values for at least two variables indicate that the slope of the linear regression is not zero and the two could provide variance to mpg in a non-random fashion.

• Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    Interestingly, the intercept (p-value=5.08e-08) has a significant p-value too. This indicates that aside from vehicle_length and ground_clearance, there might be at least another variable that could affect mpg. 

#### Summary
By at least tow variables (vehicle_length and ground_clearance) having significant p-values, we could reject the null hypothesis and state that the slope in the model is not zero. The manufacturer could transform, scale or optimize these two variables as they could affect mpg. In conclusion, it seems the linear model did not fully predict mpg as the intercept also had a significant p-value.



## Summary Statistics on Suspension Coils 
To manouver around ground_clearance variable, the MechCar automaker needs to evaluate suspension coils provided from different suspension manufacturers to choose the ones that satisfy the design standards of the company. Figure 3 shows a sample of suspension coils available.


#### Figure 3: Suspension coils

------------------------------
![2.1.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/2.1.png)

------------------------------

The mean of suspension coils PSI metric is 1498.78  (+/- SD = 7.9). The summary table calculated from the available suspension coil lots will be very helpful to choose the ones that provide the company design standards (Figure 4).

#### Figure 4: The total summary of suspension coils

------------------------------
![2.2.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/2.2.png)

------------------------------

• Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
    The suspension coils from three manufacturing lots seem to meet those standards as their mean is or is close to 1500 PSI.

To summarize:
As the design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Moreover, we had earlier noticed (Figure 4), that the "variance" of the suspension coils could be tolerated at around 62 PSI. Adding the variance of 170 to a mean of 1496 PSI from the third manufacturing lot, renders this lot outside the expected range of MechaCars standard design for suspension coils.


#### Figure 5: Lot summary
------------------------------
![2.3.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/2.3.png)

------------------------------




## T-Tests on Suspension Coils
briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.
•	An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population (5 pt)
•	An RScript is written for three t-tests that compare each manufacturing lot against mean PSI of the population (10 pt)
•	There is a summary of the t-test results across all manufacturing lots and for each lot (5 pt)


#### Figure 6: 
------------------------------
![3.1.png](https://github.com/BHashemi2021/MechaCar_Statistical_Analysis/blob/main/Resources/images/3.1.png)

------------------------------


## Study Design: MechaCar vs Competition
1.	Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
2.	In your description, address the following questions:
•	What metric or metrics are you going to test?
•	What is the null hypothesis or alternative hypothesis?
•	What statistical test would you use to test the hypothesis? And why?
•	What data is needed to run the statistical test?


(((((After you’ve completed the technical analysis for each deliverable, provide a short summary of the results in the README.md of the analysis. For the final deliverable, you’ll write up a short description of the study design for additional statistical analysis. In the written summaries, we would like you to think critically about your analysis, not demonstrate mastery of automotive manufacturing.)))))


•	A metric to be tested is mentioned (5 pt)
•	A null hypothesis or an alternative hypothesis is described (5 pt)
•	A statistical test is described to test the hypothesis (5 pt)
•	The data for the statistical test is described (5 pt)


#### Software Employed
  * R (x64, 4.1.0)
  * RStudio for Windows 
  * Microsoft csv files (x64, 2016)
 
  
  
