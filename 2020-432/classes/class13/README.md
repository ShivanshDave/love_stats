# 432 Spring 2020 Class 13: 2020-03-03

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Class 13 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class13/432_2020_slides13.pdf) | [Class 13 Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class13/432_2020_slides13.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Key Topic

Ridge Regression and the Lasso.

## Today's Announcements

1. Dr. Love will hold additional **walk-in office hours** on Tuesday 2020-03-03 and Thursday 2020-03-05 from Noon to 12:45 and from 2:15 to 3 PM in Wood WG82-J specifically to help address questions related to project 1 portfolio and/or poster work. 
    - I'm hoping you'll use this opportunity to show me something specific from your portfolio or from your poster and ask for advice about how to present something most effectively. 
    - This is just to help supplement the TA office hours, which will continue to be held as usual.
    - If you have a question about coding, it's generally more effective for you to send your R Markdown and csv and a description of the problem you're having to 431-help, or to visit TA office hours.
2. Quiz 1: I've finished grading and sent you my thoughts via email. 
    - [Post-Quiz materials are posted here](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/postquiz1). This includes: 
        - the [Answer Sketch, Rubric and Results document](https://github.com/THOMASELOVE/2020-432/blob/master/quizzes/postquiz1/quiz1_with_sketch.pdf) (which I updated at noon today to fix Question 11's answer) and 
        - the [R Markdown of code and evaluation for Question 2](https://github.com/THOMASELOVE/2020-432/blob/master/quizzes/postquiz1/quiz1_checkquestion2code.Rmd).
    - If you didn't do as well as you'd hoped, I'm sorry. I hope you all do very well on the next Quiz.
    - As a group, there were some questions ([answer sketch](https://github.com/THOMASELOVE/2020-432/blob/master/quizzes/postquiz1/quiz1_with_sketch.pdf) has results for each item) where less than 75% of available points were awarded. Those are the questions I'll be looking at again when I develop Quizzes 2 and 3. 
    - I thought every item was reasonable except maybe Question 7a, but since that was only 1 point, I left it alone.
    - In the Minute Paper after Thursday's class, I'll be asking you how long it took you to do the Quiz.
    - My bonus office hours today and Thursday are designed to be about the project 1 portfolio and poster. Please stick with that, rather than using the time to rehash the Quiz. 
        - There's not much we can do now about Quiz 1 (and whatever we can do, we can probably do via email), but there's a lot we can do about Project 1, and it's far more important for your grade in the course.
        - The 3 Quizzes (Quiz 1 worth 75 points, Quiz 2 worth 75 points, Quiz 3 worth 100 points) combined are worth 15-25% of your course grade. The 2 Projects are together worth 40% of your Course Grade.
3. Homework 3 grades were posted on 2020-02-27 to http://bit.ly/432-2020-grades. 
    - We built a [Google Doc containing several of the essays we really enjoyed in response to Question 6](https://docs.google.com/document/d/1krZRnMTniOKfU0EqlE-dnJjqP4n7hBgFB7JSPN-x8mQ/edit?usp=sharing).
4. *Homework Regrades*. A reminder...
    - If we've added your points up incorrectly on a Homework, send an email to Dr. Love before 5 PM 2020-04-30.
    - To request a Homework regrade for any other reason, fill out the Form at http://bit.ly/432-2020-homework-regrade-requests  any time before 5 PM on 2020-04-30. Dr. Love will review all of those requests in a batch then. [See the Grading Errors section here](https://github.com/THOMASELOVE/2020-432/blob/master/homework/README.md#grading-errors) for a little more detail.
5. [Instructions for Homework 4](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw04) are now available.
6. Minute Paper after Class 12 feedback is available at http://bit.ly/432-2020-minute12-feedback.
7. In response to some Minute Paper questions about non-linearity, spending degrees of freedom and the Spearman rho-squared plot, [I wrote up some thoughts](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class13/nonlinearity.md). Please take a look. I also encourage you to look closely at the relevant sections of [the Course Notes](https://thomaselove.github.io/2020-432-book).
8. There have been several updates to the [Course Notes](https://thomaselove.github.io/2020-432-book), in particular there's a new Chapter 16 on Multiple Imputation (with `mice` and with `aregImpute`) in Linear Regression.
9. [Project 2 instructions](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) are started, and the rest will appear on 2020-03-17 by 1 PM. The answer to all questions not already answered there is probably "I'm not sure. It depends on how Project 1 goes."

## Reminders/Notes (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
----: | ---------------------------------------------------------------
03-06 | There will be a Minute Paper after Class 14, due at 2 PM.
03-09 | [Project 1 Posters/Portfolios](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) are due at 2 PM.
Break | No class and no TA office hours from 03-09 through 03-13. `431-help` will be open.
03-17 | [Project 2 Instructions](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) should be available by 1 PM.
03-20 | There will be a Minute Paper after Class 16, due at 2 PM.
03-23 | [Homework 4](https://github.com/THOMASELOVE/2020-432/tree/master/homework) due at 5 PM
03-26 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) made available at 5 PM
03-30 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) due at 2 PM
04-01 | [Project 2 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) due at 2 PM

## Other Things

1. [Nathan Yau tweeted](https://twitter.com/flowingdata/status/1233169893022826496?s=11) that there's [a new candidate for funny pie chart placeholder](https://www.reddit.com/r/funny/comments/f78kuo/i_hear_you_like_pie_charts/)...

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class13/figures/piechart.png)

2. I just learned of the existence of the [Tidy Tuesday Podcast](https://www.tidytuesday.com/). There are about 15 episodes available, each about 5 minutes long. I hope that you find these helpful to you!
    > TidyTuesday is a weekly podcast and community activity brought to you by the R4DS Online Learning Community. Our goal is to help R learners learn in real-world contexts.
3. [Biostats4You](https://biostats4you.umn.edu/) from the University of Minnesota may be of interest to you. 
    > (The site) was developed to serve medical and public health researchers and professionals who wish to learn more about biostatistics. The site contains carefully selected and vetted training materials especially suited for a non-statistician audience.
4. The [useR! conference](https://user2020.r-project.org/) will next be held July 7-10, 2020 in St. Louis. 


## One Last Thing

From FiveThirtyEight: [Pick Your Own Super Tuesday Winners And Watch The Race Change](https://projects.fivethirtyeight.com/super-tuesday/)
