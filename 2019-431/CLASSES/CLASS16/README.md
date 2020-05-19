# 431 Fall 2019 Class 16: 2019-10-24

## Today's Slides

- Class 16 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS16/431_class-16-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS16/431_class-16-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Reminder of Upcoming Deadlines

Reading: You should be through Chapter 8 of *The Signal and the Noise* by now.

1. [Study B Task 3 (Data Update)](https://thomaselove.github.io/2019-431-project/task3b.html) is due at 2 PM Friday 2019-10-25.
2. The Study A Survey is available at http://bit.ly/2019-431-survey and you will complete [Study A Task 4 (Taking the Survey)](https://thomaselove.github.io/2019-431-project/task4a.html) by 10 AM on Monday 2019-10-28.
3. [Study A Task 5 (Comparison Plan)](https://thomaselove.github.io/2019-431-project/task5a.html) is due at 2 PM Wednesday 2019-10-30.
4. [Homework G](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/G) is due at 2 PM Friday 2019-11-01.
5. [Study B Task 4 (Sharing the Raw Data)](https://thomaselove.github.io/2019-431-project/task4b.html) is due on 2019-11-04 at 9 AM via Canvas.

## So, I'm back from study section ...

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS16/images/phd_2016-09-16.PNG) 

from Jorge Cham at [PhDComics, published 2016-09-06](http://phdcomics.com/comics/archive.php?comicid=761)

## Today's Agenda

- Working through the README
- Comparing Means of Populations based on Paired Samples

## Things Other Than the Project

1. Dr. Love's [Response to the Minute Paper after Class 15](http://bit.ly/431-2019-minute-15-response) is available now. 
    - The next Minute Paper will be after Class 19.
2. [Course Notes](https://thomaselove.github.io/2019-431-book/) - there is a new version posted, full of corrections.
    - A student (to whom I am very grateful) found errors (or typos/confusing references, at least) in Sections 4.2, the start of Chapter 6, section 7.6, section 8.3, 8.4, 8.6, 9.6, 10.3 and 11.2, 11.4 and 11.6. 
    - I then found errors/typos/glitches with references in Chapters 16, 19, 20, 21, 22 and 23, as well.
    - I hope others will pick up this mantle and help us eliminate problems. Just send them to 431-help.
3. All remaining Homeworks are now posted, including the new [Homework I](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/I), and I moved the deadline back to 2019-12-01 (Sunday after Thanksgiving) at 5 PM.

------------

# About the Project

## Project Study A

1. All project small groups have completed Tasks 2 and 3 for Study A. That's the end of the small groups for the project.
2. [Study A Task 4 (Taking the Survey)](https://thomaselove.github.io/2019-431-project/task4a.html) (due Monday 2019-10-28 by 10 AM) involves actually taking the survey.
    - Take the survey at http://bit.ly/2019-431-survey. Thanks to those of you who've gotten started on this already.
    - **Clarification** Regarding Q039: In the past week, how many times have you purchased coffee or tea?
        - Since you can purchase either prepared or unprepared coffee/tea in most grocery stores and coffee shops, I interpret this question to refer to either prepared or unprepared coffee/tea.
3. [Study A Task 5 (Comparison Plan)](https://thomaselove.github.io/2019-431-project/task5a.html) is due at 2 PM on Wednesday 2019-10-30, and you now have what you need to complete that Task. http://bit.ly/431-2019-studyA-codebook links to a Google Drive folder.
    - In that folder, there is a Google Doc containing all of the items, possible responses, scoring instructions and (critically for Task 5) the item numbers.
    - In that folder, there is also a Google Sheet which tells you what the data set variables will be when I send you the data on Halloween.
    - There is also a PDF of the Google Form for the survey located in that folder, if you want it.

## Project Study B

1. Study B Proposal Titles and Data Sets are posted at http://bit.ly/431-2019-studyB-proposal-status. All have been accepted. 
2. [Study B Task 3 (the Data Update)](https://thomaselove.github.io/2019-431-project/task3b.html) is due at 2 PM Friday 2019-10-25 via Canvas. It's simpler than the Proposal.
3. A [Google Drive Folder](http://bit.ly/431-2019-studyB-example) containing Dr. Love's [Study B Course Project Example](http://bit.ly/431-2019-studyB-example) portfolio is also available now. (A similar item for Study A will appear by 2019-11-05.)
4. [Study B Task 4 (Sharing the Raw Data)](https://thomaselove.github.io/2019-431-project/task4b.html) is due on 2019-11-04 at 9 AM via Canvas. There's no need to share variables you will not use in your study. See tip 1 below.
5. [Study B Task 5](https://thomaselove.github.io/2019-431-project/task5b.html#the-task-5) is due in early December.

### Introducing 43 Course Projects: Part 1

Today, we'll meet the investigators working with NHANES data. I think in each case, these folks can be working with data from both the 2013-14 and 2015-16 administrations of NHANES, although at least one set up their proposal differently.

Investigator(s) | Title          | Outcome | Key Predictor(s)
:-------------------: | -------------------------------------------| ------------------------------ | --------------------
Stephanie Wood | Drunk and Drowsy: Does alcohol use affect sleep? | SLD012 (How much sleep do you usually get at night?) | mean drinks on days you drink
Timothy Walker | What does health feel like to you? | Body Mass Index | How do you consider your weight - Overweight, Underweight, About Right, Don't Know
Alena Sorensen and Emily Tyszka | Less money = more cholesterol? | Lab-determined LDL | statin usage and SES
Anna Miller | Effect of Poverty Level on LDL-cholesterol Level | Lab-determined LDL | Ratio of Family Income to Poverty (ceiling effect at 5)
Ahmet Hacialiefendioglu | Association of LDL-cholesterol and diabetes | Lab-determined LDL | Doctor told you you have diabetes (yes/no/borderline)
Rebeka Bordi | High Cholesterol and Blood Pressure Regulation in NHANES subjects | SBP (and also DBP) | LDL (pick LDL or HDL or Total but not all three)
George Hoeferlin and Youjoung Kim | Predicting Biochemical Health Based on Personal Care Product Use and Income | Triglycerides and Biochemical Index | poverty category, amounts of several specific chemicals
Paola Saroufim | Hemoglobin A1c and Waist Circumference in NHANES Adults | Waist circumference | A1c
Seth Rotz | Poverty's Effect on Iron Deficiency in Young US Children | Ferritin blood level in kids 2-5 | poverty (income categorized)
Ebtesam Alshehri and Carolyn Goldschmidt | Predictors of adolescent obesity at home and at school | BMI in kids 12-15 | Have PE during school days (Yes/No/DK/Refused)
Hussam Alqahtani and Kimberly Noriega | Cognitive Impairment and Blood Pressure in the Elderly | [symbol-digit substitution test](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6291255/figure/F1/) (assesses processing speed and working memory) | Systolic BP

In subsequent classes, I'll be asking the rest of you to provide us a similar reminder of your outcome and key predictor(s).

### Data Tips Related to Project B

1. Suppose you download an enormous .csv file, like [this one for the 500 cities data](https://chronicdata.cdc.gov/500-Cities/500-Cities-Local-Data-for-Better-Health-2018-relea/6vp6-wxuq). I suggest you first restrict the .csv file to the columns you're actually interested in using, possibly with R, but more likely with Excel. Then resave it as a much smaller file.
2. In doing your work, I **strongly** encourage you to work in R Markdown rather than an R script, from the very beginning. It takes an additional 5% of effort at the beginning, but pays big dividends when you get stuck and need help from us.
3. Project-Oriented Workflow: `rm(list = ls())` and `setwd` are **horrible** things to put at the top of an R script. Don't do that, and [here's a blog post from Jenny Bryan explaining why](https://www.tidyverse.org/articles/2017/12/workflow-vs-script/).
4. **Only load packages you're using**. Packages I would load for any regression-based project (like Study B) include: `here`, `janitor`, `magrittr`, `broom` and `tidyverse`. It will make me happier to see you including these packages, but only if you use them. I don't know how you could avoid using `broom` and `tidyverse` in Study B.
5. Data types that I won't let you use in this project:
    - Categorical variables with more than 7 levels are a big problem, as predictors in this project. Collapse.
    - Time to event data involving censoring (like survival data) where a status (dead/alive) and time are both involved.
    - Longitudinal data (unless you're creating simple differences or ratios comparing after to before in an outcome.)
    - Hierarchical data that requires you to mix different units of analysis in your modeling. If your data are about counties, you want all of the data to be measured at the level of the county, and not (for instance) at the level of the state or the zip code.
6. Avoid using a binary variable as a predictor if it has less than 5% of the subjects in your data in its smaller group.
    - For example, if you have a phenotype variable in your study of 270 observations, and 261 are "wild type" and 9 are "mutant", then your phenotype variable isn't a useful predictor for our purposes, because 9 is less than 5% of 270.
7. Avoid using any categorical variable level that has less than 10 (or less than 1%) of your observations endorsing it. Instead, collapse the data a bit.
    - For example, if you have a race category with 5 levels, like White, Black or African-American, American Indian or Alaska Native, Asian, and Native Hawaiian or Other Pacific Islander, but you have 200 White, 300 Black or African-American, and less than 10 people in the other three levels combined, then you probably have in fact a binary variable that should be operationalized as either [a] "White / Non-White" or [b] "Black or African-American / All Others" depending on which way you decide to collapse the categories.
8. You may find that you have -999 or some other value taking the place of NA in your data. If that's the case, you want to add code in R to change all of the -999s to NA first, then go through the process of identifying what you have. If you don't know how to do this, take a look at `na_if()` at https://dplyr.tidyverse.org/reference/na_if.html.
9. Some of you wonder why I don't like research questions about whether systolic blood pressure *correlates to* body-mass index, for example. It's because everything is correlated with everything else, practically, especially in an observational study. 
    - What you're trying to talk about, usually, is whether one can predict the other, or whether one causes the other, and delineating whether you're trying to do prediction (which is what your 431 project is doing) or estimating a causal effect (which is a topic for 432 and beyond) is important. So don't use "correlates to" or anything like it.
10. There are [lots and lots of ways to divide the United States into regions](https://en.wikipedia.org/wiki/List_of_regions_of_the_United_States). You might as well use one that you can cite should you be confronted with the need.

-----------

## Miscellaneous Things I've Been Meaning to Pass Along

1. I encourage you to read Douglas Altman on [How to obtain the confidence interval from a P value](https://www.bmj.com/content/343/bmj.d2090.short) in *BMJ* 2011, if you're confronted with an article or report that provides point estimates and p values only, and you want instead to get (at least an approximate) confidence interval.
2. Jeff Leek has [a nice little package called slipper](https://github.com/jtleek/slipper) to help you do bootstrapping using the tidyverse. I like it.
3. Some of you may be interested in using [the ggforce package](https://ggforce.data-imaginist.com/) to customize your visualizations. [Here's a nice blog post on what ggforce can do](https://rviews.rstudio.com/2019/09/19/intro-to-ggforce/).
4. [Why should I use the here package when I'm already using R Projects?](https://malco.io/2018/11/05/why-should-i-use-the-here-package-when-i-m-already-using-projects/) is worth your time if you're asking that question.
5. Those of you wanting to learn more about the p value controversy will get plenty of that in 432. But two key sources that we'll study more closely next semester are:
    - [Statistical Inference in the 21st Century: A World Beyond *p* < 0.05](https://amstat.tandfonline.com/toc/utas20/73/sup1) from 2019 in *The American Statistician*
    - The American Statistical Association's 2016 [Statement on p-Values](http://amstat.tandfonline.com/doi/full/10.1080/00031305.2016.1154108): Context, Process and Purpose.
6. For those of you working with spreadsheets in the real world, I heartily recommend [Data Organization in Spreadsheets](https://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989) by Karl W. Broman and Kara H. Woo in The American Statistician, 2018 Special Issue on Data Science, or you can [read the PeerJ preprint version](https://peerj.com/preprints/3183/).
7. From the Ten Simple Rules series at PLOS Computational Biology, I also recommend:
    + [Ten Simple Rules for Effective Statistical Practice](http://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1004961) by Kass RE et al. 2016
    + [Ten Simple Rules for Graduate Students](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.0030229) by Gu J Bourne PE 2007
    + [Ten Simple Rules for Better Figures](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003833) by Rougier NP Droettboom M Bourne PE 2014
    + [Ten Simple Rules for Creating a Good Data Management Plan](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004525) by Michener WK 2015

----------------

# One Last Thing

- [Do Americans Support Impeaching Trump?](https://projects.fivethirtyeight.com/impeachment-polls/) by Aaron Bycoffe, Ella Koeze and Nathaniel Rakich at FiveThirtyEight.

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS16/images/impeach_538.PNG)
