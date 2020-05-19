431 Homework I
================
Due **2019-12-02** at 5 PM. Last Edited 2019-11-20 13:08:02

# NEW! Hints!

We've added a [Hints for Homework I page](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/I/hints.md). Take a look.

# General Instructions

This homework includes **six** questions. Be sure to respond to each
question.

# Question 1 (30 points)

Tell us about the most useful thing (an insight, example or key idea)
that you learned from reading Nate Silver’s *The Signal and the Noise*.
Be sure to specify **in detail** how this insight/example/idea connects
to your own life, or work. Specify at least one quote from the book that
discuss this issue, and explain the context.

Be sure that when we finish your essay we have a clear understanding of
how reading this book has changed the way you think about the thing you
describe or things related to it.

## Specifications for the essay

In reading your essay, we will look for the following specifications to
be met:

1.  Length is between 200 and 400 words.
2.  English is correctly used throughout, and there are no
    typographical, grammatical or syntax errors.
3.  A key idea is identified and clearly stated that actually appears in
    *The Signal and the Noise*.
4.  An accurate and properly cited quote from the book is provided that
    is relevant to the identified key idea.
5.  The context for the quote within Silver’s book is described in the
    student’s essay.
6.  The essay clearly specifies how the idea in the book has changed
    their way of thinking about something which is explained in the
    essay.
7.  The essay is clearly written, in general.
8.  The essay is interesting to read.

# General Description of the Data for Questions 2-6

Low dietary intake or low plasma concentrations of retinol,
beta-carotene, or other carotenoids might be associated with increased
risk of developing certain types of cancer. However, relatively few
studies have investigated the determinants of plasma concentrations of
these micronutrients. A cross-sectional study was designed to
investigate the relationship between personal characteristics and
dietary factors, and plasma concentrations of beta-carotene. Study
subjects (*n* = 290) were patients who had an elective surgical
procedure during a three-year period to biopsy or remove a lesion of the
lung, colon, breast, skin, ovary or uterus that was found to be
non-cancerous.

|      Variable | Description                                                                |
| ------------: | -------------------------------------------------------------------------- |
|     `subj_ID` | Subject identification code (S-1001 to S-1290)                             |
|         `age` | Subject’s age (in years)                                                   |
|         `sex` | Subject’s sex (M = male, F = female)                                       |
|     `smoking` | Smoking Status (Never, Former, or Current)                                 |
|         `bmi` | Body-Mass Index ( weight in kilograms / \[height in meters\]<sup>2</sup> ) |
|     `vitamin` | Vitamin Use (1 = Often, 2 = Sometimes, 3 = Never)                          |
|    `calories` | Number of Calories consumed (per day)                                      |
|         `fat` | Number of grams of fat consumed (per day)                                  |
|       `fiber` | Number of grams of fiber consumed (per day)                                |
|     `alcohol` | Number of alcoholic drinks consumed (per week)                             |
| `cholesterol` | Number of milligrams of cholesterol consumed (per day)                     |
|  `betaplasma` | Plasma beta-carotene (in ng/ml)                                            |

The `hwI_plasma.csv` data set is available on our web site. It contains
290 observations on the 12 variables described in the table above. You
will use a particular subset of 240 of those observations (details on
how you’ll pull this random sample follow so we all pull the same one)
to fit your models, and the remaining 50 observations to validate your
model selection.

In questions 2-6, you will build and evaluate a pair of multiple
regression models for plasma beta carotene levels. To get started, I
suggest this approach to loading the data, a version of which is
**provided for you** as part of the Homework I R Markdown template.

``` r
knitr::opts_chunk$set(comment = NA)

library(here); library(janitor); library(magrittr)
library(patchwork); library(broom); library(tidyverse)

hwI_plasma <- read_csv(here("data", "hwI_plasma.csv")) %>%
    mutate_if(is.character, as.factor) %>%
    mutate(subj_ID = as.character(subj_ID))
```

Then use the following code to select a training sample from the data
set (to be used in questions 2-5) and a test sample (to be used in
question 6). Use `2019431` as your seed as we have done here - that is
what we’ll do in the Answer Sketch.

``` r
set.seed(2019431)
hwI_training <- hwI_plasma %>% sample_n(240)
hwI_test <- anti_join(hwI_plasma, hwI_training, 
                      by = "subj_ID")
```

If you want to check that you’ve done this in the way you’ll see it in
the sketch…

  - The first two rows in my `hwI_training` describe subjects S-1137 and
    S-1042.
  - The first two rows in my `hwI_test` describe subjects S-1006 and
    S-1016.

# Question 2 (15 points)

Use the `hwI_training` data frame to plot the distribution of the
outcome of interest, which is `betaplasma`, and then plot the logarithm
of `betaplasma`. Specify which of the two distributions better matches
the desirable qualities of an outcome variable in a regression model.
Whichever choice you make about the outcome – either `betaplasma` or
`log(betaplasma)` – stick with it for the rest of this homework.

# Question 3 (10 points)

Use the `hwI_training` data frame to build a model for your outcome (as
decided in Question 2) using four predictors: `age`, `sex`, `bmi`, and
`fiber`. Call that model `model_04`.

Summarize `model_04` and write a sentence or two to evaluate it. Be sure
you describe the model’s R<sup>2</sup> value. Also, be sure to interpret
the model’s residual standard error, in context.

# Question 4 (10 points)

For your `model_04`, what is the estimated effect of being female,
rather than male, on your outcome, holding everything else (age, bmi and
fiber) constant. Provide and interpret a 95% confidence interval for
that effect on your outcome.

# Question 5 (15 points)

Now use the `hwI_training` data frame to build a new model for your
outcome (as decided in Question 2) using the following 10 predictors:
`age`, `sex`, `smoking`, `bmi`, `vitamin`, `calories`, `fat`, `fiber`,
`alcohol`, and `cholesterol`. Call that model `model_10`.

Compare `model_10` to `model_04` in terms of **adjusted** R<sup>2</sup>,
and residual standard error. Which model performs better on these
summaries, in the training sample?

# Question 6 (20 points)

Use the code provided in Section 14 of the [Project Study B
Example](http://bit.ly/431-2019-studyB-example) to calculate and then
compare the prediction errors made by the two models (`model_10` and
`model_04`) you have generated. You should:

  - Calculate the prediction errors in each case, then combine the
    results from the two models, tweaking the code and descriptions
    found in Section 14 of the [Project Study B
    Example](http://bit.ly/431-2019-studyB-example).
      - **HINT**: If you chose to transform the outcome variable back in
        Question 2, then you will need to estimate the predictions here
        back on the original scale of `betaplasma`, rather than on the
        logarithmic scale. That involves making predictions on the log
        scale, and then back-transforming them with the `exp` function
        before calculating the residuals and eventually the summary
        statistics.
  - Visualize the prediction errors in each model, using the code in
    Section 14.2 of the Project Study B Example.
  - Form the table comparing the model predictions, using the code in
    Section 14.3 of the Project Study B Example. Compare the models in
    terms of MAPE, MSPE and maximum prediction error.

Based on your results, what conclusions do you draw about which model
(`model_10` or `model_04`) is preferable? Is this the same conclusion
you drew in Question 5?

