# 431 Fall 2019 Class 21: 2019-11-12

## Today's Slides

- Class 21 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS21/431_class-21-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS21/431_class-21-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Upcoming Deadlines

1. There is a [Minute Paper after Class 21](http://bit.ly/431-2019-minute-21). Please complete it by 2 PM Wednesday 2019-11-13. 
    - The form is now accepting responses - sorry about the problem last week.
2. [Quiz 2](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ2) will be available to you on 2019-11-14 by 5 PM. It's due 2019-11-18 at Noon.
    - Quiz 2 is primarily about Chapters 15-28 (and 30) of the Course Notes. It also covers material from Chapters 1-14 of those Notes, as well as Chapters 1-11 of Nate Silver's *The Signal and the Noise* and all of Jeff Leek's *Elements of Data Analytic Style*.
    - Questions about adding covariates to ANOVA models, about chi-square tests for contingency tables larger than 2x2, or about Mantel-Haenszel methods, or even the Holm procedure for multiple comparisons will show up on Quiz 3 instead.
    - Chapter 30 of the Course Notes provides a pretty thorough review, but there are things on the Quiz not included there, too.
    - [Links for all Quiz 2 materials will appear here](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ2).

## Course Notes

- Students found some typos in Section 9.5, Section 17.8.4 and Section 28.3 which [I've recently fixed](https://thomaselove.github.io/2019-431-book/). Thanks very much!

## Project Portfolio Examples

- For Study A (the Course Survey), [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/EXAMPLE/README.md) to review the Example Portfolio.
- For Study B (your data) [this page links you to everything you need](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_B/EXAMPLE/README.md) to review the Example Portfolio.
    - In Task 5 (due 2019-12-02) what you are sending is your post-cleaning, post-sampling, final, final, final analytic data set. If you start with more than 2500 rows, or more than the final number of columns you actually need, you should prune and sample first. You can send the full one pre-sampling, too, but the final one is key.

## Homework H Answer Sketch

- is [now available](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/H/post-deadline.md).

### Having trouble using the `here` package?

Have you tried running `here()` in the R Console? What does it show you? It answers the question: "What does `here` think the top-level of the current project is?" That's a very important thing to know.

So, for homework H, I would have a folder called *HomeworkH* and that's where I would put my R project, so that when I run `here()` in that project the top level directory it points to is *HomeworkH*. Under *HomeworkH*, I keep subfolders called *data* and *R*. So I source in an R script with something like ...

```
source(here("R", "nameofscript.R"))
```

or read in a data set with something like. ... 
```
read_csv(here("data", "nameofdata.csv"))
```

### When you specify a confidence level to R, what does it change?

- Does it change the lower and upper bound of the confidence interval?
- Does it change the number R provides as a *p* value? Should it?

### A Little Demonstration: Changing the Confidence Level and working with `here()`

``` r
library(here); library(magrittr); library(tidyverse)
```

``` r
here()
```

    [1] "C:/Users/Thomas/Dropbox/2019-431/431_class_21"

``` r
dm431 <- readRDS(here("data", "dm431.Rds"))
```

``` r
dm431 %$% t.test(sbp ~ sex, conf.level = 0.90)
```

``` 

    Welch Two Sample t-test

data:  sbp by sex
t = -0.13838, df = 419.27, p-value = 0.89
alternative hypothesis: true difference in means is not equal to 0
90 percent confidence interval:
 -3.108582  2.627120
sample estimates:
mean in group F mean in group M 
       131.1673        131.4080 
```

``` r
dm431 %$% t.test(sbp ~ sex, conf.level = 0.95)
```

``` 

    Welch Two Sample t-test

data:  sbp by sex
t = -0.13838, df = 419.27, p-value = 0.89
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 -3.660307  3.178845
sample estimates:
mean in group F mean in group M 
       131.1673        131.4080 
```

--------------

## A few more things

1. The [Consortium for the Advancement of Undergraduate Statistics Education](https://www.causeweb.org/cause/) holds a monthly contest.  Each month a cartoon, drawn by British cartoonist John Landers, is posted for you to suggest statistical captions. The next cartoon and the entry rules for the contest ending November 30 are at https://www.causeweb.org/cause/caption-contest/november/2019/submissions. 
2. There's an update to [the `ggrepel` package](https://github.com/slowkow/ggrepel) which allows you to [highlight text on non-overlapping plot labels](https://twitter.com/benmarwick/status/1193622804693803010). Very slick.
3. The Holm-Bonferroni method for dealing with multiple comparisons is worth some of your time. The [essential ideas are described at Wikipedia](https://en.wikipedia.org/wiki/Holm%E2%80%93Bonferroni_method), and I like it because it's uniformly more powerful than Bonferroni in all settings. In the future, I'll focus on Holm rather than Bonferroni as a solution. Understand that [`pairwise.t.test()` does Holm tests, as do all of the `p.adjust` methodologies](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/p.adjust.html), in R.
4. David Robinson gave a talk on "Ten Tidyverse Tricks" at an R Meetup on 2019-11-09 in Washington DC. Details were enthusiastically [tweeted by Jon Harmon](https://twitter.com/JonTheGeek/status/1193203057330466818) and [by Emily Robinson](https://twitter.com/robinson_es/status/1193210110132310022). Well worth some of your time to take a look.
    - David's [Tidy Tuesday screencast](https://www.youtube.com/channel/UCeiiqmVK07qhY-wvg3IZiZQ) videos provide terrific insight into how a data scientist thinks through new data, and explores/visualizes it in R.
    - The [tidytuesdayR package](https://github.com/thebioengineer/tidytuesdayR) helps make it easy to extract the TidyTuesday data sets.

## One Last Thing

Karl Broman presents [The Top Ten Worst Graphs in the Scientific Literature](https://www.biostat.wisc.edu/~kbroman/topten_worstgraphs/) as published in the period 1994-2012.

## Also...

The play I am in, *Noises Off*, gives its final performances on November 15 and 16. It's suitable for **adult** audiences. For more details or to buy tickets, visit [this link](https://app.arts-people.com/index.php?ticketing=hudpl) or my [theater page](https://github.com/THOMASELOVE/theater). The show is going well. If you're interested, please come!
