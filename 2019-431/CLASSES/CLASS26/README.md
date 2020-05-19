# 431 Fall 2019 Class 26: 2019-12-05

## Today's Slides

- Class 26 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/431_class-26-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/431_class-26-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Please [fill out this form](http://bit.ly/431-2019-last-class-survey) now.

There's a 90-second survey for you to fill out at http://bit.ly/431-2019-last-class-survey. You should have received it also via email this morning. Please do it now, so that everyone's results are in by the end of class today. Thanks! As of 12:50, 31/59 had done this.

## Extended Office Hours

- Dr. Love is available today 2:30 - 3:45. A *great* time to run an idea or a plot by him, or see where his office is.
- TA office hours continue today and tomorrow, and that's it.
- 431-help is open all weekend and next week through Thursday at noon.

## Remaining Deliverables

1. [Quiz 3](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ3) will be available to you by 5 PM. It is due on Thursday 2019-12-12 at noon. Visit [this link](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ3).
2. Your Project Portfolio [for Study A](https://thomaselove.github.io/2019-431-project/task6a.html) **and** [for Study B](https://thomaselove.github.io/2019-431-project/task6b.html) are due at 2 PM on 2019-12-11, regardless of when your presentation is scheduled.
3. Your [Project Presentation](https://thomaselove.github.io/2019-431-project/task7.html) will be in Wood WG82-J, [as scheduled here](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT/SCHEDULE). 
4. Please submit the **course evaluation** form as requested by CWRU. You'll hear from them directly on this.
5. Optionally, submit the [Homework Regrade Request Form](http://bit.ly/431-2019-regrade-requests) form by 2019-12-12 at Noon if you have a specific request of me in that regard.

-------------

## [Today's Fun Interactive: 3D Animation of Measles in the US](https://datapleth.io/blog/2019/10/17/2019-10-17_usa_measles_map_video/)

Or read the [tweet](https://twitter.com/datapleth/status/1202338909340012545). All made with rayshader and R. [Code is available.](https://datapleth.io/blog/2019/10/17/2019-10-17_usa_measles_map_video/)

-------------

## Feedback on the Minute Paper after Class 25 

[is available here](http://bit.ly/431-2019-minute-25-response). I sent it out by email last night, so I'll skip over this today.

-------------

## Check out [this example](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/example_26.md).

This is an issue that's come up in looking over some of the early project work. Let's see what you can come up with...

-------------

## 12 Key Tips and Things I'll Look For In Evaluating Your Portfolio

These are generic things about R coding that apply to everyone, and though some of them are perhaps less important than good models, visualizations and explanations in your portfolio, but show an attention to detail that is also a meaningful part of your grade.

1. A tip: You should expect to need to restart R within RStudio many times. Ctrl-Shift-F10 or Cmd-Shift-F10 is the way to do it. Definitely restart R if something that "worked before" stops working. I restart R routinely before knitting a R Markdown for the "final" time.

2. Another tip: Update R to 3.6.1 and then be sure to update all of your packages in R before producing the final version of your portfolio.

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/images/update_packages.PNG)

3. I will be looking to see that all packages are:

- loaded at the top of the document with `library()` commands without additional `library()` commands later in the document, and 
- are visible to me in the HTML results (i.e. not hidden within the setup section), and
- are not accompanied by useless warnings or messages, and 
- are actually used in the document somewhere (don't load things senselessly)

You must load `here` and the `tidyverse` in both studies, at a minimum. 

- I will be very suspicious if you're not also using `janitor` and `magrittr` (in both Studies) and `broom` (at least in Study B) and `Epi` (at least in Study A).

4. You need to show the use of the `here()` package, specifically in the context of reading in data for Study A, but also Study B, unless you're using a package like NHANES to pull in data. I will check to see that you're using it properly. 

- If you've set up your project study A and study B as R Projects, this should be very simple. 

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/images/proj1.PNG)
![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/images/proj2.PNG)

- Two reasonable approaches, assuming your data is in a csv file in a subfolder of your main project are: 
    - `read_csv(here("subfoldername", "datasetname.csv"))` or 
    - `read_csv(here("subfolder/datasetname.csv"))`.

5. I will want to see blank lines in between code chunks and text in your R Markdown files, and between paragraphs, too. Hit ENTER a lot.

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/images/badgood.PNG)

6. Every part of each of your HTML files should have an appropriate heading linked in the table of contents, and you should use complete sentences in the text between headings whenever possible. Use subheadings for subparts of your work. Follow the templates I've provided. Write text as plain text, and use #, ## and ### to build headings only. If you want to bold things, use **bold text** and to italicize, use *italicized text*.

7. Your HTML files should display no warnings, since you should have fixed all of those. As for messages, use `message = FALSE` in the chunk header to hide the unimportant ones. Most of them are unimportant. 

8. Use either `sessionInfo()` or `sessioninfo::session_info()` at the end of each R Markdown file, and include those results at the end of your HTML, so that I can verify you're using the right form.
    - [For example, go here](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS26/sessioninfo.md) to see my `session_info()` result after Quiz 3.

9. Run spell check on your R Markdown file before knitting it into HTML. Just hit F7.

10. If you want to build a table, make sure it looks right in HTML before you submit it. If you are having problems mirroring the approaches I've used, ask us for help at 431-help, please.

11. You need to submit both R Markdown and HTML for Study A, and both R Markdown and HTML for Study B. If your csv file submitted as part of Task 5 needs to change, you should submit that again, as well.

12. Don't include anything in your HTML that you wouldn't be happy to have me look at, either in your portfolio presentation or later. If you have questions, ASK THEM OF US BEFOREHAND at 431-help, please!

## On the project presentation itself

In your presentation, you'll be walking me through your HTML file. You won't be live coding in R Studio, and you are welcome, but by no means required, to provide some additional source (like a Powerpoint) if that helps you. But you will have to show me your HTML document, at a minimum, and of course, that's a big part of what you'll submit in the Portfolio.

- I suggest you think of the presentation as more of an important meeting with an active lead investigator rather than as a formal presentation to a quiet audience.
- You'll be seated, in my office, and we'll be looking together at your laptop. Although there is a place to plug it in, try to bring it properly charged. My computer will be busy.
- I will definitely make you jump around in your presentation, focusing on things I want to evaluate in person.
- If you're working with a partner, I will make you switch off regularly. You won't know in advance who is speaking about what. 
    - To prepare, the best advice is to get it done early enough that you can have some time to explain/teach what you're trying to show to each other, and then switch roles. 
    - When I ask questions, I'll want to hear from each of you, so if one of you answers the first few, I'll focus on the other person.
- I use a version of the form at http://bit.ly/431-2019-project-eval-draft to make notes at the end of each presentation and help me construct my final evaluation after all of the projects for the day are done.
- As noted previously, there are some specific questions I will ask you at the end of your presentation. Check the draft evaluation form below to be sure you're ready for those issues.

-------------

## From Today's Session

We're going to take a look at [an interactive from 538, located here](https://fivethirtyeight.com/features/science-isnt-broken/#part1) from Christie Aschwanden and Ritchie King, to hammer home a few ideas.

-------------

## "After Class" Materials

After today, subsequent postings will appear on [the "After Class" page](https://github.com/THOMASELOVE/2019-431/blob/master/AFTER_CLASS/README.md). If you go there now, you'll find the materials for 432, including the book I'd like you to get started reading over the break.

-------------

## One Last Thing

Thank you for taking the class, and putting up with the workload. I hope you'll look back on it fondly. I look forward to seeing you all in the next week, and to enjoying what I'm sure will be some terrific projects.

TEL
