# Stock-Price-Prediction

**Problem Statement:**
The objective of this project was to develop two machine learning models by examining European call option pricing data on the S&P 500 to predict the current option value (C) and to check if Black-Scholes option pricing model prediction overestimated the option value or underestimated the option value.

**The Big Picture:**
A European call option gives the holder the right (but not the obligation) to purchase an asset at a given time for a given price. Valuing such an option is tricky because it depends on the future value of the underlying asset. The Black-Scholes option pricing formula provides an approach for valuing such options. The Black-Scholes formula states:
where,
C_pred: predicted option value
d1=log(S/K)+(r+2)tau/(tau)
d2=d1-(sÖTau)
S: Current asset value
Φ(x): represents the probability that a standard normal random variable will take on a value less than or equal to 𝑥.
K: Strike price of Option
r: Annual interest rate
tau: time to maturity (in years)
Using a dataset of 1680 options, we built statistical/ML models. For training our models, we used 70% of this data and the rest 30% was used to test out the models. We explored regression models like linear Regression and Random Forest Regressor for predicting the Value and classification models like Logistic Regression, SVM, KNN, Random Forest Classifier and Naïve Bayes Classifier for classifying if the option value has been over-estimated or under-estimated.

**Results:**
We found Random Forest Regressor to be our best model for predicting the Value. On the test data we created, we see out-of-sample R2 as 99.82%.
For classification we used a different approach which we call Majority Principle. We used all 5 classification models that we had built and predicted BS for each record. Basis the majority prediction of these 5 models we classified our final BS as either ‘Over’ or ‘Under’. The test accuracy we achieved using this approach on the test data we created is 93.04%.
