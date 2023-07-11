# NFL-WR-Preds
## Using Machine Learning to predict the NFL WRs receiving yards

Using sci-kit learn machine learning library, a linear ridge regression model was implemented to predict each NFL WR's receiving yards in their successive season. Past 10 years of [NFL WR statistics](https://www.pro-football-reference.com/) were gathered as well as statistics reflecting each team's overall passing offense for those respective years. From the compiled data, there were more than 15 possible parameters on a year-to-year basis to evaluate next year's receiving yards for that corresponding WR. The data was cleaned up to only consider WRs with at least 4 years of data to evaluate.

A Sequential Feature Selector was used to determine the 10 best parameters that strongly correlate to **Next Year's Receiving Yds** and was applied to the ridge regression model. By iterating through each year's data and training the model, the test data results produced Root-Mean-Squared-Error of around 300 yds. In comparison, the standard deviation was around 400 yards, indicating that the model has some substance. 

To improve the model, additional parameters that reflect how each WR's receiving yards are trending from year to year as well as how the WR performs in comparison to their peers. After incorporating these parameters into the model, the predicted test data results' Root-Mean-Squared-Error improved to 290 yds but should not be considered as anything substantial. 

Further improvements of the model are dependent on the gathering of more data, particularly a quantitative representation of injury history and whether a player is playing through a certain injury that may have limited his production. A larger dataset beyond going beyond 2018 containing advanced metrics such as ADOT may help in identifying better parameters that more strongly correlate to next year's receiving yards

ReceivingData folder  - contains the yearly wide receiver statistics as well as the passing offense statistics (cleaned)

DataCleaner.ipynb - a script to remove any unwanted columns within the data files 

Stats.csv - contains a cleaned-up and concatenated version of all the data files. 

MLPredictor.ipynb - contains the model and its predictive results. 
