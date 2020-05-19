431 Homework E
================
Due **2018-09-27** at 2 PM. Last Edited 2019-09-14 20:15:52

# General Instructions

This homework includes seven questions, including an Essay in response
to reading a piece of Nate Silver’s *The Signal and the Noise* as
Question 7 which will likely take you about as long as doing the other
questions, combined. Be sure to respond to each of the seven questions.

Don’t be afraid to ask questions, either of Professor Love, or of the
teaching assistants, either in person at office hours or before/after
class, or email **431-help at case dot edu**. Remember that your answer
must be prepared by you alone.

# Data for Questions 1-6

One of the data frames that comes with the base installation of R
(technically, as part of the `datasets` package) is the classic
Anderson/Fisher *iris* data set, that gives the measurements (in cm) of
the sepal length and width and the petal length and width for 50 flowers
from each of 3 species of iris. The species are *iris setosa*, *iris
versicolor* and *iris virginica*.

For more on the iris data, which has been used as an example in
multivariate statistical modeling and data mining courses for decades,
you might visit [its Wikipedia
page](https://en.wikipedia.org/wiki/Iris_flower_data_set). Yes, of
course, this data set has its own Wikipedia page. To look at the data
set in R, just type in `iris`. You can and should create a tibble
containing the iris data (I suggest using the name `iris1` for your
tibble) in the usual way. Then use this tibble to answer questions 1-6.

# Question 1

Across the entire sample of 150 flowers, find and interpret the
correlation of petal length and petal width. Does it matter much whether
you use the Pearson or Spearman correlation?

# Question 2

Draw an appropriate scatterplot to assess the prediction of petal length
(our *outcome*) using petal width as a predictor. Include both a loess
smooth and regression line in your plot. Does the plot suggest that a
straight line model is appropriate in this case?

# Question 3

Suppose we are interested in which of the three types of iris (*setosa*,
*versicolor* or *virginica*) shows the strongest *linear* relationship
between petal length and petal width. Draw an attractive and
thoughtfully labeled plot of the relevant data to address this issue,
accompanied by a sentence or two describing the key findings from your
plot. Postpone the discussion of a numerical summary to Question 4.

# Question 4

Is the *correlation* between petal length and petal width larger or
smaller in the sample of 150 flowers than in the species-specific
samples of 50 flowers each? Why does this appear to be the case? On the
basis of your correlation, which iris type shows the strongest *linear*
relationship for the prediction of petal length on the basis of petal
width? Specify the Pearson correlation (to two decimal places) for your
strongest model here.

# Question 5

Using the strongest model that you identified in question 4, what is the
difference in the predicted petal length between two new flowers, one of
whom has a petal width at the 75th percentile of the original data for
that iris type, and the other of whom has a petal width at the 25th
percentile of the original data for that iris type? Be sure to specify
which of the two new flowers would be expected to be longer.

# Question 6

Build an attractive and thoughtfully labeled plot (which might include
multiple facets, for instance) of the relationship between *sepal
length* and *sepal width*, so that the plot distinguishes between the
three types of iris. For example, you might use color to indicate each
iris type, and show color-coded loess smooths (or linear fits, your
choice) for each iris type. Or be more creative. Describe the
conclusions of your plot in a nice caption.

# Question 7 - Fox or Hedgehog?

In anticipation of this assignment, you’ve read through Chapters 2 and 3
of Nate Silver’s *The Signal and The Noise.*

I’m curious to know if a field you are interested in is more inclined to
predicting like a fox or a hedgehog. Can you (briefly, in 175-325 words)
describe how a field of interest to you (perhaps your choice of field
here should exclude baseball or political punditry, since Nate has
covered those well in these chapters) makes its predictions?

To do this, please provide an example from your chosen field of a
*typical* presentation of an important conclusion made by a thought
leader, with an appropriate citation, and a little context. In your
view, are conclusions in your field mostly presented in a
probabilistically defensible way, or else with more certainty than
perhaps can be supported. Why might this be so?

# On Grading

Homework E will be graded on a 0-100 scale. The essay in Question 7
(which is worth 30 of those 100 points) will be graded by the teaching
assistants according to guidance from Professor Love. No answer sketch
will be provided for essay questions, throughout the semester. We expect
your essay presentation to be part of your R Markdown and HTML files,
**without** further editing outside of R Studio.

For the remaining questions, as in the past, you will receive some
credit for making a reasonable effort to build a good response to each
question, and then additional credit if your response is (essentially)
correct, your code is clean and you’ve written any text using clear,
complete English sentences.
