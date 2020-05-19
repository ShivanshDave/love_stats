431 Homework D
================
Due **2019-09-20** at 2 PM. Last Edited 2019-09-19 11:41:38

# General Instructions

This homework includes seven questions, including an Essay in response
to reading a piece of Nate Silver’s *The Signal and the Noise* as
Question 6. Be sure to respond to each of the questions.

As always, you are encouraged to discuss this Homework with Dr. Love,
the teaching assistants or your colleagues, but your answer must be
prepared by you alone.

# The `unicef_lbw` Data, for Questions 1-5

These data come from
<https://data.unicef.org/topic/nutrition/low-birthweight/> and
<https://data.unicef.org/regionalclassifications/>.

> In 2015, 20.5 million newborns, an estimated 14.6 per cent of all
> babies born globally that year, suffered from low birthweight. These
> babies were more likely to die during their first month of life and
> those who survived face lifelong consequences including a higher risk
> of stunted growth lower IQ and adult-onset chronic conditions such as
> obesity and diabetes. To grow a healthy baby, mothers need good
> nutrition and rest, adequate antenatal care, and a clean environment.
> Together, these ingredients for a healthy pregnancy can help to
> prevent, identify and treat the conditions that cause low birthweight
> and thus foster achievement of the World Health Assembly (WHA)
> nutrition target to reduce low birthweight by 30 per cent between 2012
> and 2025.

The data describe, among other things, the percentage of low birth
weight (less than 2,500 grams) infants for a number of nations
(actually, counties and territories, but I’ll refer to them as nations
here) around the world. I built up the `unicef_lbw.csv` data set which
includes the following elements.

  - `iso3_code` = three-letter code for each nation
  - `nation` = the nation’s name
  - `pct_low_birthweight` = the nation’s low birth weight percentage
    estimate from 2015 (updated June 2019) from
    <https://data.unicef.org/wp-content/uploads/2014/10/Low-birthweight-data-2000-2015.xlsx>
  - `unicef_subregion` = March 2017 regional classifications from
    UNICEF, found at <https://data.unicef.org/regionalclassifications/>
  - `least_developed` = whether or not the nation is regarded by the
    United Nations High Representative for the Least Developed
    Countries, Landlocked Developing Countries and Small Island
    Developing States as one of the “least developed” countries on Earth
    (note that `least_developed` = 1 if the nation is in the “least
    developed countries” group and `least_developed` = 0 otherwise.)
  - `pct_no_birthweight` = the nation’s percentage of births without a
    birthweight (updated May 2019, but the data come from surveys
    usually between 2010 and 2016) from
    <https://data.unicef.org/wp-content/uploads/2014/10/birthweight-data-coverage-web-May-2019.xlsx>

You’ll probably want to review [these Notes on the Data provided by
UNICEF](https://data.unicef.org/topic/nutrition/low-birthweight/).

Import the `unicef_lbw.csv` file into R Studio, turn it into a tibble,
then use that result to answer questions 1-5.

# Question 1

How many nations have non-missing low birth weight percentage estimates?

# Question 2

Which nations have the three largest low birth weight percentages? Are
each of these considered by the UN to be “least developed” nations or
not?

# Question 3

Create a histogram of the low birth weight percentages, then superimpose
a normal density function with the same mean and standard deviation in
red. Based on your plot, is the standard deviation or the inter-quartile
range a more appropriate measure of variation in the low birth weight
rates? Why?

## Hint for Questions 3-5

If you found missing data in the low birth weight percentage estimates
earlier, you may want to consider restricting the data you use to answer
Questions 3-5 to nations with complete data on that variable.

# Question 4

Create a normal Q-Q plot for the low birth weight percentage estimates.
Would you say that the data are approximately Normally distributed, or
not approximately Normally distributed? Justify your answer by
interpreting what you see in your plot, and whatever summary statistics
you deem to be useful in making your decision.

# Question 5

Display an effective graph comparing the two development groups (least
developed nations vs. all other nations) in terms of their percentages
of low birth weight births. What conclusions can you draw about the
distribution of low birth weight rates across the two development
groups? Be sure to label your graph so it stands alone, and also
supplement your graph with separate text discussing your conclusions.

## Hint for Question 5

You may want to store the variable that indicates the development groups
as a factor to facilitate your plotting. Consider whether renaming the
levels of that factor to be more meaningful is an option that would help
you.

# Question 6 - When is “more data” not necessarily a good thing?

Read the Introduction and Chapter 1 of Nate Silver’s *The Signal and the
Noise*. One possible takeaway, particularly from the Introduction,
suggested, for example in a review by Jonah Sinick, might be that
increased access to information can do more harm than good.

Tell us about an example in your own field/work/experience where a
“surplus” of information made (or makes) it easier for people dealing
with a complex system to cherry-pick information that supports their
prior positions. What were the implications of your example in terms of
lessons that can be learned? If you can connect your example to some of
the lessons described in the Chapter 1 discussion of the failure to
predict the 2008 catastrophe on the US economy, that would be welcome.

Please feel free to supply as many supporting details as are useful to
you in relating the story. An appropriate response to Question 6 will
use complete English sentences with proper grammar and syntax, will cite
a link or two to a Web URL or other published work, and be between 200
and 400 words long.

# Question 7

Generate a “random” sample of 75 observations from a Normal distribution
with mean 100 and standard deviation 10 using R. The `rnorm` function is
likely to be helpful. Now, display a normal Q-Q plot of these data,
using the `ggplot2` package from the `tidyverse`. How well does the Q-Q
plot approximate a straight line?

Repeat this task for a second sample of 150 Normally distributed
observations, again with a mean of 100 and a standard deviation of 10.
Then repeat it again for samples of 25 and 225 Normally distributed
observations *using a different mean and standard deviation* than the
first two plots you built. Which of the four Q-Q plots you have
developed better approximates a straight line and what should we expect
the relationship of sample size with this phenomenon to be?

# On Grading

Homework D will be graded on a 0-100 scale. The essay in Question 6 is
worth 30 points, and will be graded by the teaching assistants according
to guidance from Professor Love. No answer sketch will be provided for
essay questions, throughout the semester. We expect your essay
presentation to be part of your R Markdown and HTML files, **without**
further editing outside of R Studio.

For the remaining questions, as in the past, you will receive some
credit for making a reasonable effort to build a good response to each
question, and then additional credit if your response is (essentially)
correct, your code is clean and you’ve written any text using complete
English sentences. A more detailed rubric for grading will appear at the
end of Dr. Love’s Answer Sketch.
