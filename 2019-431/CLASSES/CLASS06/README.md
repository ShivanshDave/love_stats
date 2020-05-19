# 431 Fall 2019 Class 06: 2019-09-12

## Today's Slides

- Class 6 slides will be available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS06/431_class-06-slides_2019.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS06/431_class-06-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.
- Have you checked out the [RStudio Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)?
- Today's analyses again use data from the [National Health and Nutrition Examination Survey](https://www.cdc.gov/nchs/nhanes.htm), and focus on visualization and working with categorical data.

## Reminders

1. I've updated the [Course Calendar](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md) to include all deliverables I am aware of, and I don't think there will be more.
2. [Homework C](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/C) is due Friday 2019-09-13 at 2 PM.
3. Please read the Introduction and Chapter 1 of Silver's *The Signal and the Noise* by 2019-09-17.
4. [Homework D](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/D) is due Friday 2019-09-20 at 2 PM.

---

From [@allimoberger (Allison Moberger) 2019-01-15](https://twitter.com/allimoberger/status/1085268564821585921) quoting Hadley Wickham...
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS06/images/2019-01-25_moberger_better.png)

## Homework B

- Grades and Comments for Homework B are now available. See [the Homework B post-deadline page](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/B/post-deadline.md) for details and reminders.
    - In grading, we let typographical and syntax errors mostly slide this time, losing at most a point or two. Going forward, and certainly by Homework D, expect us to hold you to a higher standard in this regard.
- On all homeworks, we ask you to submit both an R Markdown file **and** an HTML file. 
    - It's great that you can also knit to PDF or to Word. Congratulations! But please, for the purposes of the Homework, do it the way we want you to do it.
    - If you're having trouble knitting and the error message isn't helpful, update your packages, and look closely at the YAML, as possible culprits.
    - Starting with Homework D, we're going to penalize you in grading if you don't accomplish this on time.
- When doing your Homework, knitting the R Markdown file *isn't* the last step before posting to Canvas. **Proofreading the HTML file** is the last step before posting to Canvas.
    1. Make sure your name is in the author section of the YAML.
    2. Make sure you haven't printed a long batch of output pointlessly.
        - Common problem: You printed a full data frame, not just the first 10 rows (and that indicates you don't have a tibble)? Actually, no need to print a full data frame in HW or in project, ever.
    3. Make sure all of your graphs show up.
        - Common problem: You left out a + in a ggplot so it built some of the plot and then fell apart
    4. Make sure you can successfully hide/show all of your R code.
    5. Make sure you don't have any warnings (messages are OK) in the output.
    6. Make sure you haven't left in any of Professor Love's instructions from the template.

Also, when asking for coding help through `431-help`, it would help us help you if you either:

1. **better**: post your R Markdown file to the 431-2019 workspace in RStudio Cloud and tell us about it (specifying your R Markdown's file name), so we can run it ourselves to diagnose and help fix your problem. (Sometimes just running it yourself in RStudio Cloud solves your problem, actually) or
2. **still ok**: send us your R Markdown file in your email.

## Feedback (Please take a look!)

- In Homework B, Question 7, I asked you to ask me a question. I got 61 questions, and [answered every single one of them here](http://bit.ly/431-2019-hwB-question7-responses). Please take a look.
- [Reactions to the Minute Paper after Class 05](http://bit.ly/431-2019-minute-05-response) are now available.

---

## The Course Project

The current draft of the Project Instructions [is posted here](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/README.md). 

*Study A*: take a data set we will build as a class and use it to make some visualizations and comparisons without adjustment for covariates (everyone has the same data set but selects a subset of different variables from it for their comparisons and visualizations)

*Study B*: take a data set you find out in the wild that meets certain specifications and use it to build predictions for a quantitative outcome using a linear regression model (everyone has a different data set)

- We'll take questions today, and also **facilitate an opportunity for you to meet potential "partners" for the project** (Thanks for that suggestion!) 
- I added extensive material this morning.
    - Deadlines are now [posted to the Calendar](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md), and are part of the [Instructions](https://thomaselove.github.io/2019-431-project/), too.
    - Details on grading are also part of the [Instructions](https://thomaselove.github.io/2019-431-project/) now.
- Coming in October:
    - Details on formatting requirements, templates for the portfolios (Task 6).
    - Demonstration project portfolios are also coming.
- First three things to address:
    - By the start of class on 2019-09-24, you need to know the answer to "Will I work alone, or with a partner?"
    - By 2019-09-30, you (and your partner, if you have one) must finish the [Project Scheduling Form](http://bit.ly/431-2019-project-scheduling).
    - You need to identify a data set for Study B, that meets the specifications. You'll need to tell us about it in Task 2, due 2019-10-08.
- Get more information at `431-help`, as questions arise from here.

## Two Project-Related Tips

1. Check out [Data is Plural](https://tinyletter.com/data-is-plural): A weekly newsletter of useful/curious datasets.
2. You may be interested in Krista DeStasio's [R Best Practices (for Research Projects)](https://kdestasio.github.io/post/r_best_practices/).

## One Last Thing

- [This here](https://twitter.com/jpmarindiaz/status/1171462067464704001) links to an inspired bit of silliness.
    - Learn more about [DataSketch at its Kickstarter](https://t.co/arTIogalUZ?amp=1) and its effort to bring open source data visualization to developing countries.
