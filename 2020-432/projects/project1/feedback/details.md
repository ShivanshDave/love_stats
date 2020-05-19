# Project 1: Explaining the Feedback Sheet

Early in the morning of Saturday 2020-03-28, I sent you a document from me (via email) that summarizes our feedback on your Project 1. The material on this page should be useful to you in interpreting what you receive.

I would very much appreciate it if you would do me one favor: I will be happy to address any of your questions about this feedback but **please wait until AFTER class on Tuesday 2020-03-31 to send any questions you have about Project 1 feedback**, please. Thanks.

# 1. Basic Summaries of Minimum Requirements 

Some of this stuff is here because writing it down forced Dr. Love to look closely at everything you did in the portfolios.

## "Basics Complete"

This is the result of an initial "minimal check" of all on-time projects. It should Yes if your project was ON TIME and included:

- R Markdown of your portfolio
- HTML of your portfolio
- R Markdown of your poster
- HTML of your poster
- Raw csv file (unless you were using NHANES data)
- Tidy RDS file
- Your Portfolio HTML includes...
    - Code-folding
    - An automated and clickable table of contents
    - Understandable (but perhaps not 100% appropriate) section headings
    - code to indicate the saving of the tidy Rds file (ideally where you were supposed to show it)
    - session information
    
## Number of Sections

- This is the number of numbered sections in the Portfolio HTML.
- 18 projects had 13, 10 had 14, 9 had 12 and the remaining one had 15.

## Most common packages explicitly loaded in portfolios

Projects | Package(s)
-------: | ------------------------------------
All 38 | `broom`, `magrittr`, `rms`, `tidyverse`
35-37 | `car`, `caret`, `here`, `janitor`, 
30-34 | `GGally`, `ROCR`, 
25-29 | `knitr`, 
20-24 | `naniar`, 
15-19 | `patchwork`, `skimr`,
10-14 | `Hmisc`, `simputation`, 
5-9 | `leaps`, `modelr`, `pROC`, `rmarkdown`, `rmdformats`, `tableone`

Less than five projects loaded the following packages...

- `arm`, `dbplyr`, `e1071`, `Epi`, `foreign`, `gridExtra` 
- `haven`, `kableExtra`, `lubridate`, `MASS`, `mice`, `mosaic`
- `nhanesA`, `plotly`, `posterdown`, `RColorBrewer`, `readxl`
- `sessioninfo`, `survey`, `vcd`, `visdat`

### Notes

- The list excludes misloads of packages that are part of the core tidyverse, and counts only once packages loaded in the same project multiple times.
- Note that loading `rms` also loads `Hmisc`.
- The mean number of packages explicitly loaded was 14.8, with a standard deviation of 3.4. The range was 9-22.

## R version used

- 34/38 students used R version 3.6.2 (2019-12-12)

## Operating Systems

- 20 used Windows
    - 16 used Windows 10 x64
    - 4 used Windows 7 x64 SP 1
- 17 used MacOS
    - 4 used macOS Catalina 10.15.3
    - 3 used macOS Mojave 10.14.6
    - 2 used macOS Catalina 10.15.2
    - 2 used macOS High Sierra 10.13.6
    - 1 each used macOS Catalina 10.15, macOS Catalina 10.15.1, macOS Mojave 10.14, macOS Mojave 10.14.2, macOS Mojave 10.14.4 and macOS Sierra 10.12.6
- 1 used Ubuntu 19.10

## Lines in portfolio

This was, of course, mostly something I collected to force me to open all of your R Markdown files for the portfolio. In all, students produced **36,710** lines of code, just in the portfolios alone. Here's a stem and leaf plot, sort of...

```
 3 | 65
 4 |
 5 | 35 49 55 58
 6 | 24 44 50 81 93
 7 | 29 55 82
 8 | 51 61 67 90 94
 9 | 11 15 19 35 66 98
10 | 01 10 82 83 97
11 | 17 35 44
12 | 
13 | 83 
14 | 11 18 
15 | 02
16 | 
.
.
.
20 | 75
21 | 25
```

So the mean was 966, and the standard deviation 378.

# 2. Description of the Linear Regression Modeling Work (Portfolio Section/Task 10)

There are brief notes in the following areas, all derived from reading the Portfolio HTML document.

## Lin - Missing?

This section describes what you did about missing data in your linear regression (Section 10.)

- 28/38 used a complete case analysis, sometimes because there was no missing data to start with, and sometimes because the investigators dropped missing values.
- The other 10 did at least some simple imputation.

## Lin - Trans?

This section describes what outcome transformation you settled on in your linear regression (Section 10.)

