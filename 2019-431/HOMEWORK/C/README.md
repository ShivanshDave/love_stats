431 Homework C
================
Due **2019-09-13** at 2 PM. Last Edited 2019-09-08

# General Instructions

Homework C includes eleven questions. Be sure to respond to each of
them. You are welcome (encouraged, really) to discuss Homework C with
Dr. Love, the teaching assistants or your colleagues, but your answer
must be prepared by you alone.

## An R Markdown Template for Homework C

We have again provided a useful R Markdown document template for this
assignment called `YOURNAME-HomeworkC.Rmd` that you should use to
complete your work.

  - The `YOURNAME-HomeworkC.Rmd` file is available in the [main folder
    for Homework
    C](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/C).
  - The file is also found on the [Data (and code)
    page](https://github.com/THOMASELOVE/2019-431-data) of our web site.
    Just click on the green **Clone or download** button and select
    Download ZIP to get the files you’ll need, including the
    `YOURNAME-HomeworkC.Rmd` template, as part of a ZIP file. Unzip the
    file on your computer into a directory you can find again, and
    you’ll be ready to go.

## The Data for Homework C

The setup for this assignment involves the following chunk of R code.

``` r
knitr::opts_chunk$set(comment=NA)
options(width = 70)

library(MASS); library(tidyverse)
## make sure these packages are loaded in R
```

The data come from the `faithful` data frame contained in the base
installation of R, specifically, within the `datasets` package. These
data describe the duration of an eruption for the Old Faithful geyser in
Wyoming’s Yellowstone National Park, as well as the waiting time until
the next eruption.

The commands below place the `faithful` data frame in a tibble called
`hwC`, then display the tibble. We encourage you to use this `hwC`
tibble to develop your answers to Questions 1-10.

    hwC <- tbl_df(faithful)
    hwC

Use the command `?faithful` to see some additional details about these
data. The `hwC` tibble contains observations on two variables:

  - `eruptions` = eruption time in minutes
  - `waiting` = waiting time to next eruption, also in minutes

# Question 1

Plot a histogram or other summary plot which meaningfully describes the
distribution of the waiting times. Be sure it is very clearly labeled.

# Question 2

What appears to be a typical waiting time? Compare the mean, median and
80% trimmed mean (mean of the middle 80% of the observed waiting times.)

# Question 3

What is the inter-quartile range, and how does it compare to the
standard deviation?

# Question 4

Is the distribution multi-modal or unimodal? How do you know?

# Question 5

Is the distribution skewed (and if so, in which direction) or is it
essentially symmetric? How do you know?

# Question 6

Are there any unusual (outlier) values in the distribution, and if so,
what are they?

# Question 7

Would a model using the Normal distribution be an appropriate way to
summarize the waiting time data? Why or why not?

# Question 8

Plot a scatterplot of the waiting times (y-axis) vs. the eruption
durations (x-axis) and be sure your plot is very clearly labeled.
Describe your general impression of the plot: what sort of relationship
do you see?

# Question 9

What is the correlation of waiting time with eruption duration? How
would you interpret this result?

# Question 10

Would a linear model be an appropriate thing to use in attempting to
predict the waiting time given the most recent eruption duration, based
on these data? Why or why not? Add a simple least squares regression
line to the plot.

# Question 11

Investigate questions 8-10 again using the `geyser` data in the `MASS`
package, and compare your results to what you obtained originally, in an
appropriate way.

  - Use the heading **Question 11a** to describe your response to
    question 8 using the new data.
  - Use the heading **Question 11b** to respond to question 9 with the
    new data.
  - Use **Question 11c** to respond to question 10.

Be sure to use the command `?MASS::geyser` to see some additional
details about these data, and to learn more about how they differ from
the data in our original data set.

**Hint**: There is at least one key difference between the variables
available in `geyser` and those which you dealt with in the `faithful`
data. For full credit, you must specify that difference (and describe
its impact) in your response.

The commands below will place the relevant data for these questions in
the `hwCextra` tibble.

    hwCextra <- tbl_df(MASS::geyser)
    hwCextra

# On Grading

Homework C will be graded on a 0-100 scale. You will receive some credit
for making a reasonable effort to build a good response to each
question, and then additional credit if your response is (essentially)
correct, your code is clean and you’ve written any text using complete
English sentences. A more detailed breakdown of the grading rubric will
appear with the answer sketch.
