# 432 Spring 2020 Class 23: 2020-04-16

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 23 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/432_2020_slides23.pdf) | [Class 23 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/432_2020_slides23.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 23 is available here](https://cwru.zoom.us/rec/share/1e1IBJb9qmFIQp32s0jBfvMaJKfLaaa813Mar_ELyRteGlEYc_NGkxQt69mGTsgP?startTime=1587056460000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a white board for communication with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.
- The [COVID-19 Resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) will remain available through May, although I expect to stop adding to it May 1.
- [Things I Won't Get To This Semester](https://github.com/THOMASELOVE/2020-432/blob/master/not_this_semester.md)

## Announcements

1. There is a [Minute Paper after Class 23](https://bit.ly/432-2020-minute-23). Please complete it by 9 AM Sunday.
2. Please remember to submit [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) before 10 AM on Monday.
    - If you want to be able to access the Quiz 2 alternative assignment, let Dr. Love know via email by 9 AM Sunday. No commitment or reason is required.
3. Rebecca Barter has a great post on [tidymodels](http://www.rebeccabarter.com/blog/2020-03-25_machine_learning/) which in some ways is the successor to the `caret` package to help you do machine learning things within the tidyverse. Next year's course will use this approach, certainly. Other key references Rebecca cites include...
    - [A Gentle Introduction to tidymodels](https://rviews.rstudio.com/2019/06/19/a-gentle-intro-to-tidymodels/) by Edgar Ruiz
    - Alison Hill's slides on [Introduction to Machine Learning with the Tidyverse](https://education.rstudio.com/blog/2020/02/conf20-intro-ml/).
4. For those of you putting together a codebook...

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/figures/tweet_rows_2020-04-14.png)

## Today's Discussion

will be centered around replicable research as well as thinking about power issues through retrospective design. The main resources are:

- Andrew Gelman and John Carlin [Beyond Power Calculations: Assessing Type S (Sign) and Type M (Magnitude) Errors](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/references/Gelman_Carlin_2014_Beyond_Power_Calculations.pdf)
- Ronald L. Wasserstein, Allen L. Schirm & Nicole A. Lazar (2019) [Moving to a World Beyond "p < 0.05"](https://www.tandfonline.com/doi/full/10.1080/00031305.2019.1583913), *The American Statistician*, 73:sup1, 1-19, DOI: [10.1080/00031305.2019.1583913](https://doi.org/10.1080/00031305.2019.1583913). The PDF of this article [is also available here](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/references/ASA_2019_A_World_Beyond.pdf).
- Ronald L. Wasserstein & Nicole A. Lazar (2016) [The ASA's Statement on p-Values: Context, Process, and Purpose](https://www.tandfonline.com/doi/full/10.1080/00031305.2016.1154108), *The American Statistician*, 70:2, 129-133, DOI:
[10.1080/00031305.2016.1154108](https://doi.org/10.1080/00031305.2016.1154108). PDF [also available here](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/references/ASA_2016_Pvalues_Context_Process_Purpose.pdf).

### Need to have a tough talk with someone about p values?

- The ASA Section on Teaching of Statistics in the Health Sciences has [some interesting material](https://tshsblog.wixsite.com/main/single-post/2018/05/08/ReadyResources-Publications-for-teaching-p-values)
- I've given these posts: [Why I've lost faith in p values, part 1](https://lucklab.ucdavis.edu/blog/2018/4/19/why-i-lost-faith-in-p-values) and [Why I've lost faith in p values, part 2](https://lucklab.ucdavis.edu/blog/2018/4/28/why-ive-lost-faith-in-p-values-part-2) to a few people. Maybe they'll help you.
- "[Abandoning statistical significance is both sensible and practical](https://peerj.com/preprints/27657/)" by Amrhein, Gelman, Greenland and McShane at PeerJ Preprints.
- Frank Harrell's post about "[Language for communicating frequentist results about treatment effects](https://discourse.datamethods.org/t/language-for-communicating-frequentist-results-about-treatment-effects/934)"
- "[Calculating Observed Power is Like Believing in Fairy Tales](https://lesslikely.com/statistics/observed-power-magic/) at [LessLikely](https://lesslikely.com/)
    - "A discussion of events that transpired in the past year, where a group of surgical researchers decided to ignore much of the statistical literature and promote a highly misleading practice of calculating post-hoc power using the observed effect size."
    - Some related pieces at LessLikely include "[When Can We Say That Something Doesn't Work?](https://lesslikely.com/statistics/evidence-of-absence/)" and "[Misplaced Confidence in Observed Power](https://lesslikely.com/statistics/misplaced-power/)".
- Andrew Gelman: [Statistical-significance thinking is not just a bad way to publish, it’s also a bad way to think](https://statmodeling.stat.columbia.edu/2019/03/16/statistical-significance-thinking-is-not-just-a-bad-way-to-publish-its-also-a-bad-way-to-think/) - the money quote: "it’s ultimately not about what it takes, or should take, to get a result published, but rather how we as researchers can navigate through uncertainty and not get faked out by noise in our own data."

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/figures/shruggies.PNG) from [Kevin Reuning](https://twitter.com/KevinReuning/status/796107864704188420)

 
## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Sun | 04-19 | [Minute Paper after Class 23](https://bit.ly/432-2020-minute-23). Submit before 9 AM Sunday, please.
Sun | 04-19 | 9 AM: Last chance to request Quiz 2 alternative via email. (No commitment/reason needed.)
Mon | 04-20 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) is due at 10 AM.
Thu | 04-23 | Final Class Session
Fri | 04-24 | (Optional) To request a regrade on HW 1-4, complete [this Google Form](http://bit.ly/432-2020-homework-regrade-requests) by 5 PM.
Sun | 04-26 | Minute Paper after Class 25. Submit before 9 AM Sunday to make the feedback.
Fri | 05-01 | Final TA Office Hours. 
Fri | 05-01 | 5 PM: Last chance to request Project 2 alternative via email. (No commitment/reason needed.)
Mon | 05-04 | Due Date for All Project 2 deliverables as well as optional Homeworks 5 and 6

# One Last Thing

Have you heard about [raincloud plots](https://github.com/RainCloudPlots/RainCloudPlots)?

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class23/figures/raincloud_example.png)


