# Homework 1

## Answer Sketch

- The answer sketch is posted as a [Github Markdown file containing code and results](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/sketch_hw1.md). 
- I have also provided the [R Markdown file I used to do the work](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/sketch_hw1.Rmd).

## Submission Details

Submit your work via [Canvas](https://canvas.case.edu/) by the deadline specified in the [Course Calendar](https://github.com/THOMASELOVE/2020-500/blob/master/calendar.md).

## 1. Get access to the DIG training data

Visit https://biolincc.nhlbi.nih.gov/teaching/ and request copies of the DIG "teaching" data set.

## 2. Build a mock proposal for a DIG observational study

Review the documentation available to you on the BIOLINCC page, and complete a **mock proposal** not to exceed 300 words for an observational study based on the available data from the DIG randomized trial. A list of questions you should address follows below. 

To help you build a response, you will find the following items ([above](https://github.com/THOMASELOVE/2020-500/tree/master/homework/hw1))

- a [PDF of the DIG data description](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/dig_documentation_with_supplement.pdf) now refreshed so it should work properly with Github.
- the [original 1997 publication](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/dig_NEJM_1997.pdf) in the *New England Journal of Medicine*  by the Digitalis Investigation Group, now refreshed so it should work properly with Github.
- a .csv file (`dig1.csv`) of [the DIG data set](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/dig1.csv) you will obtain from NIH/BIOLINCC
    - To download the .csv file, click on it, then click on Raw, and then download the result. Or just download the data from our [Data page](https://github.com/THOMASELOVE/500-data).

### Questions to be addressed in the Mock Proposals

1. What comparison do you want to make? (Select a comparison different than the one made in the original DIG paper)
    + Did patients receiving "EXPOSURE A" have lower rates of "BAD OUTCOME" than those who received "EXPOSURE B"?
2. Why is this of interest?
    + "OUTCOME" is important because ...
    + "EXPOSURE" (A or B) is important because ...
    + (*Be sure to clearly indicate what you hypothesize the effect of EXPOSURE on OUTCOME to be.*)
3. What are the key measures - specifically, the exposure/treatment, the primary outcome, and important covariates that are available in the data to help address your question of interest?
    + Exposure/Treatment = A or B, and be sure to specify the way in which you will know which exposure someone receives, and whether the exposure / treatment is applied using a randomized approach, or not.
    + Outcome = ..., and be sure to specify the variables you will use to determine the outcome, as well as the *type* of outcome, be it continuous, categorical (and if categorical, binary or multi-categorical) or survival (and if survival, is censoring involved?) 
    + Covariates of interest: We'd be interested in anything related to treatment choice or to outcome. You should provide a list of such variables of interest. Remember to include **ONLY** things which are measured prior to the exposure/treatment of interest, or which are not possibly changed by it.

Note that I'm **NOT** asking you to do any analyses in Question 2. Please be ready to share your answer to Question 2 at Class 2, even though the assignment isn't due until later that day.

## 3. Build and evaluate a logistic regression model using DIG data

Use R, R Studio and R Markdown to execute a logistic regression model on the `dig1.csv` data. 

Your model should be fitted to a random training sample of 5,000 subjects (be sure to specify the seed you used to select that sample) and then tested on the remaining 1,800 subjects, but you'll probably want to check for and deal with missingness in the entire sample before splitting into training and test groups. *In this case, "dealing with missingness" could be via imputation, as I'd like you to do in the rest of this semester's assignments, or by more simply developing a complete-case analysis.* Your model will predict the probability that a subject in the study will die (all causes), based on:

- the subject's assigned treatment (digoxin or placebo),
- the subject's age at randomization, 
- race, 
- sex, 
- ejection fraction (percent), 
- calculated body mass index, 
- NYHA functional class, and
- whether or not the subject currently has angina.

The relevant variables in the `dig1.csv` data set are therefore: `subjectid`, `DEATH`, `TRTMT`, `AGE`, `RACE`, `SEX`, `EJF_PER`, `BMI`, `FUNCTCLS`, and `ANGINA`.
