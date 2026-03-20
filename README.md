# ts-analysis-with-prophet
This project explores the El Niño–Southern Oscillation (ENSO) time series over decades of data and uses forecasting framework provided by Meta's Prophet. The entire thing is coded in R.

Firstly, we use R's simple plot() function to get a general idea of ENSO and then we can use R's linear regression function to get a general idea of the trend. We can see that the mean is incredibly stable with negligible increase.

Secondly, R's decompose() function is excellent for helping us understand the time series in six different ways!

Finally, we infer from these plots that the majority, if not all, of the variation can be explained by the high seasonality of the data. However, we are not statisticians, and we most certainly are not mathematicians in this project. We are simply answering the question of, "Here's what has happened before. What is happening now and what can we expect for the years to come?" So we must adapt our thinking to that of a time series analyst.

How do we do that though? Luckily, we can run the Prophet library which provides exceptionally easy-to-use and powerful forecasting methods. The issue (which can be inferred after running '?prophet') is that Prophet requires that we have a data frame (not a time series) with columns ds and y. I had to convert the time series into a data frame, then use Prophet to extend it by an amount of my choosing and plot the results. Prophet proved to be effective, showing it understood all of the components of a time series - the trend, the seasonality, the irregular noise - and coalesced these notions to give a very realistic forecast.
