# 431 Fall 2019 Class 08: 2019-09-19

## Today's Slides

- Revised Class 08 slides are posted in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS08/431_class-08-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS08/431_class-08-slides_2019.Rmd) above. 
    - I've added key slides from what was originally planned for Class 07 as Part 1 of the Class 08 slides now. Then, in Part 2 of the Class 08 slides, we'll start working on the slides originally posted for today's class. Everything is in the revised set above.
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.
- Homework C grades are posted. [Visit the post-deadline materials](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/C/post-deadline.md).

## Deliverables Reminder

1. [Homework D](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/D) is due Friday 2019-09-20 at 2 PM.
    - I fixed a typo about an hour ago. The variable originally listed as `least.dev` is actually `least_developed` in the data. I apologize for any confusion. Please help me kill typos.
2. We expect you to read Chapters 2-3 of *The Signal and the Noise* for next Tuesday 2019-09-24.
3. [Homework E](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/E) is due next Friday 2019-09-27 at 2 PM.
4. Project Task 1 ([Scheduling for Presentations](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/SCHEDULE)) is due at 9 AM on Monday 2019-09-30.

## Do you know how to use spell check in RStudio?

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS08/spellcheck.PNG)

-----

## [Today is an important day](https://en.wikipedia.org/wiki/International_Talk_Like_a_Pirate_Day)

Definitely a good day to discuss our favorite subject...

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS08/today.jpg)

Shiver me timbers!

------

## Minute Paper Feedback

[Comments on the Minute Paper after Class 07](http://bit.ly/431-2019-minute-07-response) are now available. Thanks to everyone for filling out the form. I really appreciate it.

## Project: Should I work with a Partner?

1. There is no need to do so.
2. If you do, the two of you will work together on both Study A and Study B, and will present the same findings for both Studies to me in your portfolio and in your presentation, which will occur at the same time. 
    - Everything you present and everything you analyze must be joint work, for every part of the project except for actually taking the Course Survey (which everyone will do individually). 
    - All analyses for Study A and all analyses for Study B would be jointly by the two of you. If you're reading the instructions as suggesting anything different, you are misunderstanding what I've written (and let me know, so I can clarify the instructions.)
3. If you're potentially working with a partner, you will need to be in the same small group as they are on 2019-09-24, but you don't actually commit until the [Project Scheduling Form](http://bit.ly/431-2019-project-scheduling) ([Project Task 1](https://thomaselove.github.io/2019-431-project/task1.html)) due at 9 AM on 2019-09-30.
    - In filling out that form, you and your partner will need to identify each other as your partner, and you'll need to put down the same schedule of available time slots and preferences.
4. The 10 small groups (each will have 6 people) we will create on 2019-09-24 to complete two tasks in Study A do not materially affect your grade in any way. There is no reason to be nervous about those small groups, and they will disband as we take the actual Survey.

### Why do I allow you to work with a partner on the project?

1. There are 60 students in the class and intensively experiencing 60 individual projects over three days is almost impossible for me, based on past experience. I get too tired to engage properly, and I want to avoid that.
2. Some people want very much to be able to work with another person on the project.

My experience is that working with a partner works out very well **only if** you and your partner have different skills with which you are comfortable, so that together you are comfortable with much more than you are individually, and that you make a substantial commitment to spend the time to teach each other what each of you are comfortable with, so that by the end, you both have acquired new skills. This almost inevitably leads even the most successful partners to say at the end that the project took them longer (working together) than it would have if they'd done it alone (although they also believe the quality of the finished project is much better than it would have been if they'd worked alone.) 

- If you're working with a partner just to save time by somehow having to do less work, I would rate your chances of success (in either producing a high-quality project, or in actually feeling like its meaningfully less work) as low.
- If you're working with a partner because you have complimentary "comfort zones" or because your work is of higher quality when you feel accountable to another person, then that's a great idea.

Again, there is no advantage or disadvantage that I can see to working with a partner on the Project.

## Project: Two Key Issues Regarding Acceptable Study B Data Sets for 431

1. Regarding the Study B data, you must have at least 250 and no more than 2,500 observations. (If you have more than 2,500 observations, you'll look at a subset that fits in that limit.)
    - If you have a fascinating data set with 200-249 observations, contact Professor Love with some details in advance (including available variable descriptions and your proposed research question) to see if he will provide you special dispensation. In most cases, he'll recommend you find another set for 431, and consider using your fascinating data in one of your 432 projects, which have less stringent rules. If you have less than 200 observations, find other data.

2. Also regarding the Study B data, *hierarchical* (or *multi-level*) data is not what we want for 431, either. Some examples of what **will not** work for 431 (but *might* be OK for one of the 432 projects)...
    - Suppose you have data measured at the county level for counties located in several states, and want to include both county and state-level variables in your model. You must have the same unit of observation for each row in your data set, and for each variable you are studying.
    - Suppose you have time series data from a series of hospitals, and you want to study the effects of changes in quality ratings over time on some outcome in the future, so you have the same hospitals at each time period, and want to include some hospital-level predictors as well as measures for each hospital at separate times as predictors. Not in 431. 
    - Also, suppose you have data on a set of patients (where the predictors are all measured at some baseline point in time), and you want to assess their outcome (measured a year later.) That's OK, but you cannot include longitudinal measurements in the predictors, at all, and you cannot include anything longitudinal in the outcome except a simple difference between the outcome a year later and the outcome at baseline.

## One Last Thing

If we have time today, we'll return to [FiveThirtyEight.com's analysis of the recent Democratic Primary Debate](https://fivethirtyeight.com/features/who-won-the-debate-among-voters-who-prioritize-electability-health-care-climate-change/).

- Specifically, we'll discuss a piece by Laura Bronner and Nathaniel Rakich called [Who Won The Debate Among Voters Who Prioritize Electability? Health Care? Climate Change?](https://fivethirtyeight.com/features/who-won-the-debate-among-voters-who-prioritize-electability-health-care-climate-change/) from 2019-09-17.
- Laura Bronner and Ella Koeze also have a great item called [The Third Democratic Debate in 7 Charts](https://fivethirtyeight.com/features/the-third-democratic-debate-in-7-charts/) from 2019-09-13 that may be of interest.

If we don't have time, we'll discuss this stuff next Tuesday.

--------

## A Non-Class-Related Announcement

is on [my theater page](https://github.com/THOMASELOVE/theater). I've been cast in a play. Further details to come as the performances (November 1, 2, 8, 9, 10, 15 and 16) approach. 

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS08/2019-07-28_hayes.png)

