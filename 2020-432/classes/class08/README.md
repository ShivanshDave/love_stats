# 432 Spring 2020 Class 08: 2020-02-11

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Week 4 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class08/432_2020_week04.pdf) | [Week 4 .Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class08/432_2020_week04.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Announcements

1. Your [Project 1 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) is due Friday 2020-02-14 at 2 PM.
    - It may (or may not) be helpful to you to look at my [old Project 1 demonstration](https://github.com/THOMASELOVE/2020-432/tree/master/projects/2019-project-1-demo) since your rules are a bit different, and the demo hasn't been updated for 2020. 
2. I moved Homework 3 to be due next Tuesday 2020-02-18 at 5 PM, instead of today, and I've now fixed that on Canvas. You should have everything you need to complete that homework after today's class.
    - Homework 2's [Answer Sketch and Grading Rubric](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw02) and also the [Homework 2 Grades](http://bit.ly/432-2020-grades) are now posted.
3. I'm updating the [Course Notes](https://thomaselove.github.io/2020-432-book/). So far,
    - I've added a new Chapter 8, and moved back the old chapters on logistic regression and called them Chapters 9 and 10.
    - I've added a new Chapter 11, focused on some prostate cancer data and cross-validation methods, so that's directly relevant today. I also threw in a little bit of robust linear modeling.
    - I've added a new Chapter 12, which uses the best subsets approach we used in Class 07.
    - I've added new Chapters 13 and 14, which cover material on incorporating non-linearity we'll discuss in Classes 09 and 10.
    - I've also posted a draft of Chapter 15, about ridge regression and the lasso, but I may drop that later or change it substantially.
4. I've posted [slides for Classes 9 and 10](https://github.com/THOMASELOVE/2020-432/tree/master/classes), if you want to see where we're going next in class.
5. No Minute Paper today. Sorry.

## What is Wrong with This Picture?

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class08/Futier_2020_FLASH_JAMA_visual_abstract.png)

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class08/Futier_2020_conclusions.PNG)

- See [Frank Harrell's Tweet 2020-01-24 and the follow-up comments](https://twitter.com/f2harrell/status/1220683246507307014).
- See [DataMethods](https://discourse.datamethods.org/t/language-for-communicating-frequentist-results-about-treatment-effects/934), too.
    - A *p* value conveys essentially no information when it's large. "Large *p* means (1) at present, with our sample, we cannot bring evidence against the supposition of "no difference" and (2) get more data."
    - [Absence of evidence is not evidence of absence](https://www.bmj.com/content/311/7003/485) from *BMJ* by Douglas Altman 1995. https://doi.org/10.1136/bmj.311.7003.485
    - [ASA Statment on P-values 2016](https://amstat.tandfonline.com/doi/full/10.1080/00031305.2016.1154108#.W-sCjhBRceY)

## Next Few Deliverables (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
---------: | -----------------------------------------------------------------------
2020-02-13 | Read *The Art of Statistics* Chapter 8 (Probability)
2020-02-14 | [Project 1 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) due at 2 PM.
2020-02-18 | [Homework 3](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw03) due at 5 PM.
