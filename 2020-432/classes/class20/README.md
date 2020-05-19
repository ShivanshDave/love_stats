# 432 Spring 2020 Class 20: 2020-04-07

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 20 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class20/432_2020_slides20.pdf) | [Class 20 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class20/432_2020_slides20.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 20 is available here](https://cwru.zoom.us/rec/share/5OhSNonRqVJJW6uT0xHdc_Q7ErvcX6a8hnRK_aJbxEvM5lkijGGflD6KWbngcd21?startTime=1586278846000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a white board for communication with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.
- The [COVID-19 Resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) will remain available through April. I'll post new things as I can, and discuss them on Thursdays.

## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Sun | 04-12 | Minute Paper after Class 21. Submit before 9 AM Sunday to make the feedback.
Tue | 04-14 | Be sure you've read **ART** Chapters 12-13
Sun | 04-19 | Minute Paper after Class 23. Submit before 9 AM Sunday to make the feedback.
Mon | 04-20 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) will be due at 10 AM.

## Recent Q & A (Questions edited a bit.)

Note: We're storing all questions and answers of relevance to Project 2 [at the bottom of the Project 2 instructions, too](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project2/README.md#questions-and-answers).

> What's the difference between a count outcome and a quantitative outcome?

- The possible values. A quantitative outcome is any quantity - it includes ratios, percentages, fractions, decimal places, negative numbers, anything that can be expressed on a continuous scale in addition to counts. Counts are a subset of quantities - they start at 0 and increase by integers, so those are the only possible values. 
- A Poisson distribution, for instance, would be an option to use in modeling a count. A Normal distribution is what we typically use for other types of quantitative outcomes.

> Am I right in thinking that you don't want us to impute an outcome in Project 2?

That's correct. I do not. If you have a key predictor that your research question is focused on (for instance, did receipt of this treatment affect the outcome, adjusting for these covariates), I am reluctant to have you impute that "treatment" either. I'm happiest when you're only imputing variables you are adjusting for as covariates in your models.

> I am pondering how to move forward with missingness in my data. The codebook suggests that some subgroups (they specifically highlighted black males) tend to not respond to questions regarding high risk behaviors in similar surveys. I am looking at illicit drug use in my model, and there is missingness in the variables I am using. In the Project 2 instructions, you write: If missingness is not random, we suggest you reduce the scope of your data set to eliminate either the observations that are not missing at random, or to eliminate the variables containing those missing values. Can you provide some insight on how to move forward with the missingness here? 

- "Missing at random" isn't a great name, as we discussed. It doesn't mean "missing arbitrarily" but rather it means that the missingness can be fully accounted for by variables where complete information is available. 
- "Missing not at random" means that the missingness depends on things we DON'T have in our data set.
- If black males are believed to be less likely to respond, then your imputation models should include both race and sex. If each of those variables in is your data, then imputation may be reasonable. If they're not, then you have a real problem, and would need to, for instance, select a different set of variables to study. That's the kind of thing you want to talk to us about at `431-help`. 

> Can you help me with (some particular situation) related to my project?

Sure, but can we ask you to make it as easy as possible on us. What we want to be able to do is look at R output in addition to R code. We need to be able to recreate exactly (and I mean exactly) what you're looking at. With imputation involved, this becomes very challenging. What we want to see is what the implications of various decisions you have already made are, and what the implications would be of various suggestions for going forward in order to help you make sense of your data. 

1. The best solution is to settle on a version of your data set that you're happy with, then actively **save it as an Rds file within your R Markdown** so we know where in your file you created what you send to us, then send us the R Markdown, HTML result and R data set files, along with your questions. 
2. The second best solution is to send us the **raw `.csv` files** you are importing, using the names that are used in your R Markdown file to import them, along with your R Markdown and HTML files and questions.
3. If you cannot send us the raw data or the tidied data, helping you will be much more challenging, but we'd still like to try. At the least, we need an R Markdown and HTML file along with your questions.

## Announcements

1. If you haven't already done so, please verify that you can access the Google Form for [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) and the shared drive containing my video recording, the four data sets, and the PDF file containing the instructions and items. 
    - Look at the email stream with the subject heading "432 Quiz 2 is now available to you" which I sent on 2020-04-03, and be sure to read the second email I sent at 11 AM on 2020-04-03 to provide the Google Drive direct link. I sent it again today, in the same link.
    - Please let us know at `431-help` if you have any questions or are having any problems accessing the materials. 

2. The **survminer** package is where you can find the **ggsurvplot** approach we'll take today. For more customization of plots like the Kaplan-Meier curves we'll build today, visit https://rpkgs.datanovia.com/survminer/ or https://github.com/kassambara/survminer/. 
    - For instance, they provide a [PDF cheat sheet](https://rpkgs.datanovia.com/survminer/survminer_cheatsheet.pdf) which was pretty helpful to me.
    - In today's slides, I'll make reference to [this PDF guide by David Diez on Survival Analysis in R from OpenIntro](https://www.openintro.org/book/surv_in_r/), which I also recommend, and which provides the `OISurv` package.
    - Materials on time-to-event outcomes are found in Chapters 22 and 23 of our [Course Notes](https://thomaselove.github.io/2020-432-book/exploring-time-to-event-survival-data.html).
    
3. Happiness is a challenging thing to find these days. I enjoyed the [2019 World Happiness Report](https://en.wikipedia.org/wiki/World_Happiness_Report) a year ago, and kept meaning to discuss it with you. [The data available in the full report](https://worldhappiness.report/ed/2019/) or even just on [the Wikipedia page](https://en.wikipedia.org/wiki/World_Happiness_Report) might be a nice source for visualizations and modeling in Homework 5, should you decide to pursue that.

## One Last Thing

I had some fun taking the [Statistical "Which Character" Personality Quiz](https://openpsychometrics.org/tests/characters/) which is part of an [Open-Source Psychometrics Project](https://openpsychometrics.org/). It attempts to compare your self-description on several traits to a selection of just over 500 fictional characters and matches you to the "most similar" one. One thing I like about it is that it is [well-documented](https://openpsychometrics.org/tests/characters/development/). 

- Using their recommended list of 28 items, I matched best (according to a Pearson correlation) with [Sam Seaborn](https://en.wikipedia.org/wiki/Sam_Seaborn) from *The West Wing*, which is probably more an indication of how I feel about myself than anything else. It's a better fit in some ways than others. Still, I'll take it.
- When they say I have an 86% match with Sam, this essentially means that they took my Pearson correlation (on a scale from -1 to +1) and added 1, and then multiplied by 50. So my Pearson correlation with Sam was actually *r = +0.72*, so our R-square is 52%.

