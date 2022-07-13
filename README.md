# Unemployment-Mental-Illness

Link to Presentation Slides: https://docs.google.com/presentation/d/1FV5DZINW1crgByETuaF4vUng_kAeqYqvMTowfl_Ye3A/edit?usp=sharing

## Intro
This presentation acknowledges how mental illness and symptoms without a diagnosis can influence possible employment. The following research question and hypotheses had been made.

The research question is: Does being diagnosed with having a mental illness have a strong effect on unemployment? 

This dataset was done by paid respondents on Survey Monkey in a general population. We cleaned the data and got 294 total participants. We looked at employment and mental illness &  the following symptoms : lack of concentration, anxiety, depression, obsessive thinking, mood swings, panic attacks, compulsive behavior, and tiredness

## Methods 

In our first hypothesis, we look at whether being diagnosed with a mental illness would put individuals at a disadvantage in terms of being employed. We ran logistic regression using mental illness as the variable and employment as the prediction task. 

In our second hypothesis, we looked at which symptoms had the most significant effect on being unemployed. For our first method, we ran logistic regressions using each mental illness symptom as a 1-variable predictor to see if any of the predictors were significant. For our second method, we used best subset selection, which generated every combination of models including every predictor, to see which combination of symptoms would have the highest effect on being unemployed. We then ran multiple logistic regression on the model that had the lowest mean squared error to create the regression table which allowed us to calculate the log-odds ratio. 

In addition, we performed a 5-fold cross-validation for both methods to calculate the accuracy using the proportion of correctly labeled cases which included the true positives and true negatives. We would then choose the model with higher accuracy to pursue.

The reason we used logistic regression was because this was a binary classification problem, meaning we were looking at whether someone was employed or not. We also decided to use best subset selection because we wanted to find the best subset of predictors that best predict employment. 

## Results (1)

Looking at our first descriptive statistic’s bar graph, it appears to be there's a significant relationship between the employment rate and mental illness. However, going down to inferential statistics, where we fit a logistic regression. Mental illness's p-value turned out to be much greater than our significance level of 0.05. This indicates mental illness is not significant, therefore our alternative hypothesis is not supported. After performing a 5-fold cross-validation, we produced an accuracy score of 59%. 

## Results (2) 

Moving onto the next hypothesis, we processed the data by scaling to fit to derive these multiple bar graphs. This graph indicates the frequency of each symptom's of unemployed and employed count. Just by looking at this graph, we can assume that those who are unemployed suffer from each symptom more than those who are employed. ‘As you can see lighter green bar is relatively higher than the dark green bar graph throughout all the symptoms’

For our inferential stats, after performing best subset selection, we were able to get the lowest MSE from the model that included all 8 symptoms. By performing logistic regression, we found that panic attacks was the only predictor with a p-value of 0.033.   Looking at its coefficient, which tells us, a 1 unit increase in panic attacks leads to a 0.92 unit decrease in employment. After calculating the log odds using the beta coefficients, we found that the probability of being unemployed with 1.00 symptoms of panic attack is 49.52 percent. After performing a 5-fold cross-validation, we produced an accuracy score of 66%. 

## Discussion

There were a few limitations that may have affected our data and results in our work. The survey was taken by random sampling, therefore the number of employed and unemployed individuals were unequal. We also have to consider the possibility that those who take the survey may falsify their data (either recording symptoms that are undiagnosed and/or denying symptoms). Due to the nature of an online mental illness survey, it may have appealed more to those with mental illnesses or those who experience more severity in symptoms are not participating. An online setting is also not natural, we would prefer a more naturalistic approach in order to increase our internal validity.

Regardless of the fact that the findings do not support the hypotheses fully, the findings of this project suggest that mental illness is common in both employed and unemployed individuals. Our project aims to emphasize the importance of speaking about mental health in the workplace and acknowledging the difficulties that they bring to those who want to be employed. We’d like to encourage further exploration in terms of evaluating the possibility in a larger sample of what identification of certain illnesses and more severe symptoms can lead to. 
