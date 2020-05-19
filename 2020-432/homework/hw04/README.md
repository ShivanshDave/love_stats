432 Homework 4
================

# Post-Deadline Materials

1. A ([PDF](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/sketch_hw4.pdf) and [R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/sketch_hw4.Rmd) of the answer sketch and rubric is available now. 
2. Grades are now posted to http://bit.ly/432-2020-grades. Check your email for your HW-Code.

## [Hints for Homework 4 (very important) were revised 2020-03-21](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/homework4_hints_2020-03-21.pdf).

This version of Homework 4 was built 2020-02-28 16:09:14

### Setup and Package Loading

``` r
library(here); library(janitor)
library(magrittr); library(knitr)

library(tidyverse)

opts_chunk$set(comment = NA)
```

# General Instructions

Submit your work via [Canvas](https://canvas.case.edu/). The deadline is
specified on [the Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md).

  - Your response should include an R Markdown file and an HTML document
    that is the result of applying your R Markdown file to the
    `hbp432.csv` data, available in the data subfolder for this
    homework, as well as on our Data and Code page.
  - Start a separate R Project for Homework 4, as your first step, and
    place the data in that project’s directory or (perhaps better) in a
    data sub-directory.
  - In all of our homeworks, do not include R output without complete
    sentences describing what you are doing in each step, and what you
    conclude from that work.
  - This homework assignment will be graded as if it were out of 100
    points in compiling your overall homework grade, but there is an
    opportunity for you to earn up to 115 points on it. If you score
    over 100, that’s a bonus\!

## Packages We Think You’ll Use in Building Your Answer

In addition to those listed above, we used the following packages in
building the answer sketch.

    broom
    car
    caret
    knitr
    mice
    naniar
    rms
    simputation

## Getting the `phr` data

Please visit <https://www.lerner.ccf.org/qhs/datasets/> and click on the
link marked **Register here to download datasets**. Once you have access
(it shouldn’t take more than a couple of minutes) you will be obtaining
the Personal Health Records data set.

  - The data come from a paper by Tenforde et al. in *J Gen Inten Med*
    from 2012. You’ll find a [description of the study
    here](https://www.lerner.ccf.org/qhs/datasets/PHR.docx) and a
    [description of the data set
    here](https://www.lerner.ccf.org/qhs/datasets/PHRDataDictionary.docx) and you’ll
    be able to download the `phr.csv` data set once you’ve successfully
    registered.

Read the `phr.csv` data into R, and clean the names.

``` r
phr <- read_csv(here("data", "phr.csv")) %>%
    clean_names()

phr
```

    # A tibble: 10,746 x 20
          id   age female caucasian insurance income engagement  user logins
       <dbl> <dbl>  <dbl>     <dbl>     <dbl>  <dbl>      <dbl> <dbl>  <dbl>
     1     1  69.9      0         1         0  38518      0.322     0      0
     2     2  36.8      0         0         1  66989      0.667     1     16
     3     3  39        1         1         1  52954      0.306     1     28
     4     4  60.3      0         1         1  47258      0.382     0      0
     5     5  73.3      1         1         0  46955      0.37      1      1
     6     6  52        1         1         1  97002      0.521     1     11
     7     7  65.4      1         1         0  44096      0.516     0      0
     8     8  66.6      0         1         0  55781      0.382     1     10
     9     9  52.2      1         1         0  47258      0.515     1      2
    10    10  70.1      1         1         0  69401      0.25      0      0
    # ... with 10,736 more rows, and 11 more variables: eye_exam <dbl>,
    #   pneumo_vaccine <dbl>, ace_arb_alb <dbl>, foot_exam <dbl>, nonsmoker <dbl>,
    #   hba1c_test <dbl>, hba1c <dbl>, sbp <dbl>, dbp <dbl>, ldl <dbl>, bmi <dbl>

# Don't do this homework without reviewing the [Hints for Homework 4](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/homework4_hints_2020-03-16.pdf).

# Question 1 (5 points)

Create a `phr1` tibble which includes

  - only those patients who have data on systolic blood pressure, and
  - only the following 9 variables: `id`, `sbp`, `age`, `female`,
    `caucasian`, `insurance`, `hba1c`, `ldl`, and `bmi`.

In addition to annotating your R code, specify (in a sentence) how the
size of your tibble changes from the original `phr` to this new `phr1`.

# Question 2 (5 points)

Use the `caret` package to help you accomplish a validation split, to
help you build up a model for `sbp` in the `phr1` data. Specifically,
split the `phr1` tibble into a training sample containing 75% of the
data, and a test sample containing the remaining 25%. Use the number
`2020` as your seed for random number generation.

# Question 3 (5 points)

Next, you will build a regression model to predict a patient’s systolic
blood pressure on the basis of seven predictors, specifically the
patient’s hemoglobin A1c, LDL cholesterol, body-mass index, age, sex,
race and insurance status. How many observations are missing for each of
the predictors in your training sample?

# Question 4 (10 points)

We’d like to use a Box-Cox procedure to evaluate whether a
transformation of the outcome is necessary, within your training sample,
but to accomplish this, you’ll need to do something about those missing
values.

So use simple imputation with a robust linear model including the other
6 predictors and the systolic blood pressure to predict any missing
values you identified in Question 3. Verify that there is no missing
data remaining after you do this imputation.

# Question 5 (10 points)

Generate appropriate Box-Cox procedure results for assessing potential
transformations of the outcome using the model described in Question 3,
and describe your conclusions. Please restrict yourself to consideration
of only five possible transformations: (a) squaring the outcome, (b) the
untransformed outcome, (c) the square root of the outcome, (d) the
natural logarithm of the outcome, or (e) the inverse of the outcome.

# Question 6 (10 points)

The planned model for the outcome you decided on in Question 5 includes
seven predictors, all of which will be included in your model as main
effects. Run this “main effects” model in your training sample using the
`lm` function, and obtain the nominal R-squared, adjusted R-squared, AIC
and BIC results.

# Question 7 (10 points)

Use an appropriate strategy to determine how best to spend exactly 5
additional degrees of freedom (beyond the main effects model) on exactly
two terms involving restricted cubic splines. Describe your conclusions
and reasoning carefully.

# Question 8 (10 points)

Fit the “augmented” model you selected in Question 7 again using the
`lm` function, and compare the training sample’s R-squared, adjusted
R-squared, AIC and BIC results to what you saw in Question 6. Then run
an ANOVA to compare the two models. What conclusions do you draw about
which model to prefer, based on the training sample?

# Question 9 (15 points)

Now use each model (the one from Question 6 and the one from Question 8)
to make predictions in the test sample you developed way back in
Question 2 and make a decision on the basis of the usual summary
statistics (specifically the validation R-square, root mean squared
prediction error and mean absolute prediction error) as to which model
produces better predictions for systolic blood pressure.

## Three Hints for Question 9

  - Remember to back-transform your way out of any transformation you
    selected in Question 5.
  - You’ll need to deal with missingness in the test sample in order to
    get predictions. For purposes of this homework assignment, do that
    by dropping from the test sample all observations with missing data
    on the predictors included in your model.
  - Note that one of two things will happen here:
      - either one of the two models will “win” the comparison of all
        three statistics (R-square, RMSE and MAE) in which case that is
        the model to choose,
      - or the model you should choose will “win” two out of the three
        comparisons.

# Question 10 (10 points)

Return to the `phr1` tibble you created back in Question 1 and fit the
regression model you preferred in Question 9 to predict your
(potentially transformed) `sbp` using all of the **complete cases** in
that tibble.

  - Provide an attractive table containing the coefficients, standard
    errors, and lower and upper bounds for a 95% confidence interval for
    each coefficient.

# Question 11 (15 points)

Return to the `phr1` tibble you created back in Question 1 and fit the
regression model you preferred in Question 9, to predict your
(potentially transformed) `sbp` but this time, use **multiple
imputation**.

  - Include all 6 other predictors and the outcome in the imputation
    model for each predictor, and set the random seed to `2020432` and
    run 10 imputations.
  - As in Question 10, provide an attractive table containing the
    coefficients, standard errors, and lower and upper bounds for a 95%
    confidence interval for each coefficient after this model has been
    fit.

# Question 12 (10 points)

Specify the `insurance` effect size in the models you obtained in
Questions 10 and 11. Provide a confidence interval and point estimate,
and describe what the point estimate means in this context. Does the use
of multiple imputation as opposed to a complete case analysis appear
have a large impact on this estimate?

### Please add the session information.

Finally, at the end of this homework and all subsequent assignments
(including the projects), please add the session information. My
preferred way for you to do this is:

``` r
sessioninfo::session_info()
```

# Again, please review the [revised Hints for Homework 4](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/homework4_hints_2020-03-21.pdf) before submitting your work.

### This is the end of Homework 4.
