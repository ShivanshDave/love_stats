## Some Project 1 Tips

1. **Representing Fractions** If you have a quantitative predictor or outcome in your project 1 data that could be represented by either a proportion (number between 0 and 1) or a percentage (number between 0 and 100), I suggest you use a percentage, multiplying the proportion by 100 if necessary.

2. **Scaling Your Predictors** If your predictors are on wildly different scales, for instance, most of your predictors are between 0 and 100 or are categorical, but one of your predictors (say, `cost`) is on a much wider scale (say from 1,000 to 10,000,000) then I strongly suggest either representing the costs with a base-10 logarithm or dividing by, say, 1000 to represent the costs in thousands of dollars. This will reduce the chances of you having a very very small or very very large coefficient that you need to explain. 

3. **Imputation** For Project 1, I suggest that using simple imputation or complete cases is fine. We'd like to see multiple imputation in Project 2, but it's not something Dr. Love will be looking for in Project 1, *except* that it's an excellent thing to mention in the Discussion session as a likely next step for the work.

4. **Box-Cox and Transformations of Your Linear Regression Outcome**.

The Box-Cox procedure is **not** going to provide useful information on transformation of a quantitative outcome if your outcome is:

- not all positive, (although it's always possible to add a number to every observation to get them all to be strictly positive) *or*
- actually discrete with limited potential values *or*
- subject to a ceiling and/or a floor effect *or*
- not particularly skewed at all, but instead either heavy-tailed or light-tailed, 

since the limited set of transformations available really don't deal with any of those issues.

Other things that can cause trouble include:

- if you have one or more predictors that essentially define the outcome value (for instance, everyone who smokes has a higher outcome value, or close to that, than everyone who doesn't smoke)
- if you have two or more predictors that are highly collinear with one another (you can use `car::vif` to check this for a model you're fitting with `lm` or `glm`, and `rms::vif` to check collinearity for a model fit with `ols` or `lrm`.)

In any case, if you run the Box-Cox procedure and it doesn't give you a sensible transformation (meaning that it gives you a value wll outside the range of -1 to +2), then I vehemently encourage you to use your common sense and understanding of what might be helpful to select a **sensible transformation** instead of whatever Box-Cox recommends. A sensible transformation is one of the following five:

- inverse, logarithm (either natural or base-10 has the same effect,) square root, raw data (untransformed), or square

I cannot anticipate a good reason for you to use any transformation other than those five for your outcome in your linear regression for Project 1. So **don't**. 

5. **Exploding Coefficients or Failure to Fit a Logistic Model**. Some of you may have a logistic regression model that won't run, or that produces explosive results, with extremely large or small coefficients or standard errors. 

- If that's the case, check to see that your binary outcome occurs at least a few times (and doesn't occur at least a few times) at every level of each of your categorical predictors. 
- If, for example, you have a factor with levels A, B, C and D, and your outcome is always 1 (and never 0) for subjects in level D, you have a problem. 
- The simplest solution in that case would be to recast the logistic regression model as a model for the sample including only subjects from levels A, B and C.

6. **Confusion Matrix and ROC curve**. In fitting a confusion matrix, there's no need to force a standard of 0.5 for the cutoff you use. Selecting a different standard will change both the sensitivity and specificity, and often, the results will be a bit stronger at a value further away from 0.5, especially if your outcome occurs at a rate that's not close to 50% in your data. It’s up to you to decide what the probability cutoff should be to classify an individual as "predicted positive." The most important thing to think about is the relative costs of misclassification. Often we are willing to increase the costs of misclassification in one direction to reduce the costs of misclassification in the other direction.

- The ROC curve (if you plot it) helps to indicate how changing the cutoff for the decision rule affects the sensitivity-specificity relationship. Specifically, the ROC curve does this by plotting sensitivity, the probability of predicting a real positive will be a positive, against 1-specificity, the probability of predicting a real negative will be a positive, for various decision rules.
- In fact, the ROC curve plots out the sensitivity and specificity for every possible decision rule cutoff between 0 and 1 for a model.
- The further the curve is from the diagonal line, the better the model is at discriminating between positives and negatives in general.
- The Youden index is one statistic that can be used to identify the decision rule (between 0 and 1) for the fitted values that provides the optimal cutpoint (under specific circumstances.)
- If you're essentially agnostic about the two types of misclassification, a common approach is to find the cutpoint that maximizes the sum of the sensitivity and the specificity. [The `cutpointR` package](https://cran.r-project.org/web/packages/cutpointr/vignettes/cutpointr.html) can be helpful in doing this.

**In short**, it's not important to me that you optimize this choice in Project 1. Feel free to use a different standard for your decision rule than 0.5 for any reason you like. You might, for instance, try a few options (I would stick to a decision rule where the fitted is either 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8 or 0.9) and select the one with the highest combined sensitivity + specificity. Just make sure to make it clear that is what you are doing. 

7. **Picking between Model A or B via Validation** If you are comparing models A and B in Project 1 and they are very comparable in terms of validation statistics (perhaps the R-squares are within 1-2 percentage points of each other, and the RMSE and MAE disagree) then if both models' residual plots look OK, I would probably pick the main effects model, personally. (If model A's residuals look fine, but model B's don't, then you'd clearly choose model A.) You can choose whatever model you feel is more justified by your analyses.

- The same advice goes for the comparison of Models Y and Z in the logistic regression work, except that there I wouldn't be looking at residuals, but mostly at the C statistic.

A good strategy if you're unsure is probably this:

- In a linear model, compare the validated R-squares. If they differ by 0.02 or less, it's not critical that you pick one over the other, so you might as well follow the advice from Spiegelhalter and go with the smaller (i.e. main effects) model.
- In a logistic model, compare the validated C statistics. If they differ by 0.02 or less, it's not critical that you pick one over the other, so you might as well follow the advice from Spiegelhalter and go with the smaller (i.e. main effects) model.

8. My note on **back-transformation in nomograms** for linear and logistic regression is available [in R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/class14_nomogram_note.Rmd) or [as a PDF](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/class14_nomogram_note.pdf). The only other thing you should be back-transforming is your prediction in a linear model with a transformed outcome.

9. One clear tip for the poster is that if you chose model B instead of model A in your linear model, model B is the only model we should see any evidence of in the poster.

10. When you draw an ROC curve, make sure that the result matches what you get from an lrm fit of the model. If not, it may be that your outcome is misspecified, or misinterpreted by the code. It is very important that you identify the C statistic correctly. If your plot doesn't match the correct C statistic, do not include it. Not having an ROC plot might cost you 1 point out of 100 for the project, at most. Having a mismatch between plot and C statistic obtained through `lrm` would be much more costly.

11. The key thing to explain any interaction is to remember to use the words "It Depends" - if the AxB product term is important in predicting Y, then the effect of A on Y depends on the status of B. Similarly, the effect of B on Y depends on the status of A.

12. If your nomogram is too small in the portfolio try using `fig.height` in the code chunk name to make it larger.

13. When you build your poster, use the Rds file (that you create at the end of your portfolio) to import the data through `readRDS()`. That way, you don't have to worry about matching your data management decisions from the portfolio. 

14. While it is possible to save pictures you build in the portfolio to files and then post those images into the poster, please do not do that.

