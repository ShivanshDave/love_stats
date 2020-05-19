# 431 Fall 2019 Class 07: 2019-09-17

## Today's Slides

- Class 7 slides are posted in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS07/431_class-07-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS07/431_class-07-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Dr. Love's Office

is actually **Wood WG-82 J** on the ground floor of the Wood building, and not WG-82 L. I need to fix this everywhere.

## Work on your Horizon

1. There is a [Minute Paper after Class 07](http://bit.ly/431-2019-minute-07). Please complete it by 2 PM Wednesday 2019-09-18.
2. [Homework D](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/D) is due Friday 2019-09-20 at 2 PM.
    - A generic homework template [is now available](https://github.com/THOMASELOVE/2019-431-data/blob/master/YOURNAME-HWtemplate.Rmd).
    - I've posted a project assignment on RStudio Cloud for Homework D, which includes the data set.
    - I revised [Homework D's instructions](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/D) on Saturday evening to add a few modest **hints**. Make sure you see them.
    - Beginning with Homework D, we will exact a stern penalty if you fail to get both an R Markdown and HTML (preferred) or Word/PDF document submitted to Canvas on time. 
        - We will continue to allow a one-hour grace period without penalty on Homeworks. 
        - Should you fail to get things in by four hours after the deadline, we will not accept the Homework without the clearance of Professor Love.
    - Homeworks [E](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/E) and [F](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/F) are also posted, if you want to get ahead of the game a little bit. 
    - I've also posted a project for Homework E on RStudio Cloud, but I won't do one for Homework F, because you don't have to do any R coding in that Homework.
3. Please come to class on 2019-09-24 knowing if you're going to have a partner for your course project, so you can join a small group with that partner if necessary. 
    - Your partner (if you choose to have one) works with you on Study A *and* Study B, and you build and present your portfolio jointly.
4. You'll also need to read Chapters 2 (Political Forecasting) and 3 (Baseball Forecasting) of Silver's *The Signal and the Noise* by 2019-09-24.
    - We won't discuss the Introduction and Chapter 1 today, because you'll be writing an essay about them for Homework D. 
    - Instead, we'll look at [this project on the Third Democratic Debate from Aaron Bycoffe, Sarah Frostenson and Julia Wolfe at FiveThirtyEight](https://projects.fivethirtyeight.com/democratic-debate-september-poll/).

## NEW Chapters posted in Course Notes

The [Course Notes](https://thomaselove.github.io/2019-431-book/) have substantial new material posted since we last met, including new Chapters 8-14, which complete Part A of the course, as well as some [early chapters from Part B](https://thomaselove.github.io/2019-431-book/introduction-to-part-b.html). 

- There are some minor revisions to [Chapter 2](https://thomaselove.github.io/2019-431-book/Rsetup.html) (the R setup).
- [Chapter 8](https://thomaselove.github.io/2019-431-book/assessing-normality.html) provides some tools to help decide whether a data set can be fit well with a Normal distribution.
- [Chapter 9](https://thomaselove.github.io/2019-431-book/using-transformations-to-normalize-distributions.html) demonstrates the use of Tukey's ladder of power transformations on skewed data.
- [Chapter 10](https://thomaselove.github.io/2019-431-book/summarizing-data-within-subgroups.html) discusses summarizing data across subgroups, both numerically and graphically.
- [Chapter 11](https://thomaselove.github.io/2019-431-book/straight-line-models-and-correlation.html) on fitting straight line models and measuring correlation between quantitative variables.
- [Chapter 12](https://thomaselove.github.io/2019-431-book/studying-crab-claws-crabs.html) studies crabs and their claws in assessing transformations, adjustment and regression models.
- [Chapter 13](https://thomaselove.github.io/2019-431-book/WCGS-Study.html) mixes review and new materials using the Western Collaborative Group Study.
- [Chapter 14](https://thomaselove.github.io/2019-431-book/part-a-a-few-of-the-key-points.html) summarizes some key lessons available in Part A of the Course Notes.

## We have a new Teaching Assistant!

As of today, Ben Booker has joined the group, and we've added [some additional office hours on Friday mornings](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md), too. Contact Ben via 431-help, just as you do the other TAs, and learn [more about him through the Syllabus](https://thomaselove.github.io/2019-431-syllabus/teaching-assistants.html#benjamin-ben-booker-bs), if you're so inclined.

## Interested in Learning More about R Markdown and Medicine?

Check out https://rmd4medicine.netlify.com/, which is the website for Dr. Alison Hill's four hour workshop on the subject that she's given (most recently) at the R/Medicine Conference on 2019-09-12. You can review her slides, and some of the other materials. 

Incidentally, if you want to learn more about R conferences and meetings, [try this listing of events](https://jumpingrivers.github.io/meetingsR/events.html).

## Composing `ggplot2` Plots

In the Course Notes and in our Slides, I will use (at least) three different approaches to arranging multiple graphical objects over this semester.

1. `grid.arrange()` from the `gridExtra` package: see [this vignette](https://cran.r-project.org/web/packages/gridExtra/vignettes/arrangeGrob.html), for more. This is the approach I used more or less exclusively until mid-2018, and I still use it a bit.
2. `plot_grid()` from the `cowplot` package: see the [Introduction to cowplot](https://cran.r-project.org/web/packages/cowplot/vignettes/introduction.html) from Claus O. Wilke, which is extensively used in Claus' [Fundamentals of Data Visualization](https://serialmentor.com/dataviz/) primer. This is one of the approaches I've started using more frequently now.
3. the `patchwork` package, and you can [read about it here](https://github.com/thomasp85/patchwork). `patchwork` isn't on CRAN, so you need to install it from Github. [Follow the instructions](https://github.com/thomasp85/patchwork#installation). This is rapidly becoming my favorite, but it has a rather limited scope as compared to the others.

# One Last Thing

Wondered about R's Release Names? Visit [Lucy D'Agostino McGowan's post here](https://livefreeordichotomize.com/2017/09/28/r-release-names/) and wonder no more.

- R 3.6.0 is named "[Planting of a Tree](https://www.gocomics.com/peanuts/1963/03/03)" from *Peanuts* 1963-03-03.
- R 3.6.1 is named "[Action of the Toes](https://www.gocomics.com/peanuts/1971/03/22)" from *Peanuts* 1971-03-22.
