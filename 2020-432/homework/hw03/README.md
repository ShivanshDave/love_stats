432 Homework 3
================

# All post-deadline Homework 3 stuff is now available.

- [PDF](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw03/sketch/sketch_hw3.pdf) including both the sketch and rubric, adjusted to fix the error we had in the original version on Question 3.
- [R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw03/sketch/sketch_hw3.Rmd) used to build the updated PDF.
- Grades are now posted to http://bit.ly/432-2020-grades. Check your email for your HW-Code.
- We built a [Google Doc containing several of the essays we really enjoyed in response to Question 6](https://docs.google.com/document/d/1krZRnMTniOKfU0EqlE-dnJjqP4n7hBgFB7JSPN-x8mQ/edit?usp=sharing). Thanks!

This assignment was revised 2020-02-18 at 9:30 AM to reflect a
shortening of the request in Question 5.

# General Instructions

Submit your work via [Canvas](https://canvas.case.edu/). The deadline is
specified on [the Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md).

  - Your response should include an R Markdown file and an HTML document
    that is the result of applying your R Markdown file to the
    `hbp432.csv` data, available in the data subfolder for this
    homework, as well as on our Data and Code page. - Start a separate R
    Project for Homework 3, as your first step, and place the data in
    that project’s directory or (perhaps better) in a data
    sub-directory.
  - In all of our homeworks, do not include R output without complete
    sentences describing what you are doing in each step, and what you
    conclude from that work.

# Question 1 (30 points)

Again, consider the `hbp432` data used in Homework 1. Build your best
model for the prediction of body-mass index, considering the following
14 predictors: `practice`, `age`, `race`, `eth_hisp`, `sex`,
`insurance`, `income`, `hsgrad`, `tobacco`, `depdiag`, `sbp`, `dbp`,
`statin` and `bpmed`. Use an appropriate best subsets procedure to aid
in your search, and use a cross-validation strategy to assess and
compare potential models.

  - Feel free to omit the cases with missing values in the variables you
    are considering (these 14 predictors, plus the `bmi` outcome) before
    proceeding. This should not materially affect your sample size very
    much. In the answer sketch, we will use a complete cases analysis.
  - Use the `nvmax = 7` command within your call to `regsubsets` to
    limit your investigation to models containing no more than seven of
    these candidate predictors.
  - Do not transform any variables, and consider models with main
    effects only so that no product terms are used.
  - A 5-fold cross-validation strategy would be very appropriate.
    Another reasonable choice would involve partitioning the data once
    (prior to fitting any models) into training and test samples, as we
    did in 431.

Be sure to provide a written explanation of your conclusions and specify
the variables in your final model, in complete sentences.

# Question 2-5 (40 points, total)

Using the `hbp432` data, you will build models to predict whether or not
the subject has a statin prescription based on the subject’s current LDL
cholesterol and which of the four practices they receive care from. Fit
logistic regression models both with and without an interaction term
between the practice and the LDL level.

## Question 2 (10 points)

Use a likelihood ratio test to compare the models, and describe its
conclusions.

## Question 3 (10 points)

Compare the confusion matrix produced by the two models (using a 0.5 cut
point). Produce an attractively formatted table comparing the models in
terms of prediction accuracy, sensitivity, specificity, as well as PPV
and NPV.

## Question 4 (10 points)

Based on your general assessment of each model’s quality of fit, select
the model (interaction or no interaction) that seems more appropriate,
and justify that selection.

## Question 5 (10 points)

For the model you selected in Question 4, interpret the odds ratio
associated with the `ldl` main effect carefully, specifying a 90%
uncertainty interval and what we can conclude from the results.

# Question 6 (30 points)

  - First, in 2-4 complete English sentences, please specify, using your
    own words and complete English sentences, the most useful and
    relevant piece of advice you took away from reading the chapters in
    David Spiegelhalter’s **The Art of Statistics** that you have read
    so far.
      - Please provide a reference to the section of the book that
        provides this good advice.
  - Then, in an essay of 4-8 additional sentences, describe why this
    particular piece of advice was meaningful or useful for you,
    personally, and how it will affect the way you move forward.
      - You are strongly encouraged to provide a specific example of a
        past or current scientific experience of yours that would have
        been (or is being) helped by this new approach or idea.
      - After reading your work, we want to be able to easily specify
        what this idea is, and why it is important and worth sharing.

### Please add the session information.

Finally, at the end of this homework and all subsequent assignments
(including the projects), please add the session information. My
preferred way for you to do this is:

``` r
sessioninfo::session_info()
```

### This is the end of Homework 3.
