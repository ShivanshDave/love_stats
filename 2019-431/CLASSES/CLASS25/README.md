# 431 Fall 2019 Class 25: 2019-12-03

## Today's Slides

- Class 25 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/431_class-25-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/431_class-25-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

-------------

## Additional Help

- **Supplemental Office Hours** Dr. Love will hold office hours today from 10 AM to 12:45 PM and from 2:30 to 3:30 PM in Wood WG82-J. He also plans to hold office hours this Thursday from Noon to 12:45 PM and from 2:30 to 3:30 PM also in Wood WG82-J.
- TA office hours continue through Friday 2019-12-06. There are no formal TA office hours next week.
- `431-help` remains open until 2019-12-12 at 12 noon. It will re-open in mid-January for students taking 432.

## Deliverables from Today

- Homework I was due today at noon. The Answer Sketch [is now available](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/I/post-deadline.md).
- Be sure to get your Project Study B Task 5 submitted to Canvas. It, too, was due at noon today.

## Remaining Deliverables

1. There is a [Minute Paper after Class 25](http://bit.ly/431-2019-minute-25) due at 2 PM Wednesday 2019-12-04.
2. [Quiz 3](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ3) will be made available to you by 5 PM on Thursday 2019-12-05. It is due on Thursday 2019-12-12 at noon. Some instructions and details are [already posted](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ3).
3. Your Project Portfolio [for Study A](https://thomaselove.github.io/2019-431-project/task6a.html) **and** [for Study B](https://thomaselove.github.io/2019-431-project/task6b.html) are due at 2 PM on 2019-12-11, regardless of when your presentation is scheduled.
4. Your Project Presentation will be in Wood WG82-J, [as scheduled here](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/SCHEDULE). 
    - Presentations run from 2019-12-05 through 2019-12-12. Please come on time, as indicated in the "Arrive At" section. 
    - If the door is open, please come in. If not, have a seat and we'll call you in as soon as possible.
5. Please submit the **course evaluation** form as requested by CWRU. You'll hear from them directly on this.
6. Optionally, submit the [Homework Regrade Request Form](http://bit.ly/431-2019-regrade-requests) form by 2019-12-12 at Noon if you have a specific request of me in that regard.

-------------

## Having Trouble with Project Study A? 

On 2019-11-22, I posted a [revised set of data files](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/STUDY_A) (removing all apostrophes, I think) and also [posted this PDF document](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-describe-after-merging-with-hints.pdf) and the [R Markdown I used to make it](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_A/studyA-2019-describe-after-merging-with-hints.Rmd) which walks step by step through how I created the project directory so that `here()` works as you'd expect, then imported the data sets, then merged them, then generated summaries for all variables in Project Study A. Please look this over if you're having any trouble.

## Repaired Project Study B Example

The old version of the Example had some hard-coding of explanations of results. When I reran the file, R's change in how it selects random numbers (between version 3.5 and 3.6) caught me up, and so some of those explanations described results that were a bit off, because of the different choices for the training and test samples. This was repaired on 2019-12-02, and is available in R Markdown and PDF as part of [the shared Google Drive folder linked here](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/STUDY_B/EXAMPLE).

--------------

## Multiple linear regression teaching assistants (from [Allison Horst](https://twitter.com/allison_horst/status/1197778932575031296))

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/horst1.PNG)
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/horst2.PNG)
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/horst3.PNG)
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/horst4.PNG)
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/horst5.PNG)

----------------

## College Football Predictions?

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS25/collegefb20191201.PNG)

See [the interactive tool at FiveThirtyEight](https://projects.fivethirtyeight.com/2019-college-football-predictions/?ex_cid=rrpromo)

--------------

## Five Last Things

1. Gavin Simpson has a nice new tutorial called [Pivoting Tidily](https://www.fromthebottomoftheheap.net/2019/10/25/pivoting-tidily/) on `pivot_longer` and `pivot_wider`.
2. A new [default color palette](https://developer.r-project.org/Blog/public/2019/11/21/a-new-palette-for-r/index.html) is coming in R version 4.0, which is currently under development. R 3.6.2, which, as I understand it, could well be the final version of R starting with 3, is scheduled for release on 2019-12-12, so I expect we'll be using it in 432.
3. Care to make a beautiful streetmap with ggplot2? [Check out this tutorial](https://ggplot2tutor.com/streetmaps/streetmaps/).
4. A [new paper in BMJ Open by Adrian Barnett and Jonathan Wren](https://bmjopen.bmj.com/content/9/11/e032506.full) examines nearly 1 million confidence intervals in health and medical journals over the period of 1976-2019 and found a huge number (perhaps an unbelievable number) that were just below the magic 0.05 "statistically significant" threshold. See [Adrian's tweet, too](https://twitter.com/aidybarnett/status/1197633930943315968).
5. From Kiirsti Owen, [an R Advent Calendar](https://kiirstio.wixsite.com/kowen/post/the-25-days-of-christmas-an-r-advent-calendar) which is a series of tutorials for learning how to use R.
    - Jason Winget is intending to put up a set of YouTube videos working through the tutorials. The [first one is here](https://www.youtube.com/watch?v=ms7u9jvkjNI).
