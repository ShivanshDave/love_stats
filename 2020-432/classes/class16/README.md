# 432 Spring 2020 Class 16: 2020-03-24

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 16 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class16/432_2020_slides16.pdf) | [Class 16 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class16/432_2020_slides16.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- Zoom has finished its processing! [The link to the Class 16 recording is here](https://cwru.zoom.us/rec/share/_MYkcvL3qX9OQ6v9xxD-QKUBT6K0T6a8gXIX_aFYz0rVtLcAVvL8jxx-SZ5BiNld?startTime=1585069253000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a place for you to communicate with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.

## Announcements

1. Please do not assume we know what you're going through. If you're having trouble with anything related to the course, large or small, please ask.

2. I've had to change the 432 Class Zoom sessions to no longer allow you to sign in before I do. 
    - I will try to open each session at about 12:45 PM, and I will stay on the line until everyone else is gone after class. I changed this to stop accidental log-ins, and reduce the delay in Zoom processing the recordings.

3. [Feedback on the Minute Paper after Class 15](https://bit.ly/432-2020-minute-15-feedback) is now available.
    - Thanks for responding.
    - One question I want to be sure to addresss was "... if we're presenting with a partner, are the two presentations supposed to complement each other or should they describe the same information, but in our own separate words (as if we were presenting alone)?"
        - The former. They should complement each other. In your video presentation, we want one of you to give the first half of the full presentation, and the other to give the second half. You're not giving two different versions of the same material - you're each presenting half of your group's complete presentation.
    - I've also adjusted the time limit for the video presentations [in the Project 2 Instructions](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project2/README.md) to give you 3-5 minutes if you're working alone, and a total of 6-8 minutes (3-4 minutes each) if you are working with a partner.

4. I revised the [Hint for Homework 4](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/homework4_hints_2020-03-21.pdf) on 2020-03-21 to clarify that we only use the simple imputation in Question 4 and 5, but not in the remainder of the Homework.
    - A student asked about the choice of transformation in Question 5, specifically why I suggest the use of the logarithm instead of the inverse square root. [I wrote a long answer](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/question5_discussion.md) with some generally useful advice. 
    - [TL;DR](https://www.howtogeek.com/435266/what-does-tldr-mean-and-how-do-you-use-it/)? Box-Cox point estimate isn't that critical. All models are wrong, some are useful, and the log is more useful (easier to interpret) than the inverse square root. 

5. I added Chapter 19 (Regression Models for Count Outcomes) and Chapter 20 to the [Class Notes](https://thomaselove.github.io/2020-432-book).
    - [Chapter 19](https://thomaselove.github.io/2020-432-book/modeling-a-count-outcome-in-ohio-smart.html) goes into more extensive detail on the models we'll discuss today provides even more options.
    - [Chapter 19](https://thomaselove.github.io/2020-432-book/modeling-a-count-outcome-in-ohio-smart.html) doesn't cover cross-validation for models with count outcomes. That's only in today's slides.
    - I also revised Section 11.7.3 to fix a typo (replaced MSE with MAE.)
    - [Chapter 20](https://thomaselove.github.io/2020-432-book/modeling-an-ordinal-categorical-outcome-in-ohio-smart.html) illustrates approaches for modeling ordinal multi-categorical outcomes, which will be our next topic. 

6. Project 1 grading continues. I am hoping to have grades for all by the end of this week, and I'm very grateful to the TAs for helping me with the posters. Further bulletins as events warrant, but it won't be sooner than Thursday.

7. To install the `countreg` package we'll use to build rootograms for count outcome model results today, type `install.packages("countreg", repos="http://R-Forge.R-project.org")` into the R Console within R Studio.

8. I am not deeply in the "looking at COVID-19 data" business myself, but I added several things to [our resources list](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) that I encourage you to look at if you're interested.

## Upcoming Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Wed | 03-25 | [Homework 4](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw04) due to Canvas at 5 PM. Don't miss [the revised Hints](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw04/homework4_hints_2020-03-21.pdf).
Sun | 03-29 | Minute Paper after Class 17 deadline is 9 AM. Dr. Love will write up the feedback on Sunday.
Wed | 04-01 | [Project 2 Proposal Google Form](http://bit.ly/432-2020-project2-proposal-form) due at Noon. [Project 2 instructions are here](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2).
Thu | 04-02 | Be sure you've read **ART** through Chapter 11 before Class.
Fri | 04-03 | [Quiz 2](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes/quiz2) will be made available (it's due 2020-04-20)

