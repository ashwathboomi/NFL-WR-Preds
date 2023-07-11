# NFL-WR-Preds
## Using Machine Learning to predict the NFL WRs receiving yards

Using sci-kit learn machine learning library, a linear ridge regression model was implemented to predict each NFL WR's receiving yards in their successive season. Past 10 years of [NFL WR statistics](https://www.pro-football-reference.com/) were gathered as well as statistics reflecting each team's overall passing offense for those respective years. From the compiled data, there were more than 15 possible parameters on a year-to-year basis to evaluate next year's receiving yards for that corresponding WR. The data was cleaned up to only consider WRs with at least 4 years of data to evaluate.

A Sequential Feature Selector was used to determine the 10 best parameters that strongly correlate to **Next Year's Receiving Yds** and was applied to the ridge regression model. By iterating through each year's data and training the model, the test data results produced Root-Mean-Squared-Error of around 300 yds. In comparison, the standard deviation was around 400 yards, indicating that the model has some substance. 

To improve the model, additional parameters that reflect how each WR's receiving yards are trending from year to year as well as how the WR performs in comparison to their peers. After incorporating these parameters into the model, the predicted test data results' Root-Mean-Squared-Error improved to 290 yds but should not be considered as anything substantial. 
