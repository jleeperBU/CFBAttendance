# CFBAttendance-DSC-630
Introduction

  College Football is one of the largest sporting leagues within the United States and can have lucrative costs and revenues associated with it. It is interesting to determine what considers a program successful, as well as external factors that may be at play when it comes to how those programs have longevity and excitement within the school and the fanbase. For these external factors, we can come away with a question that would be able to be answered through analytical data: Does team performance impact attendance, or does attendance impact team performance? 

  The answer to this question would be either correlation or regression. While correlation would help determine if there is a relationship between the two, it will not indicate which one is causing the other to change. For regression, this would allow a model to determine how one variable predicts another. Within this model, I want to investigate both correlation as well as regression.
	
 I believe this problem to be extremely interesting, as within predictive analytics, we can determine how successful a program could be and what factors could lead to those specific outcomes. If a school can maintain a high rate of attendance, what would be their winning percentage? However, we can also go about this in the opposite direction – if a team has a high win percentage, as well as has maintained a high win percentage in previous seasons, how will their attendance be?
This data can help schools who are looking to bolster their attendance for their football games or could go in the opposite direction and could look to produce a better output on the field and their outcomes. This project could lead to many different individual parties that would find this data interesting – the colleges themselves as well as fans of the program. If it was likely that a higher attendance led to a better outcome, fans would be more likely to attend if they are wanting to see the team succeed, as well as the colleges would want to help attendance for better revenue and results at the end of the season.
	
 The data I have collected for this is from Kaggle.com, with data collected by Jeff Gallini. This data features many different factors, such as fill rate, broadcasts, weather, opponent information, as well as team information & conference information for each of the games from 2000-2018 for 63 different D1 FBS schools. Within the data information, Jeff states that his information does come from Wikipedia for the public information, so it does lack total integrity, but many of the specific instances can be checked if any anomalies have occurred.

This data is useful for this problem because we can determine many factors that could be touched upon through what is involved within its information. Does any level of rain or snow impact attendance and fill rates for the stadium? Does total stadium size affect how many people would go?  Does a team’s previous record matter for schools that are in power conferences such as SEC? Does the rank of the opponent also matter for the outcome?

For this project, since we are wanting to possibly go through two separate routes with the data we have, we can have bidirectional analysis to determine if attendance impacts performance or vice versa. With this being said, many different models can come to mind when it comes to predicting this information. We could have a linear regression model to predict a continuous outcome based on some predictor variables, such as having a model predict attendance using team performance metrics, and another for predicting the team performance using the attendance metrics as well as the other factors that can come into play. Logistic regression tests can also be used to determine the probability of a win based on attendance. We can also use a Granger Causality Test, which can determine whether past attendance levels can predict future team performance and vice versa. This can help us understand the direction of causality between the two variables being examined.

Methods/Results

With these models, I hope to test the different aspects of the relationship between team performance and attendance, and this could provide strong insights into the dynamics of how attendance is determined. 

For linear regression tests, the evaluation metrics we will be focusing on would be our R-squared value, which will measure the variance in the dependent variable, our RMSE, which will provide insight into the average magnitude of the error in our predictions, and MAE, which will measure the average distance between the actual values and predicted values.

For logistical regression models, we will be testing the accuracy, precision, recall, and F1-Score, which will give us the percentage of correct predictions, the number of true positives in our predictions.

For Granger Causality Test, we will be evaluating our p-value, which will prove that if the p-value is below a significance level we can conclude that past attendance helps future performance, or vice versa, providing evidence for a causal relationship.

With the information we have, I hope to learn more about how accurate our predictions can be, as well as discovering exactly what our proposed question’s answer would be.

Ethical Considerations

There are some risks and ethical implications that could be determined through this data. There could be bias and misinterpretation of the results, as some schools may feature a high attendance even if the performance is not up to standard. For example, Academy schools with D1 college football programs such as Navy & Army have a mandatory attendance for all cadets, which would skew the numbers for a higher fill rate. Other schools, such as West Virginia University, feature a program for free tickets for students for every game, which are going to be included in attendance even if a student does not attend. However, for the data that I will be using, this will be only used as a base level examination and testing. It will hopefully be able to determine exactly how the two variables, performance & attendance, can work together, but external factors that cannot be seen or posted within a spreadsheet will not be figured into the equation. 

Data Questions & Answers

For this assignment, the dataset contains variables that provide key information for both team performance (such as win/loss, ranking, and conference data) and attendance (fill rates, game day conditions, and more). This dataset allows for bi-directional analysis, where I can examine both the impact of performance on attendance and the effect of attendance on performance. Since the data spans several seasons (2000-2018) and includes various schools and conditions, there is enough information to answer these questions using statistical models like correlation and regression. However, careful consideration of external factors, such as weather and opponent rankings, is necessary to account for potential errors in my evaluation.

Visualization Possibilities

