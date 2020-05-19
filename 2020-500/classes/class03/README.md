# 500 Class 03: 2020-01-30

## Today's Slides

- The slides I'll present in class today are [available in PDF](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class03/500_2020_slides03.pdf) as well as [in R Markdown](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class03/500_2020_slides03.Rmd).
- Audio recordings of our classes will be maintained in [this Google Drive folder](http://bit.ly/500-2020-audio).

## Announcements, etc.

1. The Homework 1 Answer Sketch is posted as a [Github Markdown file (code + results)](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/sketch_hw1.md), and as an [R Markdown file](https://github.com/THOMASELOVE/2020-500/blob/master/homework/hw1/sketch_hw1.Rmd).
2. I'll spend some time discussing [The dm2200 Example](https://github.com/THOMASELOVE/500-data/tree/master/dm2200) which will help you with propensity matching, in particular, and may be a somewhat less daunting starting place than the toy example.
3. We will probably spend a little time today on a few key parts of [The Toy Example (2020 version)](https://github.com/THOMASELOVE/500-data/tree/master/toy2020). We will walk through the example in a more careful way in Class 4 (and perhaps a bit of Class 5, too.)
4. Harry Persaud put together an initial draft of [The Lindner Example](https://github.com/THOMASELOVE/500-data/blob/master/lindner/README.md) which is trying to do much of what the Toy example does, but for a real data set. Please help us improve this example.
5. Steven Franconeri has an interesting post at Medium about what cognitive science tells us about how we perceive graphs. The post is "[Multiple views on how to choose a visualization](https://medium.com/multiple-views-visualization-research-explained/multiple-views-on-how-to-choose-a-visualization-b3ffc99fcddc)" and it is definitely worth your time.
    - There is a related "[Quick Reference Guide](http://experception.net/)" downloadable pdf which I recommend heartily.
    - Don't forget about the [RStudio Cheat Sheets](https://rstudio.com/resources/cheatsheets/), in particular the one for Data Visualization, and the [associated set of references for the ggplot2 package](https://ggplot2.tidyverse.org/reference/).

## Tweet of the Day (from [Frank Harrell 2020-01-24](https://twitter.com/f2harrell/status/1220702011487932417))

![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class03/figures/harrell2020_tw.PNG)

---------

## Discussion Questions regarding Rosenbaum, Chapter 3

1. Suppose you are considering a null hypothesis of no treatment effect. What does this mean, exactly? Is it easier to find strong evidence that this hypothesis is true, or that it is false? Why?
2. How did what you read in Chapter 3 clarify or change your way of thinking about the interpretation of a hypothesis test? What does Fisher's description of randomization as the "reasoned basis for inference" have to do with your thinking now?
3. Based on what you have read so far, what conclusions can you draw about the relative effectiveness of the aggressive and less-aggressive protocols in the ProCESS trial?

## What is Wrong with This Picture?

![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class03/Futier_2020_FLASH_JAMA_visual_abstract.png)

- See [Frank Harrell's Tweet 2020-01-24 and the follow-up comments](https://twitter.com/f2harrell/status/1220683246507307014).
- See the [full paper in JAMA](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class03/Futier_JAMA_2020_FLASH_RCT.pdf) (Futier et al.)
- See [DataMethods](https://discourse.datamethods.org/t/language-for-communicating-frequentist-results-about-treatment-effects/934), too.
    - A *p* value conveys essentially no information when it's large. "Large *p* means (1) at present, with our sample, we cannot bring evidence against the supposition of "no difference" and (2) get more data."
    - [Absence of evidence is not evidence of absence](https://www.bmj.com/content/311/7003/485) from *BMJ* by Douglas Altman 1995. https://doi.org/10.1136/bmj.311.7003.485
    - [ASA Statment on P-values 2016](https://amstat.tandfonline.com/doi/full/10.1080/00031305.2016.1154108#.W-sCjhBRceY)

-----------

## After today's class, you should be moderately well-equipped to:

1. Identify a good data set and start working in earnest on your [Project Proposal](https://github.com/THOMASELOVE/2020-500/tree/master/project). 
2. Identify articles using propensity scores that you want to read for your [Observational Studies in Action](https://github.com/THOMASELOVE/2020-500/tree/master/osia) assignment. Those [already claimed are posted here](https://github.com/THOMASELOVE/2020-500/tree/master/osia/claims).
3. Read Chapter 4 of Rosenbaum, in anticipation of our discussion next time.
4. Read through most of the [The dm2200 Example](https://github.com/THOMASELOVE/500-data/tree/master/dm2200), as well as most of the first 12 parts (not so much the sensitivity analysis) of [The Toy Example](https://github.com/THOMASELOVE/500-data/tree/master/toy2020), although we'll do this together, too.

## Upcoming Deadlines

Deadline | Deliverable
------------: | ----------------------------------------------------------
Today at 3 PM | [Homework 2](https://github.com/THOMASELOVE/2020-500/tree/master/homework/hw2) via Canvas
02-05 at 3 PM | [OSIA proposals](https://github.com/THOMASELOVE/2020-500/tree/master/osia) via email to Dr. Love
Class 04 (02-06) | Rosenbaum through Chapter 4
02-12 at Noon | [Initial Draft of the Project Proposal](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal) via Canvas

