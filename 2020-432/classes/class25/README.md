# 432 Spring 2020 Class 25: 2020-04-23

## Today's Materials

Information on connecting to class and to TA office hours via Zoom was emailed 2020-03-17. For details, [visit this link](https://github.com/THOMASELOVE/2020-432/blob/master/zoom.md). 

PDF of Slides | .Rmd of Slides | Notes during Class | Need Help? 
------------: | :------------------: | :---------------------------: | :------------------------:
[Class 25 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class25/432_2020_slides25.pdf) | [Class 25 RMD](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class25/432_2020_slides25.Rmd) | [Google Doc](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) | Email **431-help at case dot edu** or attend [TA office hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#ta-office-hours)

- [The Zoom recording for Class 25 including post-class Q and A is here](https://cwru.zoom.us/rec/share/w5N2KJ-z9G9LTrfEsH7SWI8POtXuaaa8gyQW-PAEzU8HkH9-6oW41wMeY5tLzYt6?startTime=1587660666000).
    - [A separate recording of JUST the COVID-19 stuff (not included in the recording above) is here](https://cwru.zoom.us/rec/share/w5N2KJ-z9G9LTrfEsH7SWI8POtXuaaa8gyQW-PAEzU8HkH9-6oW41wMeY5tLzYt6?startTime=1587666920000).
- The [Google Doc of Notes During Class](https://docs.google.com/document/d/1VpnXK654mVLJKMnbxMyhvLSEaOwyZhO2itaMf1a3N4U/edit?usp=sharing) is a white board for communication with Dr. Love and the rest of us (and for Dr. Love to remind himself of things) during class, especially if you cannot connect to the Zoom Chat.
- The [COVID-19 Resources page](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) will remain available through May, although I don't promise to update it again after today.
- [Things I Won't Get To This Semester](https://github.com/THOMASELOVE/2020-432/blob/master/not_this_semester.md)

## Today's Agenda

1. Announcements and Project Reminders
2. [Slides for Class 25](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class25/432_2020_slides25.pdf)
3. [Other Stuff I want to tell you about](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class25/stuff.md)
4. [New COVID-19 resources](https://github.com/THOMASELOVE/2020-432/blob/master/covid19resources.md) (if time permits)

## Announcements

1. Remember that if you want Dr. Love to regrade homework 1, 2, 3 or 4, you need to submit [this Google Form](http://bit.ly/432-2020-homework-regrade-requests) by 5 PM this Friday 2020-04-24.
2. There is a [Minute Paper after Class 25](https://bit.ly/432-2020-minute-25). Please complete it by 9 AM Sunday 2020-04-26.
3. The University has asked you to evaluate the course at https://webapps.case.edu/courseevals/. Please do this by their deadline, which is Thursday May 7. It really, really matters, especially this semester.
4. TA office hours continue through May 1, and 431-help is open to help with any statistical questions (Project 2 or otherwise) through May 4 at noon, and then we will be closed for the summer.
5. The 431 and 432 web sites will disappear in June, so grab anything you need before June 1. If you need something after that, email me and I'll get back to you when I can, although you'll find my response time slows noticeably in the summer.
6. Everyone who completed Quiz 2 should have an email from me specifying your Quiz 2 grade. 
    - Details on course grading are at http://bit.ly/432-2020-grading-plan. The only change since our discusssion in Class 15 is that I added 3 extra points to Quiz 2 rather than to the Class Participation cap.
    - If you have any questions about how your course grade is determined, let Dr. Love know via email.
7. **If you'd like to be a TA** for 431 or 432 (or both) next year, we expect to have both paid and volunteer positions available. I'd be delighted to have you involved. Information about applying for positions will be emailed between May 15 and June 15. If you have questions, let us know.

# Important Project 2 Notes

### What is the Objective in Project 2?

There are three main components of the Project, all due 2020-05-04 at noon.

- The objective of the Main Document is for you to produce something that will be of as much use to you as possible two years from now when you're trying to remember what you did. It's like the Portfolio from Project 1, not the Poster. Do not show sanity checks or false starts, but present and describe every part of the data science process that you used to get to the place where you wound up.
- The objective of the Video Presentation is to ask and answer your research question in a convincing way using your data in a very short time period.
- The objective of the [End-of-Term Form](https://bit.ly/432-2020-project2-end-form) question about your conclusions is to get you to summarize your study in 50 or so very well-chosen words.

## Some Notes

1. As part of your submission for Project 2, you need to complete [an end-of-term Google Form](https://bit.ly/432-2020-project2-end-form) which is now available at https://bit.ly/432-2020-project2-end-form.
2. The most common questions we get about Project 2 involve whether or not to include something in your project. The answer is almost inevitably that the best way to determine this (for anything not explicitly required by the Project 2 instructions) is to look at your research question. 
    - The answer to virtually all questions about any analysis or communication is "it depends on your research question." 
    - If your progress towards learning about and answering your research question is helped in an important way by the (graph/analysis/approach/table/sentence) you're thinking about including, include it. If not, don't. 
    - Interesting detours are not meant to show up in this Project. This advice is even more directly relevant when thinking about the presentation. Three minutes goes by very, very quickly. 
3. As [Brendan Molin](https://twitter.com/bmo_molin/status/969596193692180480?s=11) suggests, don't skimp on the exploratory data analysis.
4. The key to a mind-capturing project is **good visualization** of the data. Show us the data!
    - You may be interested in this list of [50 `ggplot2` Visualizations (with R code)](http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html) which also links to some more introductory materials. If you want to build a waffle chart, dumbbell chart, slope chart, show clusters, build maps, or many more things, this is a nice resource. Some of the tools it uses come from the `ggExtra` package.
    - You may also like this [graphics companion from Trafford Data Lab](http://www.trafforddatalab.io/graphics_companion/index.html) which demonstrates a range of useful graphical forms via `ggplot2`.

An important reminder:

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class25/figures/turner_tw.png)

5. From [Andrew Gelman](http://andrewgelman.com/2018/03/02/audition-fools-explore/): Two important attributes of a good scientist are (a) an openness to being surprised and (b) a willingness to do the hard work to collect data of high enough quality to be able to surprise you.
6. I've changed [the grading scheme for Project 2](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project2/README.md#grading-project-2) very slightly, to allow me to award 80 points for successful completion of all elements by the 2020-05-04 deadline, and then award up to 20 for the quality of that work.
7. You may be wondering what feedback you'll get from me on Project 2 after they are all submitted on 2020-05-04. The answer is that if the project is acceptable, **almost none** - you'll get a numeric grade, and that's all. If this is a disappointment, I'm sorry. 


## Remaining Deliverables (see the [Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md) for a complete list)

Day | Date  | Description and Deadline
:--: | ----: | ----------------------------------------------------------------------------------------------
Fri | 04-24 | (Optional) To request a regrade on HW 1-4, complete [this Google Form](http://bit.ly/432-2020-homework-regrade-requests) by 5 PM.
Sun | 04-26 | [Minute Paper after Class 25](https://bit.ly/432-2020-minute-25). Submit before 9 AM Sunday to make the feedback.
Fri | 05-01 | Final TA Office Hours. 
Fri | 05-01 | 5 PM: Last chance to request Project 2 alternative via email. (No commitment/reason needed.)
Mon | 05-04 | Due Date for all Project 2 deliverables as well as optional Homeworks 5 and 6

### Remember also to evaluate the course at https://webapps.case.edu/courseevals/ by Thursday 2020-05-07.

### The five major deliverables required for the rest of the course are due at NOON on 2020-05-04 

This includes the three remaining deliverables described in the [Project 2 instructions](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2).

- [Project 2](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) Main Document (R markdown **and** HTML **and** R data set files)
- [Project 2](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) Video Presentation
- [Project 2](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project2) End-of-Term Google Form to be found at https://bit.ly/432-2020-project2-end-form.

plus the two *optional* homeworks:

- (*optional*) [Homework 5](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw05) which you submit via Canvas
- (*optional*) [Homework 6](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw06) which you submit by sending an email to Dr. Love with the subject line "432 Homework 6: My Website".

