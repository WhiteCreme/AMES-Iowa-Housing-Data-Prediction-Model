# Project 2: AMES Iowa Housing Data Prediction Model


### Table of Contents:
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Conclusion](#Conclusion)
- [Recommendation](#Recommendation)
- [Data Dictionary](#Data-Dictionary)
- [Datasets](#Datasets)
---
### Problem Statement

New developed mobile game needs testers to try out and see if the game entails sufficient and reasonable point calculation system based on features related to Car Garages  that users can pick up on without complicated computational skills. Using our regression model techniques, our ultimate goal is to come up with a proper prediction model that may accurately predict housing prices whether the predictors be garages or other more significant factors.



### Executive Summary

In order to begin any sort of analysis, we first needed to load the Ames Iowa Housing datasets for train & test datasets.  After the initial reading of the csv files, we needed to study the data dictionary provided a little bit as well.  Fortunately, a detailed data dictionary was provided as well although we did find couple incorrect interpretations/column names but this was easily identifiable as we slowly compared each of the 80 columns in the dictionary along with the given dataset. 

One of the first things we noticed was that the train dataset had an extra column named "SalePrice" which is what we were trying to calculate on the test dataset.  As we started diving into Exploratory Data Analysis to fully comprehend our dataset, we noticed that these particular datasets had a lot of missing values that we needed to account for.  In order to  ensure that we can come up with an accurate prediction of 'SalePrice' on our test set (to our best ability), we first needed to fully comprehend the 82 variables adressed in the data dictionary.  

First, we wanted to convert the dataset to a complete numeric dataset in order to be able to apply a linear regression to be able to come up with a prediction for the test dataset's 'SalePrice'.  Using the data dictionary, we were able to identify the different variable types (specifically nominal, ordinal, discrete, and continous) then began to identify the null values in each of the categories determine a process to convert all values to numeric type values.  As for the ordinal types, we succesfully used a dictionary to convert all string scoring scales into numeric values while we used get_dummies method on the nominal variables to create dummy columns of binomial values.

After the initial conversion, we checked the remaining null values individually to correctly apply a conversion method for each of them.  During the Process, we were particularly interested in features related to Garage due to the fact there were several related features that seemed useful initially.  One outlier we noticed specifically in the 'Garage Yr Blt' was that there seemed to be a typo for the year 2007 as 2207 which we were able to replace.  We also noticed that there were many missing values on the 'Garage Yr Blt' which we realized cannot be converted to 0 (unreasonable to assume any of the garages are 2000 years old) so we used a random.choice method to assign a random year that already exists in the feature column to replace the null values.  We then applied a get_dummy method as well on 'Garage Yr Blt' particularly so that we can create binomial values by 10 year bins.

We converted the remaining null values in other categories as well to complete the data cleaning process and were able to check if there were any correlations to the 'SalePrice' to see if any particular features were more noteworthy.  We also wanted to check for any significant correlations exist but later realized that strictly using garage related features was not the best approach to predict a 'SalePrice' on the test dataset.

As a result, we decided to use a single column heatmap of top correlations to identify the features we would rather use for our modeling process.  We attempted to use Linear Regression, LASSO Regression, and Ridge Regression to see if we can come up with an accurate prediction model.  

### Conclusion

Originally we used only garage related features to predict the 'SalePrice' using a linear regression however, the correlations already revealed that this might not be the best approach so we decided to use the top 10 features with the highest correlation against the 'SalePrice' to come up with a model.  As for our calculated R2 values on all 3 types of regression models, they all had similar results where the R2 on the test dataset was lower than the R2 values calculated on the training data.  This meant that our model was slightly Overfit and our model was not as accurate when it came to predicting the 'SalePrice' when applied to a non-familiar dataset such as the test data set.  As a result, we are not sure if this would be a good predictive model when applied to other cities however, it was actually not the worst so it might be a worthy investment to try to apply.  

### Recommendation

It is evident that according to the Ames Iowa Dataset, the overall quality of the house along with the Above Ground Level sq. ft. and total basement sq. ft. were the three best predictors.  Using this, we can recommend homeowners especially in the Ames Iowa Area if they were to want to flip a house or purchase a house for the best value, they should focus on these three particular features to affect the value of the house the most. We also noticed that the homes in Northridge Heights and Stone Brook had the highest prices so we do recommend to invest in homes in those area particularly to home buyers as well.  

### DATA Dictionary

http://jse.amstat.org/v19n3/decock/DataDocumentation.txt


### Datasets

- [train dataset](./dataset/train.csv)
- [test dataset](./dataset/test.csv)


These datasets were provided by Ames Assessor's Office in order to compute values for individual residential properties sold in Ames, IA from 2006 to 2010.  