Transformation | Inverse | Inverse Square Root | Logarithm | Square Root | None | Square 
-------------: | ---: | ---: | ---: | ---: | ---: | ---:
Projects | 1 | 1 | 11 | 13 | 9 | 3

## Lin - Augmentation

This section describes what non-linear augmentation(s) you attempted in building Model B (the augmented linear model.) 

Augmentation Type | rcs(5 knots) | rcs(4 knots) | rcs(3 knots) | Interaction Term | Polynomial Term
----------------: | ---: | ---: | ---: | ---: | ---: 
Projects | 20 | 14 | 5 | 12 | 2

Projects attempting more than one type of augmentation are listed multiple times in the table.

## Lin - Validation

This section describes what validation type(s) you attempted in comparing Models A and B. 

Validation Type | 10-fold Cross-Validation | 5-fold Cross-Validation | Training/Test Samples | `rms::validate`
-------------: | --------: | ---: | ---: | ---:
Projects | 13 | 16 | 3 | 24

Projects attempting more than one type of validation are listed multiple times in the table.

## Lin - Winner

Did the investigator(s) select Model A (main effects) or Model B (augmented) as their final linear model?

Model | A | B
------: | ---: | ---:
Projects | 23 | 15

## Lin - Final R2

What was the (validated if available) R-square value for the final linear regression model?

Value | Projects
--------: | ----:
Below 0.1 | 10
[0.1, 0.2) | 6
[0.2, 0.3) | 2
[0.3, 0.4) | 6
[0.4, 0.5) | 2
[0.5, 0.6) | 4
[0.6, 0.7) | 4
[0.7, 0.8) | 3
[0.8, 0.9) | 1
0.9 and above | 0

## Lin - Final Nomogram

Status of the nomogram for the final model

Projects | Comment
----: | --------------------------------------------------------------------
16 | OK, and appropriate back-transformation is part of the nomogram.
11 | Nomogram doesn't provide a needed back-transformation to the original outcome
9 | OK, and model did not use an outcome transformation.

# 3. Description of the Logistic Regression Modeling Work (Portfolio Section/Task 11)

Again, there are brief notes in the following areas, all derived from reading the Portfolio HTML document.

## Log - Missing?

This section describes what you did about missing data in your logistic regression (Section 11.)

- 30/38 used a complete case analysis, sometimes because there was no missing data to start with, and sometimes because the investigators dropped missing values.
- The other 8 did at least some simple imputation.

## Decision Rules

This section describes what cutoff value you used in your decision rules for building Model Y and Model Z confusion matrices. Most groups (correctly) chose the same cutoff value for Model Z that they had used in Model Y.

Cutpoint | 0.5 | 0.065 | 0.1 | 0.2 | 0.3 | 0.4 | 0.8
--------: | --: | --: | --: | --: | --: | --: | --: 
Projects | 25 | 1 | 1 | 4 | 2 | 1 | 2

## Log - Augmentation

This section describes what non-linear augmentation(s) you attempted in building Model Z (the augmented logistic model.) 

Augmentation Type | rcs(5 knots) | rcs(4 knots) | rcs(3 knots) | Interaction Term | Polynomial Term
----------------: | ---: | ---: | ---: | ---: | ---: 
Projects | 10 | 15 | 8 | 18 | 2

Projects attempting more than one type of augmentation are listed multiple times in the table.

## Log - Validation

This section describes what validation type(s) you attempted in comparing Models Y and Z. 

Validation Type | 10-fold Cross-Validation | 5-fold Cross-Validation | Training/Test Samples | `rms::validate`
-------------: | --------: | ---: | ---: | ---:
Projects | 1 | 2 | - | 33

Projects attempting more than one type of validation are listed multiple times in the table.

## Lin - Winner

Did the investigator(s) select Model Y (main effects) or Model Z (augmented) as their final logistic model?

Model | A | B
------: | ---: | ---:
Projects | 26 | 12

## Lin - Final AUC

What was the (validated if available) C-statistic (area under the ROC curve) for the final logistic regression model?

Value | Projects
--------: | ----:
[0.5, 0.6) | 4
[0.6, 0.7) | 9
[0.7, 0.8) | 7
[0.8, 0.9) | 10
0.9 and above | 7

## Lin - Final Nomogram

Status of the nomogram for the final model

Projects | Comment
----: | --------------------------------------------------------------------
28 | OK, and appropriate back-transformation is part of the nomogram.
8 | Missed the opportunity to include the back-transformation to a statement about the probability of the outcome in the nomogram itself.

# 4. Poster Questions

