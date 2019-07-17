# Predicting rate of crime against women in the National Capital Territory of Delhi for the year 2015.

## Data Description
The dataset contains the data for crime rate against women in the NCT of Delhi aggregated by county.

## Data Attributes

1. county - county identifier
2. year - 2015
3. crmrte - crimes committed per person
4. prbarr - 'probability' of arrest
5. prbconv - 'probability' of conviction
6. prbpris - 'probability' of prison sentence
7. avgsen - avg. sentence, days
8. polpc - police per capita
9. density - people per sq. mile
10. taxpc - tax revenue per capita
11. west - =1 if in western Delhi
12. central - =1 if in central Delhi.
13. urban - =1 if in south Delhi.
14. pctmin15 - perc. minority, 2015
15. wcon - weekly wage, construction
16. wtuc - wkly wge, trns, util, commun
17. wtrd - wkly wge, whlesle, retail trade
18. wfir - wkly wge, fin, ins, real est
19. wser - wkly wge, service industry
20. wmfg - wkly wge, manufacturing
21. wfed - wkly wge, fed employees
22. wsta - wkly wge, state employees
23. wloc - wkly wge, local gov emps
24. mix - offense mix: face-to-face/other
25. pctymle - percent young male

## Objective
1. To perform **univariate** and **bivariate exploratory analysis** of the dataset provided.
2. To develop a suitable **linear model with crmrte as the dependent variable** based on the EDA findings.
3. To explain the various aspects of the model used.

## Data Analysis & Data Cleaning

1. **The last column was getting read as 'object' data. It was found to be due to the special symbol at the last row, last column 0.074198931'**. Removed the special symbol from input csv file, to fix it.

2. It is to be noted that the **maximum value of probability features, prbarr & prbconv, are > 1** which is a data anomaly. prbpris & pctymle are found to be < 1.

3. There are 91 entries for all the 25 columns. Hence, there is **no missing value in the input dataset. Thus, no need to do data imputation** or to drop any feature.

4. The zeros for features, west, central and urban are expected, as the data is inherently boolean


**Observations**_<br/><br/>
_**From above analysis, it is found, that some rows have to be dropped before doing regression analysis. The probability values of some rows are found to be > 1 and location of one row was found to be both ’west’ and ’central’ at the same time. We will drop these rows before building the model. The special character error in the input dataset is also fixed.**_

## Univariate Analysis

Univariate visualization   provides summary statistics for each field in the raw data set. It is conducted **to find out how much a single feature in the dataset** would be helpful to determine the target feature, here in this case, crime rate.

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Crime-Analysis-Prediction/blob/master/images/uva.PNG">
</p>

