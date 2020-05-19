# 432 Spring 2020 Class 05: 2020-01-28

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Week 03 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class05/432_2020_week03.pdf) | [Week 03 .Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class05/432_2020_week03.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Announcements

1. The [Class 03](https://github.com/THOMASELOVE/2020-432/tree/master/classes/class03) and [Class 04](https://github.com/THOMASELOVE/2020-432/tree/master/classes/class04) Slides have been edited to reflect what we actually discussed each day, and reposted accordingly.
    - In slide 39 of Class 04, there was an error, now corrected, in the estimation of Sally's BMI at the top of the slide.
2. Thank you for completing the [Minute Paper after Class 4](http://bit.ly/432-2020-minute-04). By now, I hope you've had the chance to [review the feedback I posted Friday](http://bit.ly/432-2020-minute-04-feedback). Our next Minute Paper will be after Class 6.
3. When sending us a request for help at **431-help** it's extremely helpful for you to send your entire R Markdown file, in addition to pointing out whatever specific issue is concerning you. This will help us respond faster and more accurately.
4. If you're having trouble figuring out how to do something in R, consider looking at [the r-basics document](https://github.com/THOMASELOVE/2020-432/tree/master/r-basics). It's not perfect, but it does cover a lot of common issues. Section 8.3, for instance, shows a method for creating a multi-categorical factor from a quantitative variable.
5. **On jittering in an interaction plot**. A student pointed out to me that the jittering in one of our plots was a bit confusing. [Here's a quick example displaying the problem and a possible solution](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class05/quick_example.md).
6. **[Course Notes](https://thomaselove.github.io/2020-432-book/) Updated**. I made some meaningful progress revising and updating [the 2020 Course Notes](https://thomaselove.github.io/2020-432-book/). 
    - You'll find some small revisions before Chapter 3, substantial revisions to Chapter 3, and new Chapters 4-9, which should provide ample material to supplement the slides through this week.
7. I've added some new packages, including `caret` and `tidymodels` to the [software packages list](https://github.com/THOMASELOVE/2020-432/blob/master/software.md). Please get up to date for Homework 2.

## Homework 1 Hint

We sent this yesterday via email. Suppose you use a `filter()` to (in Question 1) reduce the data set to just the two practices we want to study. How, then, might you eliminate the now-unused levels of the factor for purposes of, say, building a table? We recommend [the fct_drop() function in the forcats package](https://forcats.tidyverse.org/reference/fct_drop.html).

Someone was still confused, so I wrote this:

Suppose you have...
```
hbp432_1 <- hbp432 %>%
  filter(practice == "A" | practice == "C")
```

and then try
```
hbp432_1 %>% tabyl(practice)
```

You'll get 
```
practice   n   percent
       A 116 0.5742574
       B   0 0.0000000
       C  86 0.4257426
       D   0 0.0000000
```

But if instead you try ...

```
hbp432_1 <- hbp432 %>%
  filter(practice == "A" | practice == "C") %>%
  mutate(practice = fct_drop(practice))

hbp432_1 %>% tabyl(practice)
```

you get
```
practice   n   percent
        A 116 0.5742574
        C  86 0.4257426
```


## Data for [Project 1](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1)

1. **We can help you decide if the data you want to use will work.** You really want to have your data decided upon and in R by 2020-02-05. If you have data but are not sure if it will work from reading the Project 1 proposal instructions, then please email us at **431-help** with any questions. The more specific the question, and the more information you provide, the better an answer we'll give.
    - In the Class 06 README, I've written a little bit about [what I mean by having your data in hand](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class06/README.md#what-does-it-mean-to-have-your-data-for-project-1-in-hand) and we'll discuss those details in class Thursday.
2. **No multi-level data in Project 1**. As in 431, we don't want you working with multi-level data in 432 Project 1. An example of multi-level data (for which a multi-level model would be necessary) would be a setting where you study measures on individual patients as well as measures on health systems in which the individual patients are grouped. Hierarchical or multi-level models are extensions of the linear and generalized linear models we want you to use in Project 1. So, avoid nested data, where data for participants are organized at more than one level, please.
3. **Google Dataset Search** If you're looking to find a data set for Project 1, [Google Dataset Search](https://datasetsearch.research.google.com/) just [came out of beta](https://blog.google/products/search/discovering-millions-datasets-web/).
4. **Data from Wikipedia Tables** There's a new R package called `wikitablr` which has tools to help you [simply webscrape tables from Wikipedia](https://github.com/jkeast/wikitablr), and clean them up. It looks like it could be useful.

## Next Few Deliverables (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
---------: | -----------------------------------------------------------------------
Today | [Homework 1](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw01) due at 5 PM.
2020-01-31 | [Minute Paper after Class 06](http://bit.ly/432-2020-minute-06) due at 2 PM.
2020-02-04 | [Homework 2](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw02) due at 5 PM.
2020-02-05 | You should have your data for [Project 1](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) in hand.
2020-02-06 | Read *The Art of Statistics* Chapter 7 (Estimates and Intervals)
2020-02-11 | [Homework 3](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw03) due at 5 PM. (Note that HW 3 was revised 2020-01-27)
2020-02-13 | Read *The Art of Statistics* Chapter 8 (Probability)
2020-02-14 | [Project 1 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) due at 2 PM.

## One Last Thing

You might be interested in [Guessing Names Based on What They Start With](https://flowingdata.com/2020/01/21/name-guess/) from Nathan Yau at flowingdata.com (2020-01-21).

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class05/figures/flowingdata_nameguessing.png)



