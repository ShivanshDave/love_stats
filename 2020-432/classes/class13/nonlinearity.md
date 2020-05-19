# Some Thoughts on Non-Linearity

## A few comments on the Spearman rho-squared plot

The main reason we use a Spearman rho-squared plot is as follows:

1. We know what variables we want to include in our model, but don't have a clear sense in advance of how we want to incorporate non-linear predictor terms (for instance, we don't have a prior clear understanding of which variables should interact with each other, or which variables will have a non-linear relationship with our outcome, after adjusting for all other variables.)
2. We want to avoid the possibility of using the data in such a way as to bias our eventual prediction model towards over-optimism about the significance of our coefficients, which essentially means that we cannot look directly at the X-Y relationship to see if it appears non-linear, because if we do this, we will include things we probably shouldn't, overstate the significance of the coefficients that wind up in the model, understate the standard errors, and overstate the summary statistics (R-square, C statistic, etc.) associated with the final fitted model, although we can mitigate this risk (a little bit) by splitting the data into training and test samples and performing cross-validation.  

What we're trying very hard to avoid is fitting many, many models to the data, identifying which one fits best in the data, and then believing that the summary statistics and statistical tests developed using that same data are correct, because they won't be. Every time we fit a model we spend some of the information (as measured by degrees of freedom) that we have available in the data set. Even if we have enormous data sets, we try hard not to overstate the quality of fit of a model built not for scientific reasons but instead because of p values or AIC statistics, or whatever summary you choose.

So the idea is that looking at the Spearman correlation - the rank correlation - of X with Y is somewhat safe in that it provides some evidence that helps us think about non-linearity, but it doesn't bias us so badly. We build a plot that shows for each variable X, essentially, the adjusted R-squared computed on the ranks of X and Y (and actually also on the rank of X-squared.) This absolutely does not identify which variables will most benefit from non-linear terms. Instead, it identifies (to some extent) which variables have higher and lower levels of potential predictive power for our outcome, in general. Variables with higher "potential predictive punch"  are better candidates for interactions or non-linear terms because if there is real and important non-linearity, it is more likely that it will be found by looking at those variables than at variables with lower "potential predictive punch."

We use the plot to help decide where to spend the degrees of freedom of non-linearity that we are willing to spend, but (a) if we have scientific reasons to fit non-linear terms, like splines or interactions, then those scientific reasons should be used instead of the plot and (b) the plot is by no means a guarantee that the non-linear terms we identify will wind up adding significant or substantial predictive value to the model.

## On "spending" degrees of freedom

First, I will note that for some of you, in Project 1, maintaining these standards will not be possible. I know this. 

The number of degrees of freedom that you are "spending" to fit any particular model is related to the sample size of your data, and the number of coefficients you are fitting in that model. Paying attention to how you are "spending" degrees of freedom is an important part of fitting any prediction model. If you include more regression coefficients in a model than you can reasonably support with the sample size you have, then you will run into all sorts of problems. In addition, if you fit a whole bunch of models, and compare each in terms of how well it fits to the outcome, then you will definitely run into meaningful problems in terms of the model not performing as well in new data as it appears to perform in your current data.

If you have a model that currently uses 8 degrees of freedom, that means you've spent 8 df to fit it, not that you have exactly 8 df left to spend, or anything like that. So what is the \# of degrees of freedom that we can plausibly spend?

-   In a linear model, it is, essentially, your sample size divided by 20 (some would argue 15, some 50) but see the details below on what counts as spending degrees of freedom.
-   In a logistic model, if your sample size is n, then the number of degrees of freedom you have to spend is, somewhere between n/50 and n/100, and again, see below for details.

Start by verifying that your modeling process has not spent more degrees of freedom than you can afford to spend. That means that you should:

1.  count up the number of degrees of freedom that will be used in each model that you fit to your outcome (so if you plan to use best subsets to produce eight different models, then you used all of the degrees of freedom used by each of those eight models or if you fit four different candidate models, each with 4 degrees of freedom used, that's 16.) Call that total number of degrees of freedom P.
2.  Then take your sample size (the number of complete, non-imputed values in your data set used to fit the models) and call that N.
3.  In a linear regression, N/P should be at least 20.
    -   If it's not, you need to rethink your modeling plan until it is.
    -   You don't need to count using the Spearman plot as using up degrees of freedom.
    -   If you're cross-validating, maybe you can get away with N/P being as small as 15.
4. In a logistic regression, N/P should probably be at least 50, although there's a good argument that it should be 100 or more.

