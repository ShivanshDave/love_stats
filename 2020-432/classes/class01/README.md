# 432 Spring 2020 Class 01: 2020-01-14

## Today's Announcements

Welcome to PQHS / CRSP / MPHP 432!

- The main website for the course is https://github.com/THOMASELOVE/2020-432.
- Today's [audio recording will be found (in 3 parts) on this Shared Drive](http://bit.ly/432-2020-audio).
- Today's slides are [available in PDF](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/432_2020_slides01.pdf) and [also in R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/432_2020_slides01.Rmd) formats. I used the R Markdown to generate the PDF.
- Karl W. Broman & Kara H. Woo (2018) [Data Organization in Spreadsheets](https://github.com/THOMASELOVE/2019-432/blob/master/references/pdf/Broman_and_Woo_2018_Data_Organization_in_Spreadsheets.pdf), *The American Statistician*, 72:1, 2-10, DOI: [10.1080/00031305.2017.1375989](https://doi.org/10.1080/00031305.2017.1375989) will be discussed today, and is well worth your time, as you start to think about your course project.
- The material we discuss today about building a Table 1 in R is introduced in [Chapter 1 of the Course Notes](https://thomaselove.github.io/2020-432-book/building-table-1.html).
### Getting Help

For any questions related to the course, email **431-help at case dot edu**. Our teaching assistants and myself are now monitoring this, and this should yield the fastest possible response.

- TAs this term: Ben Booker BS, Julijana Conic MD, Joseph Hnath BA, Amr Mahran MD MS, Amin Saad MD and Jing Zhang MD MS. Learn more about the [TAs in the Course Syllabus](https://thomaselove.github.io/2020-432-syllabus/teaching-assistants.html).
- TA office hours start on Friday 2020-01-17. Hours are posted [at the bottom of the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours), and are open to anyone.
- The [R-basics page](https://github.com/THOMASELOVE/2020-432/tree/master/r-basics) provides numerous examples in data cleaning, data management, and coding analyses in R.

### Roster Check

An initial course roster is found at [this Google Sheet](http://bit.ly/432-2020-roster-check). You may need to log into Google via CWRU to see the actual link, and then verify the information (editing where needed), especially the **name** you want us to call you, and your preferred **email**. If you do not appear on this roster, add your information at the bottom of the sheet and email Dr. Love to tell him.

### Upcoming Deliverables - All deadlines are in the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md).

- Complete [the roster check](http://bit.ly/432-2020-roster-check), described above, as soon as possible.
- Please complete the [Minute Paper after Class 01](http://bit.ly/432-2020-minute-01) by 2 PM tomorrow (2020-01-15).
- Read David Spiegelhalter's **The Art of Statistics** Chapters 1-2 for our next class.
- [Homework 1](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw01) is the next assignment.
- Your Proposal for Project 1 will be the next big thing to think about. You'll have all of the details by one week from now.

### Course Password

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/figures/tukey.png)

### Attendance

I expect you to come to class. If you have to miss a single class, just be sure to catch up on any needed materials - no need to let me know in advance or afterwards. We expect you to complete all necessary deliverables, and to review the README for that day's class for other announcements. If you are going to miss **more than one class in a row**, let Dr. Love know, via email, in advance, ideally.

### We'll do some "live" coding today. Materials for that include: 

- [bradley_table1.md](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/bradley_table1.md) = Github Markdown result of applying my code
- [bradley_table1.Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/bradley_table1.Rmd) = R Markdown code
- [bradley.csv](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/data/bradley.csv) data file, which the code expects to be in a `data` subfolder.
- Or maybe you want to skip to the resulting file created in R to represent Table 1, at [bradley_table1_result.csv](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/bradley_table1_result.csv). We can import this straight into Excel.

There is also a pair of files showing how I simulated the `bradley.csv` data in R: [bradley_sim.md](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/bradley_sim.md) and [bradley_sim.Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/bradley_sim.Rmd), if you are curious.

## Tweet of the Day

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/figures/branch_tw.png)

---------

## One Last Thing

Over the course of the semester, we'll look at several of the [Best Data Visualization Projects of 2019](https://flowingdata.com/2019/12/19/best-data-visualization-projects-of-2019/) as identified by Nathan Yau at [flowingdata.com](https://flowingdata.com/). 

- Today, we'll focus on [How to Cut U.S. Emissions Faster? Do What These Countries Are Doing](https://www.nytimes.com/interactive/2019/02/13/climate/cut-us-emissions-with-policies-from-other-countries.html) by Brad Plumer and Blacki Migliozzi at The New York Times from 2019-02-13.

![https://www.nytimes.com/interactive/2019/02/13/climate/cut-us-emissions-with-policies-from-other-countries.html](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class01/images/nyt_emissions_2019-02-13.PNG)

----------

## Other Materials discussed today

### On Data Organization

- The [Leek group guide to data sharing](https://github.com/jtleek/datasharing): "How to share data with a statistician"
- Shannon Ellis and Jeff Leek "[How to share data for collaboration](https://peerj.com/preprints/3139/)" preprint.
- Hadley Wickham's paper on [Tidy data](https://www.jstatsoft.org/article/view/v059i10) from *J of Statistical Software*
- Jenny Bryan "[Naming Things](https://speakerdeck.com/jennybc/how-to-name-files)" presentation on [SpeakerDeck](https://speakerdeck.com/jennybc/how-to-name-files).
- Wilson, Bryan, Cranston, Kitzes, Nederbragt and Teal "[Good enough practices in scientific computing](https://github.com/swcarpentry/good-enough-practices-in-scientific-computing#readme)".
- CRAN vignette providing an overview of functions in [the `janitor` package](https://cran.r-project.org/web/packages/janitor/vignettes/janitor.html) including `clean_names`.
- We saw several cartoons from [XKCD](https://xkcd.com/).

### Building Table 1

- Today's Table 1 example came from Bradley SM, Borgerding JA and Wood GB et al. [Incidence, Risk Factors, and Outcome Associated with In-Hospital Acute Myocardial Infarction](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2720923), published 2019-01-18 in *JAMA Network Open* doi:10.1001/jamanetworkopen.2018.73
- [Instructions for Table Creation](https://jama.jamanetwork.com/data/ifora-forms/jama/tablecreationinst.pdf) from JAMA

----------

## For Next Time

- If you haven't [completed the Roster Check](http://bit.ly/432-2020-roster-check) yet, please do so now.
- The Minute Paper after Class 01 is at http://bit.ly/432-2020-minute-01. Please complete it by 2 PM tomorrow (2019-01-23).
- We'll be discussing Chapters 1 and 2 of David Spiegelhalter's *The Art of Statistics*. Please read those chapters before class.
- We'll be discussing the cleaning of the BRFSS/SMART data shown in [Chapter 2 of the Course Notes](https://thomaselove.github.io/2020-432-book/brfss-smart-data.html).
- Skim Frank Harrell & others (2019) [Glossary of Statistical Terms](http://hbiostat.org/doc/glossary.pdf). 
    - In today's class, we assumed you knew, for example, what the following terms mean: binary variable, case-control study, categorical variable, comparative trial, confidence limits, continuous variable, data science, dummy variable, estimate, goodness of fit, inter-quartile range, mean, median, nonparametric estimator, nonparametric tests, normal distribution, null hypothesis, observational study, one-sided test, *p*-value, parametric test, percentile, predictor, probability, quartiles, random error, random sample, rate, replication, risk, significance level, standard deviation, standard error, two-sided test, Type I error, variance.
    - If any of these terms seem unfamiliar, read up on them. If that's not too overwhelming, then glance through the remainder of the list and find a few more that interest you, and read those closely.
- If you haven't done so already, get up to date versions of R, R Studio and the necessary R Packages on your computer. Instructions are on our [Software page](https://github.com/THOMASELOVE/2020-432/blob/master/software.md).


