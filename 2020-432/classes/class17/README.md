# 432 Spring 2020 Class 17: 2020-03-26

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 17 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class17/432_2020_slides17.pdf) | [Class 17 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class17/432_2020_slides17.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 17 is now available!](https://cwru.zoom.us/rec/share/6ZdKPu7c1WFLa42O513weoUvQrbleaa80yAf-aUMyQ7MlaQPbw27pmaKmhQz3Ao?startTime=1585241209000). The class starts 13 minutes and 35 seconds (roughly) into the video.
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a place for you to communicate with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat. I'll also leave some follow-up there after each class as needed, on things that come up in the chat, etc.

## Announcements

1. There is a [Minute Paper after Class 17](https://bit.ly/432-2020-minute-17). Dr. Love will provide feedback if you complete this before 9 AM Sunday 2020-03-29.

2. The most important upcoming deliverable is the [Project 2 Proposal Google Form](http://bit.ly/432-2020-project2-proposal-form), which is due at **noon on Wednesday 2020-04-01**. If you haven't gotten started on identifying your research question and data, please start as soon as possible.  The full [Project 2 instructions are here](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2).

3. **Project 1 Grading**. Dr. Love will provide an update.

4. **Homework 4**: A draft ([in PDF](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/sketch_hw4.pdf) and [R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/sketch_hw4.Rmd) of the answer sketch and rubric is available. Grading will take a week.
    - We may augment the sketch and rubric next week to address some common concerns, specifically regarding alternate approaches to dealing with missingness, or the impact of small changes on the way in which multiple imputation is used.

5. [Homework 6](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw06) (Build Your Website with Blogdown) might be a little more inspiring if you look at [some examples of the sites built by fellow students at CWRU using blogdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw06/links.md). 
    - I'll do a similar thing with [Homework 5](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw05) submissions after I have more than a couple of those.

6. We'll start today's session with **Slide 70** from the [Class 16 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class16/432_2020_slides16.pdf), and then move on to Class 17 materials.

7. We talked about hanging **rootograms** last time as a means of understanding the fit of count outcome models, like Poisson or Negative Binomial regressions. If you want some more information, a key paper is Kleiber C Zeileis A "[Visualizing Count Data Regressions Using Rootograms](https://arxiv.org/pdf/1605.01311)".

8. Alison Hill gave a very interesting talk at the R Studio 2019 conference on [Making Slides for HTML with R Markdown](https://arm.rbind.io/slides/xaringan.html). There's a lot to unpack, but these are impressive tools.

9. There are some new things posted on our [COVID-19 resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md).

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class17/figures/murray_2020-03-26.png)

## Improving/Augmenting Your Visualizations

Visualizing data can be extremely difficult. Even *The Economist* has an interesting history in this regard, as Sarah Leo writes in [Mistakes, we've drawn a few](https://medium.economist.com/mistakes-weve-drawn-a-few-8cdd8a42d368?gi=79a4498d7670). 

1. If you want to arrange plots into a grid in a more nuanced way than `gridExtra::grid.arrange()` provides and you don't like `patchwork` for whatever reason, you probably should consider `cowplot`. The [introductory vignette is here](https://cran.r-project.org/web/packages/cowplot/vignettes/introduction.html), and the [`plot_grid` function vignette is here](https://cran.r-project.org/web/packages/cowplot/vignettes/plot_grid.html). The [github site for cowplot is here](https://github.com/wilkelab/cowplot).
2. If you're looking for ways to improve the themes used in your ggplots, or perhaps to use a specific font or color scheme, you might want to look over [these examples in the hrbrthemes package](https://github.com/hrbrmstr/hrbrthemes).
3. Another interesting idea is highlighting specific values / paths within a plot, and the [gghighlight vignette](https://cran.r-project.org/web/packages/gghighlight/vignettes/gghighlight.html) may be of some interest. This was presented at the R Studio Conference 2019: [more details are here](https://yutani.rbind.io/post/2018-06-03-anatomy-of-gghighlight/).
4. Tables are a kind of visualization, too, of course, and [the gt package](https://github.com/rstudio/gt) can be a big help in trying to build information-dense and attractive tables.

Of course, if you really do a good job, it's always possible you'll be rewarded [with a parade](https://twitter.com/DapperHistorian/status/1111007778469040133)!

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class17/figures/parade.png)

## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Sun | 03-29 | Minute Paper after Class 17 deadline is 9 AM. Dr. Love will write up the feedback on Sunday.
Wed | 04-01 | [Project 2 Proposal Google Form](http://bit.ly/432-2020-project2-proposal-form) due at Noon. [Project 2 instructions are here](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2).
Thu | 04-02 | Be sure you've read **ART** through Chapter 11 before Class.
Fri | 04-03 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) will be made available (it's due 2020-04-20)

