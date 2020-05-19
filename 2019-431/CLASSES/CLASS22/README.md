# 431 Fall 2019 Class 22: 2019-11-14

## Today's Slides

- Class 22 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS22/431_class-22-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS22/431_class-22-slides_2019.Rmd) above. 
    - **Note**: These slides are actually a double batch, planned for use in both Classes 22 **and** 23. 
    - **Post-Class** In today's class, we got through slide 36. We'll start there again in Class 23, although it will be a different slide number. I've also corrected the problems we found in the screenshots, plus the labels on the tables in slides 8 and 9.
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.


## Project Portfolio Examples

- For Study A (the Course Survey), [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/EXAMPLE/README.md) to review the Example Portfolio.
    - **NEW** I revised the data02, data03, data04 and data05 data sets, so make sure you grab the new ones. For most of you, this won't matter, but some of you will have an easier time this way. What I did was mostly remove apostrophes from some items.
- For Study B (your data) [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_B/EXAMPLE/README.md) to review the Example Portfolio.

## Quiz 2

- [Quiz 2](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ2) is available to you now.
- It's due 2019-11-18 at Noon. 
- [Links for all Quiz 2 materials are here](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ2).

## General Announcements

1. Dr. Love expects to be offline most of the time from about 1 PM Friday through to about 5 PM Sunday. 431-help will be your source for any questions. If something comes up after Friday 1 PM that I must address personally, I will try to resolve it sooner, but cannot guarantee that I will get to it before Sunday evening. 
2. Homework H grades and rubric [were posted this morning](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/H/post-deadline.md).
3. Comments on the [Minute Paper after Class 21 are now available](http://bit.ly/431-2019-minute-21-response).

## Taking Other Courses With Me

In addition to 431, I teach two other semester-long courses, called **PQHS 432** and **PQHS 500**. I intend to teach both 432 and 500 in Spring 2020 and again in Spring 2021. Here's my advice, for what it's worth ...

- **432** is the continuation of this course (widely regarded as the "better" half.) I think **everyone** in this class should be planning to take 432 this Spring (i.e. Spring 2020), **unless** ...
    - you are not benefitting from this course and don't need to take 432 to finish your program at CWRU, **or**
    - you have an unshakable conflict in Spring 2020 (especially if you plan to instead take 432 in Spring 2021.)
- **500** is a project-based and more advanced course covering specific topics in the design and analysis of observational studies. 
    - I think everyone in this class who is interested in taking 500 should do so. The course is mostly about using propensity scores well to help design (and analyze) data from observational studies where we want to estimate a causal effect.
    - I especially think MS and PhD students (in any department) interested in applications of health research in real world situations should take it, as well as people looking for jobs in fields related to health care analytics.
    - Most people would benefit from taking 500 in Spring 2021 rather than Spring 2020 if that option is available to you, since it's usually better to complete 432 before taking 500, for at least two reasons. 
    - However, if Spring 2020 is your best opportunity to take 500, for whatever reason, then I will certainly permit you to do so, but I'll want to talk to you about it a little (ideally in December.)

## Some Coding Tips (for the projects, mostly)

1. Don't hide code by placing it in the setup chunk with include = FALSE. For the project, it's appropriate to use a setup chunk to include something like:

```
knitr::opts_chunk$set(comment=NA)
options(width = 60)
```

with include = FALSE in the chunk command, but that's it. All of your package loading should be in a separate chunk from this setup.

2. Every time you create a new chunk of R code, or start a new paragraph of text, or create a new table of contents element with # or ## or ###, you should precede this with a blank line, and follow it with a blank line.
3. Before you knit your R Markdown code, run a spell check on it (by hitting F7 in RStudio).
4. Before you knit your R Markdown code, make sure that all of your chunks with names have different names, and that the names have no spaces in them.
5. Use the key tidyverse verbs, like `filter()` and `select()` and so forth in your data management work whenever you can, rather than non-tidyverse ways of accomplishing similar things.

## One Last Thing

To my amazement, there's been an error in the `dm431` data set for a long time (since July, I think.) We'll fix it in class today. I won't go back and fix it in previous classes (since it doesn't affect what we did), but we'll get it right going forward.


