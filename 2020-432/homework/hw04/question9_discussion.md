# Homework 4 Question 9 discussion

A student asked:

> I got a rather unexpected result for question nine, where the model that did best according to the training set parameters (ANOVA, AIC, BIC, adjusted r=square) performed noticably worse in two parameters with the testing set (MAE and R-square). Is this abnormal for a switch like this to happen? I just feel a little weird about the flip because the ANOVA was significant for the Augmented model being better but the predictions clearly point to the Main Effects.

**Dr. Love's response**

Please don't assume that the validation sample would always confirm what the model development sample suggests. We know that the model development sample-based summaries and testing are biased and over-optimistic. One key point of doing a validation is to be less misled by that bias. If the validation sample always confirmed the model development sample results, there wouldn't be any reason to do model validation.

Statistical significance tests are very much overstating the case with their p values in any development sample, plus in this situation we also have to remember that the sample size is large enough that even a very tiny difference in model quality will produce a p value that is very small.

- In Question 8, I, too, found that the augmented model produced statistically detectable predictive value over and above the main effects model.
- In Question 9, I found that the main effects model had better summary results in terms of two of the three measures we look at, and worse results on the third. 

That's not unusual at all.

I encourage you to listen to the Question 9 results, and to the general principle from Spiegelhalter that when you have "conflicting" results, whenever you can, use the smaller model.

Main effects all the way, is my conclusion.

TEL
