# 431 Course Project Page

- Course Project instructions are at https://thomaselove.github.io/2019-431-project/.
    - This remains **work in progress**. 

## Project Portfolio Examples

- For Study A (the Course Survey), [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/EXAMPLE/README.md) to review the Example Portfolio.
- For Study B (your data) [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_B/EXAMPLE/README.md) to review the Example Portfolio.

## In the Project Portfolio (Task 6 in Study A and Task 6 in Study B)

1. you shouldn't hide any code at all, anywhere. You should hide unnecessary warnings and messages to make your output more attractive, but `echo = FALSE` is no longer permitted in your project work. If your results look like my Examples, you'll be fine.
2. you must load all of the packages you plan to load at the start of your R Markdown file. 
3. you must present NO code without an explanation, and every bit of your work should be preceded by an appropriate section heading or subheading to form an attractive table of contents.
4. you must use the `here` package and do so appropriately.
5. you must set `comment = NA` as I have done in every bit of R Markdown work I've shown you to date.
6. you must use an actual name (definitely not `data` or `data1` or anything generic like that) for each data set you generate in R.

--------------

# Older Materials follow...

## Project Study A (Update as 2019-10-31)

1. Everyone has completed Tasks 2-5 for Study A. The project small groups are now disbanded.
2. The Google Doc codebook folder (which has an updated Google Doc describing each item in detail, and an updated Google Sheet of the items you will receive in the data sets) will remain available at http://bit.ly/431-2019-studyA-codebook for the rest of the semester. There is a subfolder there called *Data for 2019* that contains some new key pieces of information.
3. [Visit this link](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/get-the-data.md) to get the data.
4. Your first task in building the data you'll need to complete Study A will be to **merge and combine** the five data sets appropriately to produce a complete data set with 67 observations (rows) and 165 columns. All merging and combining of files must be done as part of your R Markdown portfolio for Study A. [At this link](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/merging-advice.md), I provide some advice on doing this merging and combining work.
    - Even if you (somehow) don't need any of the variables in one or more of these files, you will still need to demonstrate that your starting file for Study A has 67 rows and 165 columns, and has been correctly merged and combined.
5. I have also provided a PDF description of the data after it has been correctly merged as part of the *Data for 2019* subfolder in the Google Drive codebook. This is simply the result of running `Hmisc::describe()` on the correctly merged data, plus the results of running `tabyl` on the three items where respondents were asked to "check all that apply." 
    - You'll see that one item (Q-076) showed no variation at all, and thus should not be used in your analyses. It's the question about whether you carry a smart phone. 
    - Several other items, as you'll see, show categories with less than 10 respondents endorsing them. I don't want you to use those variables with collapsing the categories so that all levels have at least 10 respondents. This may, as a result, require you to adjust your analytic plans for Study A.
6. Everyone has now submitted a sufficient version of Study A Task 5 (the Survey Comparison Plan.) Thanks. [I've reviewed them all, and my comments are here](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/comparison-plans.md). Please review what you submitted in light of those comments, and follow the instructions [provided there](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/comparison-plans.md).

--------------

## First Steps

- By the start of class on 2019-09-24, you need to know the answer to "Will I work alone, or with a partner?"
- By the end of September, you (and your partner, if you have one) must finish the [Project Scheduling Form](http://bit.ly/431-2019-project-scheduling).
- By October 8, you will need to identify and register a Study B data set that matches our specifications, as part of the Proposal Task (Task 2).

## Regarding Data for Study B

1. You must have at least 250 and no more than 2,500 observations. (If you have more than 2,500 observations, you'll look at a subset that fits in that limit.)
    - If you have a fascinating data set with 200-249 observations, contact Professor Love with some details in advance (including available variable descriptions and your proposed research question) to see if he will provide you special dispensation. In most cases, he'll recommend you find another set for 431, and consider using your fascinating data in one of your 432 projects, which have less stringent rules. If you have less than 200 observations, find other data.

2. Hierarchical (or multi-level) data is not what we want for 431, either. A few quick examples of what **will not** work for 431 (but *might* be OK for one of the 432 projects)...
    - Suppose you have data measured at the county level for counties located in several states, and want to include both county and state-level variables in your model. You must have the same unit of observation for each row in your data set, and for each variable you are studying.
    - Suppose you have data on a set of patients (where the predictors are all measured at some baseline point in time), and you want to assess their outcome (measured a year later.) That's OK, but you cannot include longitudinal measurements in the predictors, at all, and you cannot include anything longitudinal in the outcome except a simple difference between the outcome a year later and the outcome at baseline.
    - Suppose you have time series data from a series of hospitals, and you want to study the effects of changes in quality ratings over time on some outcome in the future, so you have the same hospitals at each time period, and want to include some hospital-level predictors as well as measures for each hospital at separate times as predictors. Not in 431. 


## Special Links

- [Old class surveys (for Study A in 2014-2018) are here](https://github.com/THOMASELOVE/2019-431-project/tree/master/oldsurveys).