Several visualizations will help in explaining the relationship between attendance and team performance:

1.	Scatter plots: These can visualize the correlation between attendance and performance metrics. Plotting attendance against win percentage or rank would highlight any potential trends or patterns.

2.	Line graphs: These can be used to show trends over time. For example, plotting average attendance and average team performance for a school over the years could help identify long-term trends.

3.	Bar charts: Visualizing average attendance by team performance tiers (for example, ranked vs. unranked teams) will help illustrate any differences across categories.

Data Adjustments

While the data is comprehensive, adjustments may be necessary to better handle external variables that could affect the evaluation. For instance, controlling weather conditions at certain schools in colder regions may reduce the noise in the data and improve model accuracy. Additionally, it would be beneficial to consider breaking the analysis down by school size, conference, or region to see if the relationship between attendance and performance differs across these dimensions.

As for the driving questions, the key question—whether attendance impacts performance or vice versa—remains relevant. However, considering the bi-directional nature of the analysis, I could refine the driving questions to focus on the direction and strength of the relationship. This could also include an exploration of the factors that most strongly influence this relationship.


Preparing Data

 For my data to be prepared, there needs to be a full understanding of what we are trying to find – this is a performance calculator, and an attendance calculator. Within the spreadsheet, I have added a new column of Cumulative Win Percentage – this takes the team’s current wins and losses, adds them up, and then creates a percentage of what is within the dataset. This will be my performance calculator, while the attendance calculator is already helpful with Fill Rate – Attendance divided by Stadium Capacity.

 The next step is to help with the previous new percentage. For this to be able to accurately predict in a better way, I have also removed the first year from each team, as I only have 2000-onwards, this still gives a good 2001-2018 basis to work with a more accurate win percentage over the entire sheet. For teams that have been added to the FBS since 2000, such as Ball State in 2006, I needed to remove their first year as well.
 
After completing these steps, I then went forward with the Linear Regression Model.

Linear Regression Model

 For this specific assignment and assessment, I chose to use a Linear Regression Model for determining if win percentage affects Fill Rate, and our Mean Squared Error is 3.5%, which means that our model is giving a prediction that is close to the actual value.
 
 
	
 However, when determining the reverse, where fill rate affects performance, I did not have great figures.
   
	
 For another test, I would like to perform a Granger Causality Test.



Granger Causality Test
	
 Within this, I wanted to Determine how these Cumulative Win Percentage and Fill Rate was in a bidirectional analysis such as the Granger Causality Test, and I was able to get these numbers.
  
 













For our graphing, we can see that P-values are rising each period, our F-Stat is lowering each period, and that they are still considered to have bi-directional causality.
 
 Interpretation
	
 Within these models that I have gone over, I have determined that for our linear regression models, the data shows that team performance is effective for attendance, and that attendance is not effective for team performance. However, when using Granger Causality, we have determined that these do have bidirectional causality, which leads me to believe that there is an underlying influence that each number does have on one another. This is, I believe, to be due to a feedback loop – as A causes B, B then causes A to react. This means that this is not just a correlation between the two variables but that there is a causal relationship between them.

Conclusion/Recommendations

 I believe that within this data I have found that there is a relationship between the two – team performance and attendance. Within our Granger Causality Test, our p-values were low that they remained statistically significant, although the F-test depreciation does lead me to believe there may be something to look to for potential issues. Although this may cause potential issues when comparing stats between years and team performance, we have been able to determine that the relationship between the two is correlated between each other, while regression is applicable between team performance towards attendance. 

 For this model, I do believe that they do need work to be ready for deployment towards each individual team and potentially other leagues who may be interested in this information. For this to be made applicable to each individual team, they need to have more information applied that may not be accessible to the current public but will be accessible to those teams. How much each ticket costs, the student tickets vs. regular tickets, and other variables that may affect these numbers. However, when comparing the entire league for college football, we can determine that performance affects attendance in a vacuum, with other variables needed to know exactly why this is the case and how the numbers would truly fair.
	
 For ethical concerns, mine does not have any specific concerns. However, if this were to be deployed and useful for a team, they may have more data that should not be made available to the public, such as students’ information. However, at a base level, this has been a great way for this data to be carried and explored.

References

Gallini, J. (2019, December 9). College football games (2000 to 2018). Kaggle. https://www.kaggle.com/datasets/jeffgallini/college-football-attendance-2000-to-2018 

Hakes, T. (n.d.). NCAA football teams made more money than many NFL teams in 2015 [infographic]. uCribs. https://www.ucribs.com/blog-post/ncaa-football-teams-made-more-money-than-many-nfl-teams-in-2015-infographic/ 

Hughes, G. (2024, June 28). College Athletics’ 25 powerhouses who produce the most revenue entering 2024. 247Sports. https://247sports.com/longformarticle/college-athletics-25-powerhouses-who-produce-the-most-revenue-entering-2024-233312519/#2438994 

