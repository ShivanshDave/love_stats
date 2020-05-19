# 432 Spring 2020 Class 22: 2020-04-14

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 22 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/432_2020_slides22.pdf) | [Class 22 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/432_2020_slides22.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 22 is available here](https://cwru.zoom.us/rec/share/9O1eJaHr6iBOUrPTuHmDYoccO9_iaaa81ykY_Ppeyhn0wbBWwOSYoijpIe208OSu?startTime=1586882815000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a white board for communication with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.
- The [COVID-19 Resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) will remain available through May, although I expect to stop adding to it May 1.
- [Things I Won't Get To This Semester](https://github.com/THOMASELOVE/2020-432/blob/master/not_this_semester.md)

## Announcements

1. Feedback on the Minute Paper after Class 21 is available at https://bit.ly/432-2020-minute-21-feedback.
2. By now, you should have read through Chapter 13 of Speigelhalter's *The Art of Statistics*
3. Joseph Hnath was good enough to pass along links to several of the [YouTube videos posted by 3Blue1Brown](https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw) which he has enjoyed, including [this one about Bayes' Theorem](https://youtu.be/HZGCoVF3YvM), [this one about the binomial distribution and Amazon reviews](https://youtu.be/8idr1WZ1A7Q) and [this one about probability density functions and continuous vs. discrete contexts](https://youtu.be/ZA4JkHKZM50). I hope they are of interest to you.
4. A [major new release of the rms package](https://twitter.com/f2harrell/status/1249024837621878792?s=11) is coming soon, and of particular interest to me is the ability to use Bayesian approaches to run binary and ordinal (proportional odds) logistic regression models, [as illustrated here](http://hbiostat.org/R/rms/blrm.html). Frank Harrell has [a couple of older examples for the `rms` package here](http://hbiostat.org/R/rms/examples.html), too. [Bayesian survival analysis is also available using the `rstanarm` package](https://arxiv.org/abs/2002.09633), it seems.

## Today's Discussion

will be centered around replicable research, statistical significance and *p* values. 

### Five Key References

I will include in today's conversation a brief walk through [the 2019 American Statistical Association editorial](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/references/ASA_2019_A_World_Beyond.pdf):

- Ronald L. Wasserstein, Allen L. Schirm & Nicole A. Lazar (2019) [Moving to a World Beyond "p < 0.05"](https://www.tandfonline.com/doi/full/10.1080/00031305.2019.1583913), *The American Statistician*, 73:sup1, 1-19, DOI: [10.1080/00031305.2019.1583913](https://doi.org/10.1080/00031305.2019.1583913). 
    - Ron gave a [one-hour talk you can watch here](https://t.co/GbQF01h4jU) just this past week on "[Helping to move to a world beyond p < 0.05](https://t.co/GbQF01h4jU)" which I cannot recommend enough.

You may also be interested in [the American Statistical Association's 2016 statement on P Values](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/references/ASA_2016_Pvalues_Context_Process_Purpose.pdf) which originally got me thinking along these lines: 

- Ronald L. Wasserstein & Nicole A. Lazar (2016) [The ASA's Statement on p-Values: Context, Process, and Purpose](https://www.tandfonline.com/doi/full/10.1080/00031305.2016.1154108), *The American Statistician*, 70:2, 129-133, DOI:
[10.1080/00031305.2016.1154108](https://doi.org/10.1080/00031305.2016.1154108).

Three other articles I'll be talking about this week are:

- Jeffrey Leek and Roger Peng [P-values are just the tip of the iceberg](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/references/Leek_and_Peng_2015_Pvalues_Nature.pdf)
- Jeffrey D Blume, Lucy D'Agostino McGowan, William D. Dupont, Robert A Greevy [Second-generation p values: Improved rigor, reproducibility and transparency in statistical analyses](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/references/Blume_etal_2018_Second_Generation_P_Values.pdf)
- Andrew Gelman and John Carlin [Beyond Power Calculations: Assessing Type S (Sign) and Type M (Magnitude) Errors](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class22/references/Gelman_Carlin_2014_Beyond_Power_Calculations.pdf)

Some related motivation comes from 

- [Scientists rise up against statistical significance](https://www.nature.com/articles/d41586-019-00857-9) in *Nature* 2019-03-20
- [It's time to talk about ditching statistical significance](https://www.nature.com/articles/d41586-019-00874-8) also in *Nature* 2019-03-19.

We'll spend a bit of time talking about:

- the "PROBABLE CAUSE" graphic reprinted in this [Nature piece by Regina Nuzzo](https://www.nature.com/news/scientific-method-statistical-errors-1.14700), originally from T. Sellke et al. in *The American Statistician*, 2001.
- and several great pieces by Christie Aschwanden at 538:
    - "[Not Even Scientists Can Easily Explain P-Values](https://fivethirtyeight.com/features/not-even-scientists-can-easily-explain-p-values/)", and
    - "[Statisticians Found One Thing They Can Agree On: It's Time To Stop Misusing P-values](https://fivethirtyeight.com/features/statisticians-found-one-thing-they-can-agree-on-its-time-to-stop-misusing-p-values/)", and
    - "[Science Isn't Broken](https://fivethirtyeight.com/features/science-isnt-broken/#part1)" with graphics by Ritchie King.
- You may also be interested in this piece at pbs.org about a NOVA program entitled "[Rethinking Science's Magic Number](https://www.pbs.org/wgbh/nova/article/rethinking-sciences-magic-number/)".
- I have given several talks on "Rethinking Statistical Significance" in recent years. The Github repository for one (90 minutes at MetroHealth Medical Center and the Center for Health Care Research and Policy, with an audio recording) is at https://github.com/THOMASELOVE/rethink, if you're a glutton for punishment.


## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Sun | 04-19 | Minute Paper after Class 23. Submit before 9 AM Sunday to make the feedback.
Mon | 04-20 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) is due at 10 AM.
Thu | 04-23 | Final Class Session
Fri | 04-24 | (Optional) To request a regrade on HW 1-4, complete [this Google Form](http://bit.ly/432-2020-homework-regrade-requests) by 5 PM.
Fri | 05-01 | Final TA Office Hours
Mon | 05-04 | Due Date for All Project 2 deliverables as well as optional Homeworks 5 and 6
