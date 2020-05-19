# 431 Fall 2019 Class 15: 2019-10-15

## Today's Slides

- Class 15 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS15/431_class-15-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS15/431_class-15-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Agenda for Today

1. Discussion of Quiz 1
    - [Grades on Quiz 1](http://bit.ly/431-2019-grades) and [the Quiz 1 answer sketch](https://github.com/THOMASELOVE/2019-431/blob/master/QUIZZES/QUIZ1/2019-431-quiz01-sketch_and_results.pdf) are now available. 
2. Statistical Inference and the `dm431` data: Comparing Population Means using Independent Samples 
    - wherein I'll attempt to finish off the key material from Course Notes: Chapters 19-20.
3. Discussion of [Draft Survey for Project Study A](http://bit.ly/431-2019-10-15-draft-survey-for-review).
4. Small Group Meetings (to complete Study A Task 3.)

## Upcoming Deadlines

1. The [Minute Paper after Class 15](http://bit.ly/431-2019-minute-15) is due Wednesday 2019-10-16 at 5 PM. (*Note special time.*)
2. Unless your project proposal for Study B has been approved, your revisions to [Study B Task 2 (Proposal)](https://thomaselove.github.io/2019-431-project/task2b.html) are due to Canvas at the same time: Wednesday 2019-10-16 at 5 PM.
    - Dr. Love will review these as they come in, and will give you a deadline for further revisions, as needed.
3. [Study A Task 3 (Review of Items by your Small Group)](https://thomaselove.github.io/2019-431-project/task3a.html) is due at 2 PM Friday 2019-10-18. The Draft Survey for this Task is found at http://bit.ly/431-2019-10-15-draft-survey-for-review.
4. [Study B Task 3 (Data Update)](https://thomaselove.github.io/2019-431-project/task3b.html) is due at 2 PM Friday 2019-10-25.
5. The final version of the Study A Survey will appear at http://bit.ly/2019-431-survey by 5 PM on 2019-10-23. You will need to complete [Study A Task 4 (Taking the Survey)](https://thomaselove.github.io/2019-431-project/task4a.html) by 10 AM on Monday 2019-10-28.
6. [Study A Task 5 (Comparison Plan)](https://thomaselove.github.io/2019-431-project/task5a.html) is due at 2 PM on Wednesday 2019-10-30.
7. [Homework G](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/G) is due at 2 PM on Friday 2019-11-01.

## Announcements

1. Grades on Homework F were posted to http://bit.ly/431-2019-grades on 2019-10-14 at 9 AM.
2. All nine project groups have successfully completed Study A Task 2 and should proceed on to Study A Task 3.
3. Please remember that our next class will be on **Thursday 2019-10-24**, because Dr. Love will be at Study Section in DC for the rest of this week, and because of "Fall Break" for CWRU next Monday and Tuesday.

## Comments on Project Study B

Each of the 43 proposals has now been reviewed on Canvas by a teaching assistant and by Professor Love. At present, most project Study B proposals require revision. The next revision is due Wednesday 2019-10-16 at 5 PM. Submit your revision to Canvas, as an updated version of the proposal you submitted initially. I will review submissions as I receive them.

- The more common problems were with data descriptions. To help, I've built [an example of what I'm looking for in a data description in your revision](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/data_description_demo.md), and also built a list of some of the concerns that came up repeatedly in reviewing your work.
- As I see your revisions, I will react. I intend to update the status of each project proposal at http://bit.ly/431-2019-studyB-proposal-status as well as on Canvas. There are three essential groups there, as of now: 
    1. Approved proposals (score of 1 on Canvas, move on to Study B Task 3) - note that these are in a separate tab of the sheet.
    2. Proposals where the data should work, I think, but I have other concerns requiring a REDO
    3. Proposals where I'm not convinced the data can work, and maybe also have other concerns. REDO.

Don't forget about these comments (originally provided in the [Class 14 README](https://github.com/THOMASELOVE/2019-431/tree/master/CLASSES/CLASS14)):

- If you're working with NHANES data, we want you (if possible) to use at least two panels of data (not just 2015-16 data, but also 2013-14 data so you'll need to combine them.)
- In your revision, we ideally want you to be describing 6-10 predictors, and not just 4. Of those, at least one must be multi-categorical (with, ideally, 3-7 categories, but no more than 10) and at least one must be quantitative. You can also include binary predictors, of course.
- Your outcome must be clearly and obviously quantitative, with units. A count that for all subjects will be between 0 and 10 is not a suitable candidate for an outcome in a linear regresssion model, and we don't want you fitting Poisson or negative binomial regressions in 431.
- If you've got more than 2500 observations after cleaning/management/dealing with missing data, we want you to sample down to 2500, not to something smaller than that.
- In your revision, you need to talk about how you'll handle missing data. The reasonable options are:
    - use complete cases only (in which case you'll need to specify what that will do to the size of your sample),
    - use the imputation methods we'll study later this term, specifically, you'll certainly be able to use the simputation package to impute missing data (in which case you'll need to specify how much missingness there is in each of the variables you're planning to use).
    
## Project B Example Portfolio

In Study B, you'll eventually be producing a full portfolio in Task 6. The [Project Study B Example portfolio](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_B/EXAMPLE/README.md) is now available.

Note that the Study A Example portfolio will be posted by 2019-11-05. The Project Instructions have been updated to reflect this.

---------------

## 2 PM Activity - Small Project Groups

All nine groups are now working on [Study A Task 3](https://thomaselove.github.io/2019-431-project/task3a.html). The deadline is Friday 2019-10-18 at 2 PM to submit that work, although most groups can probably complete the work and submit it today.

- To do this work, you'll need the Complete Draft of the Survey, at http://bit.ly/431-2019-10-15-draft-survey-for-review.

> As with Study A Task 2, one member of your small group will submit Study A Task 3 for the entire group, by sharing a Google Doc with Professor Love via email directly to him. Be sure that Professor Love receives an email indicating that the Task 3 form is ready for his review. The document should, of course, be shared with all six members of your small group.

The Google Doc should contain, at the top, the names of all members of the group and the group name, followed by two sections, labeled as follows:

A. Our corrections/clarifications to the draft survey (found, again, at http://bit.ly/431-2019-10-15-draft-survey-for-review). Be sure to specify which item(s) you are trying to correct or clarify referring to them by their codes on the draft survey.

B. Our new (0-3) proposed items for the survey. 

Please use the time today to do as much as you can to complete this Task. The sooner I get this back from you, the better.

