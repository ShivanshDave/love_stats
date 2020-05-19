431 Homework B
================
Due 2019-09-06 at 2 PM. Version 2019-09-03

# General Instructions

Homework B includes seven questions. Be sure to respond to each of them.

## An R Markdown Template for Homework B

You will analyze some data, and prepare a report in the form of an HTML
file, using R Markdown. We have provided you with a very useful R
Markdown document template for this assignment called
`YOURNAME-HomeworkB.Rmd` that you should use to complete your work.

  - The `YOURNAME-homeworkB.Rmd` file [is available
    above](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/B/YOURNAME-homeworkB.Rmd).
  - The file is also found on the [Data (and code)
    page](https://github.com/THOMASELOVE/2019-431-data) of our web site.
    Just click on the green **Clone or download** button and select
    Download ZIP to get the files you will need, including the
    `YOURNAME-homeworkB.Rmd` template, as part of a ZIP file. Unzip the
    file on your computer into a directory you can find again, and you
    should be ready to go.

## The Data for Homework B

Homework B uses data from the `midwest` data set, which is part of the
`ggplot2` package (which is part of the `tidyverse`) so by loading the
`tidyverse` package, we will have direct access to the `midwest` data by
typing `midwest`. The `midwest` data describe demographic information
for 437 counties in the midwestern United States. You might use
`?midwest` to obtain a little bit of additional information about these
data, and/or use `View(midwest)` to get a look at a spreadsheet-style
view of the data. We will focus on just four variables in Homework B
taken from this data set:

  - `county` = the name of the county
  - `state` = the name of the state (each county is contained in a
    single state)
  - `percollege` = the percentage of adult residents of the county who
    have completed a college degree
  - `inmetro` = an indicator variable, which takes the value 1 if the
    county is contained in a metropolitan area, and 0 if it is not

# Question 1

Write a piece of R code that counts the number of observations
(counties) in the data set within each state. Your result should also
specify the states which are included in these data. Hint: The `count`
function and the pipe `%>%` should be a big part of your code.

# Question 2

Use the `filter` and `select` functions in R to obtain a result which
specifies the `percollege` and `inmetro` status of Cuyahoga County in
the state of Ohio.

# Question 3

Use the tools we have been learning in the `ggplot2` package to build a
histogram of the `percollege` results across all 437 counties
represented in the data. Create appropriate (that is to say, meaningful)
titles for each axis and for the graph as a whole (do not simply use the
default choices.) We encourage you to use something you find more
attractive than the default gray fill in the histogram.

# Question 4

Based on your results in Questions 2 and 3, write a short description
(2-3 sentences) of the position of Cuyahoga County relative to the full
distribution of counties in terms of `percollege`.

# Question 5

Use `ggplot2` to build a single plot (a pair of histograms after
faceting would be one approach, or perhaps a comparison boxplot) which
nicely compares the `percollege` distribution for counties within
metropolitan areas to counties outside of metropolitan areas. Again,
make an effort to build and incorporate useful titles and labels so that
the resulting plot stands on its own, rather than just accepting all of
the defaults that appear.

# Question 6

Write a short description of where Cuyahoga County falls within the plot
you built in Question 5. the position of Cuyahoga County in terms of
`percollege` relative to the other counties within its `inmetro`
category.

# Question 7

Ask one question of Professor Love about this course (ideally one that
you have not asked us already) that interests you. It can be a question
about the syllabus, the readings, the project, the homework assignments,
the course notes, anything big or small, but it should not be a fact
that you can find already in the [Course
Syllabus](https://thomaselove.github.io/2019-431-syllabus/).

**Hint**: A question ends with a question mark.

# Submitting your Response

Build your response as an R Markdown file, and either an HTML, PDF or
Word document that results from the R Markdown file you built working
from the `YOURNAME-HomeworkB.Rmd` template that we have provided. Submit
both your revised R Markdown file and the HTML output file to
<https://canvas.case.edu/> in the Homework B section. Again, the
deadline is 2019-09-06 at 2 PM.

# A Few Tips

You are welcome to discuss Homework B with Professor Love, the teaching
assistants or your colleagues, but your answer must be prepared by you
alone. Don’t be afraid to ask questions, either in person at office
hours or before/after class, or email **431-help at case dot edu**.

## Grading Rubric

Homework B will be graded on a 0-100 scale, where you will receive 10
points per question for making a reasonable effort to build a good
response (even if that effort isn’t completely successful), and an
additional 5 points on Questions 1-6 if your response is complete,
correct and well-written. Well-written responses use complete English
sentences and show all required R code to achieve the desired result.
