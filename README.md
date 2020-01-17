# Project 2: Ames Housing Project : 


---
### Problem Statement

Collegeboard has informed us that there has been a sudden drop in overall average SAT scores in some states from the year 2017 to 2018.  Whether this is a random phenomena or not, we wanted to use statistical analysis to derive if there is any particular reason behind such phenomena. 


### Executive Summary

In order to begin any sort of analysis, we first needed to use the provided dataset of SAT and ACT Scores from the years 2017-2018. 
With the given dataset, we first needed to do a thorough cleaning of the data to ensure there are no errors in our data especially in the form of inaccuracy or misinformation.  Then we aggregated all our data into a final version of the data so that we can investigate any trends and/or correlations that may provide us with helpful insights. By comparing our dataset to the original source listed below, we were able to fix few mistakes in our dataset (which we corrected) to ensure the accuracy of the dataset we will be using.

Then, we used Exploratory Data Analysis to summarize the main characteristics of our data as well as prepare ourselves for the data visualizations we will be creating.  With the dataset we cleaned and fine-tuned, we were able to verify our original problem statement which showed a clear trend in the decline in overall average SAT scores in some states from the year 2017 to 2018 (using a sorting method) as their participation rate by state had skyrocketed. 

In particular, we decided to take a look at the top 3 states with the largest decline of SAT scores from 2017 to 2018 which were Colorado, Illinois, and Utah.

With further outside research, we then were able to identify that some of the states such as Colorado, Illinois had enforced a new policy amongst the graduating class of 2018 when the graduating class of 2017 were not obligated by the same policies.  

By a reasonable deduction, we were able to deduce that enforcement of a certain examination (such as the SATs) on the student body as a graduation requirement actually negatively impacted the results due to the fact that the students may not well be prepared for such examinations (because they had not been aware of such criteria for academic studies in the past).  

As far as Utah was concerned, we were able to verify using outside sources (SAT Suite Assessments Annual Report by state, provided by the Collegeboard) that there had been a mistake in our dataset as well which had made us think that there was a sudden drop in the overall SAT score results when in actuality it had only been dropped by an insignificant value (2017 average of 1238 to 2018 average of 1230) of 8 points. 

### Conclusion

For the the two states Colorado & Illinois, there was definitely a strong correlation between the two specific states introduction to the new policies mandating the SAT examination as a high school graduation requirement and the decline in the overall average of their respective SAT scores. 

For Utah, we were able to conclude that there was actually no sudden decline in SAT scores but rather was a "false alarm" on our data analysis due to misinformation provided by the collegeboard's dataset through further research.

### Recommendation

It is evident that when a students are suddenly introduced to a new testing material, they will need more time to adjust as well as requiring a more formal education on behalf of the relevant material in order to better prepare them for these tests.  As a response, if a State were to change their policy to enforcing such examinations, more thoughts need to be put in to the educational system in order to not intentionally sabotage the student's future due to poor testing grades.


### DATA Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT/SAT|The State each row of scores the dataframe represents| 
|sat_participation_rate_17|float|SAT|Participation rate from the corresponding State for SAT scores in the year 2017| 
|sat_reading_writing_17|float|SAT|The average score of Reading & Writing from the corresponding State for SAT scores in the year 2017| 
|sat_math_17|float|SAT|The average score of Math from the corresponding State for SAT scores in the year 2017| 
|sat_total_17|float|SAT|The average combined score of Reading & Writing and Math from the corresponding State for SAT scores in the year 2017 | 
|act_participation_rate_17|float|ACT|Participation rate from the corresponding State for ACT scores in the year 2017| 
|act_english_17|float|ACT|The average score of English from the corresponding State for ACT scores in the year 2017| 
|act_math_17|float|ACT|The average score of Math from the corresponding State for ACT scores in the year 2017| 
|act_reading_17|float|ACT|The average score of Reading from the corresponding State for ACT scores in the year 2017| 
|act_science_17|float|ACT|The average score of Science from the corresponding State for ACT scores in the year 2017| 
|act_final_average_17|float|ACT|The average combined score of English, Math, Reading, and Science from the corresponding State for ACT scores in the year 2017| 
|sat_participation_rate_18|float|SAT|Participation rate from the corresponding State for SAT scores in the year 2018| 
|sat_reading_writing_18|float|SAT|The average score of Reading & Writing from the corresponding State for SAT scores in the year 2018| 
|sat_math_18|float|SAT|The average score of Math from the corresponding State for SAT scores in the year 2018| 
|sat_total_18|float|SAT|The average combined score of Reading & Writing and Math from the corresponding State for SAT scores in the year 2018 | 
|act_participation_rate_18|float|ACT|Participation rate from the corresponding State for ACT scores in the year 2018|
|act_final_average_18|float|ACT|The average combined score of English, Math, Reading, and Science from the corresponding State for ACT scores in the year 2018| 


### Datasets

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018.csv)
- [Combined 2017-2018 Scores for ACT/SAT](./data/final.csv)

These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017, 2018 after they have been thoroughly cleaned.

#### Sources

The original dataset used for analysis were obtained from below.

SAT Data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/), 
ACT Data [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows).

Additional Data Cleaning was done for the state of Utah using the data obtained from below.

Utah SAT Data 2017 [here](https://reports.collegeboard.org/pdf/2017-utah-sat-suite-assessments-annual-report.pdf).
Utah SAT Data 2018 [here](https://reports.collegeboard.org/pdf/2018-utah-sat-suite-assessments-annual-report.pdf).


