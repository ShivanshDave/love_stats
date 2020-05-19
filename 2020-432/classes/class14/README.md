# 432 Spring 2020 Class 14: 2020-03-05

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Class 14 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/432_2020_slides14.pdf) | [Class 14 Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/432_2020_slides14.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Key Topic

Dealing with Aggregated Data in Logistic Regression, Probit Regression 
- These materials are discussed in the [Course Notes](https://thomaselove.github.io/2020-432-book/) in Chapter 18

## Breaking News!

- The Royal Statistical Society [made an announcement yesterday](https://twitter.com/RoyalStatSoc/status/1235174819802632192)

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/figures/guy.png)

## A Few Things That May Help

1. A useful piece of advice for academics from [Dr. Holly Witteman](https://twitter.com/hwitteman/status/1234968102263230464?s=11)

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/figures/witteman.PNG)

2. A powerful piece of insight from [Jenny Bryan](https://twitter.com/JennyBryan/status/1103066293190615041) and from [Paul Sochacki](https://twitter.com/Cyberskout99/status/1103095572288827392) back in 2019.

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/figures/jennybryan_tw.PNG)
![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class14/figures/paul_tw.PNG)

## Today's Announcements

1. There is a [Minute Paper after Class 14](http://bit.ly/432-2020-minute-14), due at 2 PM on Friday 2020-03-06.
2. The [Course Notes](https://thomaselove.github.io/2020-432-book/) have been updated to include Chapters 16, 18, and 21-24, along with placeholders for 17, 19 and 20. I also fixed a couple of typos near the bottom of Chapter 14, in the text describing validation results.
3. For Project 2, I specified [some data sources I'd be pleased to see used more](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project2/README.md#suggested-data-sources). 

## Some Project 1 Tips

I'm moving these to the [Project 1 Late Hints](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/latehints.md) page.

## Regarding `431-help` and Project 1

- `431-help` remains open through Spring Break, but there will be a noticeable slowdown in response times after Sunday at 9 AM.
- Dr. Love will be (essentially) away from email from Friday evening until Thursday morning, with one exception.
    - On Sunday morning at 9 AM, he will review and try to catch up on anything needing his input, ideally finishing that by Sunday at 10 AM. So if you have questions about Project 1 that you think he needs to see, please send them to `431-help` before 9 AM Sunday.
- Anything received after 9 AM Sunday at `431-help` will eventually get addressed, but it's very possible that this help may not come in time for your Project 1. 
- So, we do not promise to respond to any `431-help` questions received after 9 AM Sunday, in time for Project 1. You can ask, certainly, and the TAs will usually be able to help, but Dr. Love cannot guarantee a response.

## Project 1 Submission Deadline

However, this comes with some "good" news. Because Dr. Love will now be unable to start grading the Projects until Wednesday evening, he is extending the deadline for the Portfolio and Poster by 48 hours. They are now due to Canvas at 2 PM on **Wednesday 2020-03-11**.

You will submit the following items to Canvas:

1. Your Project 1 Portfolio (Rmd and HTML versions)
    - We'd like the filenames (if your name was Jane Smith and your final version was from 2020-03-11) to be `portfolio_jane_smith_2020-03-11.Rmd` and `portfolio_jane_smith_2020-03-11.HTML`.
2. Your Project 1 Poster (Rmd and HTML versions)
    - We'd like the filenames (if your name was Jane Smith and your final version was from 2020-03-11) to be `poster_jane_smith_2020-03-11.Rmd` and `poster_jane_smith_2020-03-11.HTML`.
3. Your raw data set(s) as a csv just as you imported them into R in your portfolio
    - No reason to change the filename here. Use whatever you've used previously.
4. Your tidy data set saved as an Rds (R data set) file. This is so that you preserve all of the factor work you've done. Save your R data set to a file in this way by typing in `saveRDS(nameoftidyRtibble, file = here("data", "tidy_yourname.Rds"))`, subsituting in the name of your tidied R tibble. You can do this after section 12 of your portfolio, just before you run the system information function.
    - We'd like the filename to be `tidy_jane_smith.Rds`. 

Thank you.

## Reminders/Notes (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
----: | ---------------------------------------------------------------
03-06 | [Minute Paper after Class 14](http://bit.ly/432-2020-minute-14), due at 2 PM.
03-11 | [Project 1 Posters/Portfolios](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) are due at 2 PM.
Break | No class and no TA office hours from 03-09 through 03-13. `431-help` will be open, but slow.
03-17 | [Project 2 Instructions](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) should be available by 1 PM.
03-20 | There will be a Minute Paper after Class 16, due at 2 PM.
03-23 | [Homework 4](https://github.com/THOMASELOVE/2020-432/tree/master/homework) due at 5 PM
03-26 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) made available at 5 PM
03-30 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) due at 2 PM
04-01 | [Project 2 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) due at 2 PM

# Enjoy Spring Break! 

## Our next class will be Tuesday 2020-03-17.
