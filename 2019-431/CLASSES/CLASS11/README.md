# 431 Fall 2019 Class 11: 2019-10-01

## Today's Slides

- Class 11 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS11/431_class-11-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS11/431_class-11-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.
- A new RStudio Cloud project called `PartB_Classwork` contains the vital packages, etc. for this part of the Course. 
    - To mirror this on your computer if you're not using RStudio Cloud, follow [the Package instructions page](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/PACKAGES.md).
    - The new packages not originally installed at the start of the semester that are now listed include `exact2x2`, `ggforce`, `here`, `infer`, `PropCIs` and `patchwork`, and perhaps some others, too.

## Upcoming Deliverables

- There is a [Minute Paper after Class 11](http://bit.ly/431-2019-minute-11) due at 2 PM Wednesday 2019-10-02.
- The [Schedule for Project Presentations](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/SCHEDULE) is now posted.
    - Please review your scheduled time, which you'll confirm in the Minute Paper.
- [Homework F](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/F) is due 2019-10-04 at 2 PM.
    - The [Homework E Answer Sketch](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/E/post-deadline.md) is now available.
- By today, you should have read all of Jeff Leek's *Elements of Data Analytic Style*.
- On 2019-10-08, Project Task 2 (Proposal for Study A **and** Proposal for Study B) are due at 5 PM.
    - This is the most extensive set of tasks so far assigned in the course. It requires you to submit (as part of your small group of 6-7 people) your Study A proposal, **and** (alone or with your partner) your Study B proposal. 
    - Please follow the instructions: [here they are for Part A](https://thomaselove.github.io/2019-431-project/task2a.html) and [here's Part B](https://thomaselove.github.io/2019-431-project/task2b.html).
- Also for 2019-10-08, finish Chapters 4 (Weather) and 5 (Earthquakes) of *The Signal and the Noise*.
- You will receive Quiz 1 by 5 PM on 2019-10-10. It's due at noon on 2019-10-14.

## A Few Loose Ends

1. You may be interested in learning [some basic lab skills for research computing from Software Carpentry](https://software-carpentry.org/lessons/). They have some nice lessons on several related topics to this course.

2. Here are six potential useful links related to the Bland-Altman plot. Enjoy!
    - https://en.wikipedia.org/wiki/Bland%E2%80%93Altman_plot
    - https://rdrr.io/cran/blandr/
    - https://labrtorian.com/tag/bland-altman/
    - http://derekogle.com/fishR/2017-04-20-Modified_BlandAltmanPlot
    - https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4470095/
    - https://www.r-bloggers.com/bland-altmantukey-mean-difference-plots-using-ggplot2/

3. When you type `library(tidyverse)` the core set of tidyverse packages are then active on your machine (so don't load them again).
    - The core packages are `ggplot2`, `dplyr`, `tidyr`, `readr`, `purrr`, `tibble`, `stringr`, and `forcats`. 
    - But when you install the `tidyverse` as a package, you also get the following non-core packages installed, but these must be loaded separately (using `library(broom)`, for instance,) in addition to loading the tidyverse with `library(tidyverse)`.
        - The non-core packages include: `readxl`, `haven`, `jsonlite`, `xml2`, `httr`, `rvest`, `DVI`, `lubridate`, `hms`, `blob`, `magrittr`, `glue`, `recipes`, `rsample` and `broom`.
    - Learn more about [the tidyverse packages here](https://www.tidyverse.org/packages/).

4. We've talked a little about peer review and scientific publishing in the past. I won't add more today, except to suggest that Stephen Buranyi has an interesting article called [Is the staggeringly profitable business of scientific publishing bad for science?](https://www.theguardian.com/science/2017/jun/27/profitable-business-scientific-publishing-bad-for-science) from 2017-06-27 in *The Guardian* that I was recently reminded of.

## In the News

1. [This thread by @AlbertoCairo](https://twitter.com/AlbertoCairo/status/1178298283036463104) is great, and also serves as a nice ad for his book "How Charts Lie". We'll walk through it in class, but it's basically a response to [this 2019-09-28 tweet by Lara Trump](https://twitter.com/LaraLeaTrump/status/1178030815671980032):

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS11/images/lara_trump_tweet.PNG)

-------------

Alberto shows the following *better* version of that map from [the New York Times](https://www.nytimes.com/interactive/2016/11/01/upshot/many-ways-to-map-election-results.html) ...

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS11/images/map_better.jpg)

-------------

My favorite map of this form for the 2016 election might be [this one from XKCD](https://xkcd.com/1939/)

![](https://imgs.xkcd.com/comics/2016_election_map.png)

--------------

2. I learned a fair amount about differential nonresponse bias, outliers and what to expect when a big news story happens from [How a Big Enough News Story - Like Impeachment - Could Warp the Polls](https://fivethirtyeight.com/features/how-a-big-enough-news-story-like-impeachment-could-warp-the-polls/) by Mark Blumenthal at FiveThirtyEight, 2019-09-30.
    - If this interests you, I'd also recommend Nate Silver on [How to Handle an Outlier Poll](https://fivethirtyeight.com/features/how-to-handle-an-outlier-poll/) from 2019-09-03 also at FiveThirtyEight.
    - If even that interests you, then on the [FiveThirtyEight Politics Podcast](https://fivethirtyeight.com/features/politics-podcast-impeachment-is-becoming-more-popular) for 2019-09-30, there was a detailed discussion of how much public opinion has changed since Speaker Pelosi's announcement of an official impeachment inquiry.

## One Last Thing

https://github.com/gadenbuie/tidyexplain is a great resource (complete with animations!) for learning how to join data sets in R.
  
-----------------

## 2 PM Small Group Activity

You will have some time at the end of today's class, and again at the end of Thursday's class, to meet in your [project small groups](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/small_groups.md). We want you to use that time to work on your [Study Proposal for Project Study A](https://thomaselove.github.io/2019-431-project/task2a.html), which must be completed by 5 PM next Tuesday.

A reminder that in the Study A Proposal, your group will need to:

1. develop and propose 2-3 “research questions” for Study A (The Class Survey).
2. develop and propose 6-10 “homemade” survey items for Study A that relate to your research questions.
3. identify and propose a “scale” of items for Study A (The Class Survey).

If you need ideas, the [old surveys from 2014-2018 are here](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT#special-links). In the meantime, let us know how we can help, beyond what is already posted in [the instructions](https://thomaselove.github.io/2019-431-project/task2a.html). 

Don't forget that the Study B proposal is also due on the same day at the same time. Next Tuesday 2019-10-08 at 5 PM.