The poster issues posted to the feedback sheet begin with a series of 29 questions that Dr. Love asked of himself and (in most cases) two of the TAs. Remember that the TAs only read the posters, not the portfolios. Dr. Love read both. Consensus responses are posted to the feedback sheet for these 29 items.

Possible responses for questions 1-26 listed below are:

- Yes, definitely.
- Somewhat, but there are some issues.
- No, not really.

## Data Source Questions

1. Are sufficient details provided for you to understand where the data come from?
2. Is this section concise, containing no extraneous information?

## Project Objectives section

3. Is a question is posed for the Linear Model that you understand?
4. Is a question is posed for the Logistic Model that you understand?

## "The Data" section

5. Do you have a clear understanding of who the subjects in the study are?
6. Do you have a clear understanding of what variables are available?
7. Is the section attractively formatted?

## Linear Regression section

8. Do you have a clear understanding of what the outcome is?
9. Do you have a clear understanding of the predictors included in the final model?
10. Do you have a clear understanding about why the final model was selected?
11. Is there at least one useful table or graph?
12. Is there a clear and correct description of an effect size for at least one predictor?
13. Did the project author(s) make good decisions about what to include or exclude?

## Logistic Regression section

14. Do you have a clear understanding of what the outcome is?
15. Do you have a clear understanding of the predictors included in the final model?
16. Do you have a clear understanding about why the final model was selected?
17. Is there at least one useful table or graph?
18. Is there a clear and correct description of an effect size for at least one predictor?
19. Did the project author(s) make good decisions about what to include or exclude?

## Key Findings section

20. Does this section clearly answer the Question about Linear Regression posed in the Objectives?]
21. Does this section clearly answer the Question about Logistic Regression posed in the Objectives?]
22. Does the poster provide at least one potential next step to improve the modeling or the data?]

## Discussion section

23. Does the discussion section clearly address... What was substantially harder or easier than you expected, and why?
24. address... What do you wish you’d known at the start of this process that you know now, and why?
25. address... What was the most confusing part of doing the project, and how did you get past it?
26. address... What was the most useful thing you learned while doing the project, and why?

## General Questions

27. Were there formatting problems in the poster?
    - No, the poster is beautifully formatted.
    - Yes, but just one or two.
    - Yes, several problems.

28. Were there spelling, grammatical or typographical errors in the poster?
    - No, the poster is essentially free of these mistakes.
    - Yes, but just one or two.
    - Yes, several problems.

29. Which best describes the decisions made by the poster's author(s) regarding what to include and what not to include?
    - They made generally strong decisions about what to include and what not to include.
    - They made some mistakes, and more often they included material that was not helpful.
    - They made some mistakes, and more often they left out things that should have been included.    

# 4. Comments on the Portfolio

The portfolio comments were written by Dr. Love, alone.

# 5. Comments on the Poster

The poster comments were written by the TAs and by Dr. Love. There's no clear indication of who wrote what. Sorry.

# 6. Scores

- The score on the proposal was out of a possible 25 points.
    - Successful on-time submission of the proposal got you the full 25 points.
- The score on the portfolio was out of 25 points.
- The score on the poster was out of 50 points.
    - Dr. Love determined the grades on the portfolio and the poster based on his overall assessment of each, independently. 
- The overall score on the project is the sum of those three subscores, so the maximum possible score was 100 points.

## Class-Wide Performance

The strongest project received a score of 94.

- As with the rest of the course, a grade of 85-100 should be thought of as some form of an A.
- A grade of 70-84 should be thought of as some form of a B.

Portfolio Score | 22 or 23 | 20 or 21 | 18 or 19 | 16 or 17 | 15 or below
-----: | :---: | :---: | :---: | :---: | :---:  
Projects | 5 | 11 | 10 | 7 | 5
"Grade" | A | A- | B+ | B | B- or lower

Poster Score | 44 or 46 | 40 or 42 | 36 or 38 | 32 or 34 | 30 or below
-----: | :---: | :---: | :---: | :---: | :---:  
Projects | 6 | 8 | 12 | 7 | 5
"Grade" | A | A- | B+ | B | B- or lower

Project 1 Score | 90-94 | 85-89 | 80-84 | 75-80 | below 75
-----: | :---: | :---: | :---: | :---: | :---:  
Projects | 6 | 6 | 12 | 9 | 5
"Grade" | A | A- | B+ | B | B- or lower

For details on how the Project 1 score is incorporated into your class grade at the Midterm and overall, [visit this link](http://bit.ly/432-2020-grading-plan).

Thank you all for your hard work on your project.


