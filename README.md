# Seoul-Bike-Sharing-DATA-SCIENCE-2022-

The study hereby presented concerns the topic of demand forecasting, and the case study at hand entails the industry of bike sharing for the city during a time span of one year (between 2017 and 2018) in Seoul (South Korea).
Data is available [here](https://archive.ics.uci.edu/ml/index.php)

This project aims at assessing to which extent it is possible to predict the demand for bikes given the data at hand in order, ultimately, to provide some additional insights on the public sharing industry.
For the sake of clearness, the target variable will be called "Rented.Bike.Count", and it is inherently a non-negative continuous variable.


### FINDINGS

The analysis started from the problem of estimating the number of rented bikes for the city of Seoul given data on atmospheric conditions for a time interval of 12 months that goes from the end of 2017 to the end of 2018.

The starting set of variable has required some feature engineering to improve the quality of the estimate and to keep the compliance with the assumptions of the linear regression high. In particular, it has been demonstrated how the consideration of the logarithm of the target variable, the conversion of some variables into binary factors and the removal of a small share of outliers increased the explained variance of the model.

Next, through different techniques it has been shown how the exclusion of some of the variables that were initially available was not detrimental in terms of explained variance.
The impact of of this finding is mainly related to the potential saved costs that a public administration (or, more broadly, entity) may benefit from, as the cost of acquisition and maintenance of sensors to acquire data of those variables might be eliminated.
For instance, this may be not be true for the Dew Point Temperature, since this quantity is a calculated quantity (as a function of Temperature and Humidity). But, if some equipment was thought to be bought on purpose for the measurement of the Visibility, this may not be required due to the findings of this study.

Third, another aspect to take into account is the effect of the shrinkage experienced for the data at hand. Throughout the study, it has been shown how regularization (LASSO and Ridge) provide no beneficial effects in terms of explained variance. This may be due to the fact that all the models suffer from underfitting, which is mainly related to the sample size or the lack of enough independent variables to estimate the target.
Regularization entails any strategy meant to reduce the generalization error (sometimes at the expense of the training error) - in other words, regularization adds additional bias to a model. When this is applied to an underfitting model (i.e. a model whose bias is high) the predictive power is inevitably decreased.

This consideration, however leads to another aspect, that entails the further development of the work. As a matter of facts, the variables at hand pertain for the vast majority to the atmospheric domain, and a small space is reserved to the actual life of the city: the presence of events (e.g. festivals, parades, etc.), proxy variables for the traffic in the area considered, number of active means of public transportation, and so on.

These aspects may not be neglected as, bike sharing is the most sustainable means of transportation for the big public and it perfectly serves the purpose of covering the famous "last mile" of a journey, that is the last part of the travel that ends to a destination that is not covered by public transportation but it is not far from its coverage.
However, the impact of a good prediction of the amount of bikes rented may lead to a decrease, even if slight, of the overall CO2 emissions for which public entities account for, since a public administration may realize not only how many bikes to keep available, but how to better cover areas of the city that may show the willingness to open up to this means of transportation.
