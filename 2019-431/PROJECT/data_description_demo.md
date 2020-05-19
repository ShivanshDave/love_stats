# On Data Descriptions for Revisions of Study B Task 2

The revisions are due 2019-10-16 at 5 PM for everyone whose proposal is not yet approved. Submit your revision by uploading a new version of your original submission to Canvas, in the same place you did this initially. Canvas has reopened for submissions on this now.

More people had trouble with the data description than with the proposal summary, although most still need to work a bit on the summary, too. I thought it might be helpful to put up a demonstration at this point, so you'd see even more clearly what we're looking for. Below the demonstration, I have a checklist of things that were missing in some of the first drafts that you might want to be sure you cover in revising the data description part of your proposal.

## A Demonstration of What I'm Looking For in your Revision

Suppose I was proposing a project with the `dm431` data we've studied in class. The following would cover most of the issues specified below, sufficiently.

In the `dm431` study, Better Health Partnership gathered data from 431 Northeast Ohio adults between the ages of 31 and 70 who had a diagnosis in the electronic health record of diabetes, and had at least two visits to a primary care practice in year X and two visits to that same primary care practice in year X-2. (In fact, this isn't quite true - the data are simulated, but we'll pretend it's the case for now, since that is the basis of my simulation.) The data are simulated, and can be shared freely over the internet. I know this because I built the simulation, and I know the data are fake. I have the data in hand, in both `.csv` and `.Rds` formats.

In developing my linear regression models, I will predict the current systolic blood pressure, a quantitative outcome, with some combination of six predictors, as specified in the table below. My key predictor, in which I have the most interest, is which of five `practices` cared for the subject. The other variables of interest include age, sex, type of insurance, LDL cholesterol level now, and systolic BP two years ago. There is also a subject ID code for each of the 431 subjects, which has no analytic value - it just identifies the subjects.

The `dm431` data set contains 431 observations, of which 394 have complete data on the following 6 predictors and my outcome. I'll impute the values of `ldl` as I'm doing the modeling later this semester.

Variable | Role in Model | Type of Variable | Values | Description
--------: | ----------: | ----------: | -----------: | --------------------------------------
`sbp` | Outcome | Quantitative | No missing data, values range from 90 to 208 | Units are mm Hg.
`practice` | Key Predictor | Categorical, 5 levels | A (n = 121), B (n = 133), C (n = 50), D (n = 63), F (n = 64) | There are five practices, no missing data
`age` | Predictor | Quantitative | No missing data, values range from 31 to 70 | Units are years.
`insurance` | Predictor | Categorical, 4 levels | Commercial (n = 164), Medicaid (n = 100), Medicare (n = 123), Uninsured (n = 44) | There are four insurance types, with no missing data
`sex` | Predictor | Categorical, 2 levels | Female (257), Male (174) | No missing data
`sbp_old` | Predictor | Quantitative | No missing data, values range from 85 to 194 | Units are mm Hg, Systolic BP two years ago
`ldl` | Predictor | Quantitative | 37 missing values, other values from 31 to 227 | Units are mg/dl. 

Here is a histogram of my quantitative outcome:

![](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/hist_sbp.png)

------------

## Things That Came Up in Reviewing Your Initial Attempts

In reviewing your revised Study B Proposal (Task 2) on Canvas, make sure you explicitly address the following points, in addition to everything else in the instructions and in the feedback you've received on Canvas.

1. Who gathered the data, and how was it gathered?
2. How do you know that the data can be shared freely, over the internet, with anyone in the world?
    - And if you can't convince me of this, I'm not going to approve the project.
3. Do you have the data in hand, or not? In what form is it (A .csv file, or what?) 
    - If you're waiting for it, who will ensure that you have it in time, and what are you waiting for?
4. What do the rows in the data set (the observations or subjects) represent? People? Something else? 
    - How many are there? How were these subjects selected to participate in the data collection?
5. What do the columns in the data set (the variables) describe?
    - For each variable you have, is it quantitative or categorical, or just an identifying code for the subjects? 
    - For each variable you have, specify whether it is to be used in your models or not, and if so, whether it is an outcome or a predictor.
        - For your quantitative outcome,
            - explicitly demonstrate that the variable is quantitative by specifying the units of measurement, and clarifying what the set of possible values are,
            - if you have the data, state explicitly the number of non-missing observations, as well as the minimum and maximum values
            - if you have the data in R, build a histogram to summarize the data and describe it, briefly
        - For categorical predictors,
            - state explicitly the number of categories that are possible, 
                - note that variables with more than 7 categories will certainly have to be collapsed to hold 7 or fewer categories in your modeling in order to let you interpret the results with the tools you'll have in 431, so if you have a variable with more than 7 categories, mention that you'll have to collapse some of the categories,
            - specify each possible value of the categorical variable that can appear,
            - and, if you have the data, tell us how many (or what % of) subjects have that value, and how many observations are missing.
            - If you're planning to turn a quantitative predictor into a categorical one, specify that, and identify how you'll decide how to split the quantitative predictor into categories.
        - For quantitative predictors,
            - explicitly demonstrate that the variable is quantitative by specifying the units of measurement, and clarifying what the set of possible values are,
            - if you have the data, state explicitly the number of non-missing observations, as well as the minimum and maximum values that you observe in the data
        - Be sure that you specify a quantitative outcome, and a bare minimum of 4 predictors (at least one of whom must be quantitative and one of whom must be multi-categorical). We'd prefer your revision to describe 6-8 (maybe as many as 10 but not more) predictors, so that if we must drop a couple, you'd still have a plausible project.
        - If you have the data, specify the number of complete cases with full data on your identifying variables (like Subject ID) plus your outcome and each of your predictors.

Good luck!
