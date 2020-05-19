# 432 Spring 2020 Class 21: 2020-04-09

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 21 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class21/432_2020_slides21.pdf) | [Class 21 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class21/432_2020_slides21.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 21 is available here](https://cwru.zoom.us/rec/share/5JxvLaDZ7mNOQ6vyrxqHcK47GovrX6a8gSVPrPVfxRwYG0gIcSxK_U89XaMUmoiW?startTime=1586451605000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a white board for communication with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.
- The [COVID-19 Resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) will remain available through April.
- **NEW!** [Things I Won't Get To This Semester](https://github.com/THOMASELOVE/2020-432/blob/master/not_this_semester.md)

## Announcements

1. There is a [Minute Paper after today's class](https://bit.ly/432-2020-minute-21). Complete it by Sunday at 9 AM to make the feedback and avoid worried emails from Dr. Love.
2. I'm going to implement a password for our Zoom classes after today's class. If you don't remember the course password, visit Canvas, and check out the Announcements. There, Dr. Love will remind you.
3. I've started a page of recommendations regarding [Things I Won't Get To This Semester](https://github.com/THOMASELOVE/2020-432/blob/master/not_this_semester.md) that I think might be worth your time.
4. A good resource for studying time-to-event data and survival analysis in R is [this chapter](https://argoshare.is.ed.ac.uk/healthyr_book/chap10-h1.html) of [HealthyR: R for Health Data Analysis](https://argoshare.is.ed.ac.uk/healthyr_book/) by Ewen Harrison and Riinu Pius.
5. Yihui Xie has begun to write an [R Markdown Cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/). The [R Graphics Cookbook](https://r-graphics.org/) by Winston Chang continues to be one of the most useful things ever.

## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Sun | 04-12 | [Minute Paper after Class 21 is now available](https://bit.ly/432-2020-minute-21). Submit before 9 AM Sunday to make the feedback.
Tue | 04-14 | Be sure you've read **ART** Chapters 12-13
Sun | 04-19 | Minute Paper after Class 23. Submit before 9 AM Sunday to make the feedback.
Mon | 04-20 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) will be due at 10 AM.

## Questions and Answers (also posted [to the Project 2 Instructions](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project2/README.md#questions-and-answers))

> I'm having trouble getting the `cut` function to work properly in creating categories from a continuous variable. Any suggestions?

My general approach to cutting variables by quartile is to use [the cut2 function from the Hmisc package](https://www.rdocumentation.org/packages/Hmisc/versions/4.4-0/topics/cut2) (which rms loads automatically) or to use the tidyverse's apporoach which is [cut_interval or cut_number or cut_width](https://ggplot2.tidyverse.org/reference/cut_interval.html) (all are part of ggplot2, I think) rather than [cut from the base R software](https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/cut). You might want to look at one of those options.

The most common thing I do when using any of these tools is to build a plot or table that shows me the old continuous data broken down by levels of the new categorical variable, to be sure I didn't introduce any missing values and that every subject falls into the category I intended them to fall into.

> How might I use a Poisson or other count outcome model if I have counts, but the minimum possible value is 1, instead of 0?

Try a Poisson model on (Y - 1) rather than on your original response Y.

> Suppose I run my model with simple imputation and get result "A" and then run my model with multiple imputation and get result "NOT A". Which is the one I should report?

This is a pretty clear indication that you need multiple imputation. I would report that as my final model. It's 100% reasonable to show this impact and then settle on the multiple imputation approach if you like.

> How should I explain my data cleaning and management work?

Ideally, by explaining things (why you're doing them and what you're doing) in complete sentences before you show the code. And use subheadings, please. Bite the pieces off into small chunks and present the cleaning in multiple pieces as opposed to a wall of text.

> I have a question about using the mice package to impute missing values. Specifically, how do we end up with a complete dataset? In the case of single imputation we can use: smart_16_imp1 <- mice::complete(smart_16_mice1) but in the case of multiple imputation, we end up with a pooled model of all 20 runs of our imputations. Is there a way to use this model to complete the data and fill in the missing values? If not, then what should the final analytic data set look like at the end of section 4? 

When using multiple imputation, you will thus create not one, but multiple data sets. Your final analytic data set that you create in Section 4 (and save as a tidy R data set) should be the data set including the missing values, after you've removed any cases that you will drop because of missing outcomes, but before you do any imputation, multiple or otherwise. That should also be what you display results for in Section 5. Your actual imputation work, then, should be confined to **Section 6** of the Project portfolio.

> What's the most useful thing I can do to improve my project?

Have someone else read it, looking for grammar and syntax issues, and for things that don't make sense. Ideally, you'd have cultivated friends in the class who can read your work. Happily, all of you have in the form of our TAs, but they're probably only available to read parts of your work - not the whole thing.

## One Last Thing

Richard Iannone announced on 2020-04-08 that the `gt` package is now available on CRAN. [Great Looking Tables](https://blog.rstudio.com/2020/04/08/great-looking-tables-gt-0-2/) are now much easier to create than in the past. 

>  The name `gt` is short for “grammar of tables” and the goal of `gt` is similar to that of `ggplot2`, serving to not just to make it easy to make specific tables, but to describe a set of underlying components that can be recombined in different ways to solve different problems. If you ever need to make beautiful customized display tables, I think you’ll find `gt` is up to the task. 

[The `gt` website is here](https://gt.rstudio.com/) with lots of examples and a description of the philosophy, and links to other ways to solve table-making problems with other R packages.
