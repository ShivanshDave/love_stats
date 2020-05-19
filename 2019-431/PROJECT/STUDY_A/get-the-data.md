# Getting & Managing Data from the 2019 Survey

## Having Trouble? NEW! PDF FILE WITH HINTS!

On 2019-11-22, I posted a [revised set of data files](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/STUDY_A) (removing all apostrophes, I think) and also [posted this PDF document](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-describe-after-merging-with-hints.pdf) and the [R Markdown I used to make it](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-describe-after-merging-with-hints.Rmd) which walks step by step through how I created the project directory so that `here()` works as you'd expect, then imported the data sets, then merged them, then generated summaries for all variables in Project Study A. Please look this over if you're having any trouble.

-------

The data for the survey are available in five separate files, which you will need to merge together to complete your analyses. These files were last updated on 2019-11-22, and they are:

- [`studyA-2019-student-data-01.csv`](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-student-data-01.csv), which contains the `subject` variable, and the first 15 questions for all 67 subjects (labeled R-01 through R-67)
- [`studyA-2019-student-data-02.xls`](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-student-data-02.xls), which is an **Excel** (.xls) file containing the `subject` variable and items Q-016 to Q-089 for the first 34 respondents (R-01 through R-34)
- [`studyA-2019-student-data-03.xls`](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-student-data-03.xls), which is an **Excel** (.xls) file containing the `subject` variable and items Q-016 to Q-089 for the remaining 33 respondents (R-35 through R-67)
- [`studyA-2019-student-data-04.csv`](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-student-data-04.csv), which contains the `subject` variable and the remaining items and scales for the first 34 respondents (R-01 through R-34)
- [`studyA-2019-student-data-05.xls`](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-student-data-05.xls), which is an **Excel** (.xls) file containing the `subject` variable and the remaining items and scales for the remaining 33 respondents (R-35 through R-67).

In order to merge the files, you will need to first read them into R, using appropriate tools for comma-separated text (`.csv`) and for Excel (`.xls`) files, and then you will need to merge and combine them. Note that each of the five data files contains the respondent ID information, and that will be the key variable for your merging and combination work. I have provided an illustration of what you need to do in terms of merging and combining data [on this page](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/merging-advice.md).



## The Codebook for the Data

The codebook for the data is found at http://bit.ly/431-2019-studyA-codebook, which links to a Google Drive folder.

- In that folder, there is a Google Doc containing all of the items, possible responses, scoring instructions and the item numbers.
- In that folder, there is a **substantially augmented** Google Sheet which tells you some key information on all variables.
- There is also a PDF of the Google Form for the survey located in that folder, if you want it.
- Also posted there now is a subfolder called Data for 2019 containing the data sets, and also a PDF describing the data after appropriate merging and combination. Specifically, the studyA-2019-description-after-merging file includes the results of running `Hmisc::describe` on the entire data set, and also running `tabyl` on the three items where respondents were asked to "Check All That Apply". 

## Key Steps in Data Management for Project Study A

1. **Merging and Combining Files** The first step in your Portfolio (Project Task 6) for Study A (the Course Survey) will be to create a complete data file, combining all five of these smaller files within R. The code in R that you write must take the original five files (.csv and .xls) and result in an initial tibble (which I suggest you call `sur2019_full` in R) containing all 165 variables described in the [codebook](http://bit.ly/431-2019-studyA-codebook), for all 67 respondents. 
    - To help you with this a little bit, I've [posted an illustration of what I needed to do to merge and combine](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/merging-advice.md) the (somewhat similar) 2018 survey data [at this link](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/merging-advice.md).

2. **Pruning the Full Data Set down to the Variables You Will Actually Use** Having created the `sur2019_full` tibble in R, you will then use the `select` function in the tidyverse to build a new tibble containing only the variables you will actually use (plus the respondent IDs). That new tibble (which you should name something that has meaning for you) will be your analytic data set for each of the six analyses you will perform. This tibble should still have 67 rows (respondents) but it will have many fewer than 165 columns. Of course, you'll have to know exactly which columns you will be using in your Analyses, and that may well require some revision as you move along.

3. **Other Data Management** Once you have this analytic data set, you'll likely need to calculate new variables (like BMI, for example,) or perhaps create new categorical variables (factors) or collapse some of the existing factors. There are no missing data in this year's Study A Survey.

Once you have accomplished these steps, the remainder of your analyses can and should be modeled on the template and analyses contained in the Study A demonstration project which will be provided to you by 2019-11-05.

Let us know at **431-help** if you have any questions.

