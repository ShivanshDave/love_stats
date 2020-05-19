# Project Presentations: Comments from Dr. Love after Day 1 (2019-12-09)

Hi - 

I heard 16 presentations today, all of which were at least OK, and some of which were very good or even excellent. I have a few comments to help those folks do a better job on their portfolios (due Wednesday) and to help other folks do a better job on their presentations on Tuesday and Thursday.

## On Study B

1. The number one problem presenters had today in Study 2 was interpreting the meaning of their linear regression coefficients, particularly for a categorical variable. You need to nail this down, so that you can do it in your presentation, and address it in writing in the portfolio. Identify a variable of interest in your final model, and make sure you know what the coefficient estimate means, and can explain it to my satisfaction. Some of this problem is undoubtedly because there is a lot of misinformation on this topic on the web.
    - If X is a quantitative predictor, and you have a slope estimate for predictor X of 2, then this means that the change in your outcome Y (which is measured here in points) associated with a 1 unit increase in X, while holding all of the other predictors constant, will be an estimated 2 point increase in Y. Put another way, if you have two subjects, one with X = 5 and one with X = 6 but having the same values for all other predictors in the model, the one with X = 6 is predicted to have a Y that is 2 points larger.
    - If X is a quantitative predictor, and you have a slope estimate for predictor X of -3, then this means that the change in your outcome Y associated with a 1 unit increase in X, while holding all of the other predictors constant, will be an estimated 3 point decrease. Again, if you have two subjects, one with X = 5 and one with X = 6 but having the same values for all other predictors in the model, the one with X = 6 is predicted to have a Y that is 3 points smaller.
    - If, on the other hand, X is a quantitative predictor, but C is a categorical predictor with three levels labeled Good, Fair and Poor, you might have a model like the following:  Y = 4 - 5X + 9(C = Good) - 8(C = Fair), where we define the two indicator variables "C = Good" and "C = Fair" as follows: "C = Good" = 1 if C is Good and 0 otherwise. "C = Fair" = 1 if C is Fair and 0 otherwise.
        - To think about the effect of the C predictor, we need to know the baseline case (that's the level of C that doesn't get a regression coefficient - here since we have coefficients for Good and Fair but not Poor, the baseline is Poor.) In other words, when "C = Good" and "C = Fair" are both zero, it means the subject is in the "C = Poor" category.
        - The coefficient for the predictor "C=Good" is +9. That means that if we increase "C=Good" by 1 unit while holding all of the other predictors constant, our model predicts that Y will increase by 9 points. 
        - What does it mean to increase "C = Good" by 1 unit? "C = Good" is an indicator variable (indicating whether the subject's C value is Good) that can only take on the values 0 and 1. So it means changing "C = Good" from 0 to "C = 1".
        - So we can say that the coefficient for "C = Good" = +9 means that if we move "C = Good" from 0 to 1, while not changing any of the other variables, then our model predicts that Y will increase by 9 points. But this means that we're comparing the model when "C = Good" and "C = Fair" are both 0 (which is the situation when "C = Poor") to the model with "C = Good" being 1 and "C = Fair" being 0 (which is the situation when "C = Good").
        - So what we get is that if we have two subjects with the same value of our quantitative predictor X, and one is "Good" in the C category, and the other is "Poor", then the "Good" subject is predicted by the model Y = 4 - 5X + 9(C = Good) - 8(C = Fair) to have a Y value that is 9 points higher than the "Poor" subject.
        - Similarly, if we have two subjects with the same value of our quantitative predictor X, and one is "Fair" in the C category, and the other is "Poor", then the "Fair" subject is predicted by the model Y = 4 - 5X + 9(C = Good) - 8(C = Fair) to have a Y value that is 8 points lower than the "Poor" subject.
   - Another common problem was trying to build an explanation when a transformation of Y is involved, but it's actually pretty straightforward. If your model is actually log Y = 4 - 5X + 9(C = Good) - 8(C = Fair), then this just means that the model will predict that the log of Y will go down by 8 points if we look at a "Fair" subject as compared to a "Poor" one with the same value of X. It also means that this model will predict that the log of Y will go up by 9 points if we look at a "Good" subject as compared to a "Poor" one with the same value of X.

2. The second most common problem involved back-transformation. The [Homework I answer sketch](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/I/post-deadline.md) has been helpful to some people - maybe you, too!

3. When assessing collinearity, consider VIF to be the most direct answer, perhaps supplemented by a comparison of the raw and adjusted R-square.

4. When transforming your data, if the Box-Cox suggests something but the outcome's Normality doesn't improve (much or at all), it still may be that the residual plots will improve, particularly in terms of reducing the effects of non-linearity, non-constant variance and outliers. 

5. Rather than showing the MSPE alongside the MAPE, you might want to show the square root of the MSPE, which would at least be back on the scale of the errors themselves, rather than the square of those errors. This is something I should have fixed in the code initially. Another useful statistic we'll use in 432 is to actually calculate the square of the correlation between the fitted and observed values in the test sample - a cross-validated R-square.

## On Study A

1. I spoke to a lot of people today about Analysis 2 in Study A. In doing Analysis 2 in Study A, a few thoughts:
- You are not going to have a lot of data in some (or all) of your groups. Collapse categories until you have at least 10 in each group, and you must have at least 3 groups.
- If you see signs of clear non-Normality in one or more of the samples, I would run both the ANOVA and the Kruskal-Wallis, and if the results were similar, I would go forward with the ANOVA, and run a Tukey HSD plot, in particular. 
- If you see no signs of problems with assuming Normality in each of your samples, just run the ANOVA and the Tukey HSD plot.
- If the ANOVA is not significant, the Tukey HSD won't be, either, but it's still useful to see the plot to understand the effect estimates you have for this part of the project.

2. I also spoke to a lot of folks about Analysis 5 today.
- Present your table in a sensible order, so that you may want to rearrange the factors, so that (for example) you present High Middle Low, rather than High Low Middle.
- Again, you won't have a lot of data. But you are supposed to have a minimum of 3 rows and 3 columns of data (not counting the row sums or the column sums) *and* each of the table margins (row totals and column totals) should be 10 or more. I encourage you to collapse until this is true, so long as you still have at least 3 rows and 3 columns.
- I would never run a Fisher exact test unless I had a square table, with as many rows as columns. The Fisher test isn't a meaningful improvement over a Pearson $\chi^2$ test when you have the sample sizes you folks will have.
- Make sure that you understand (and have in writing in your portfolio) a proper interpretation of your chi-square test result. What does your small *p* value (or your large *p* value) actually mean in the context of your problem?

3. The fact that I talked to a lot of people about Analyses 2 and 5 doesn't mean I won't ask you about Analyses 1, 3, 4 or 6. I was just in a 2 and 5 mood today.

