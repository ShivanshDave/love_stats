431 Homework G
================
Due **2019-11-01** at 2 PM. Last Edited 2019-10-30 22:36:58

# General Instructions

There are five questions on this assignment. Question 5 requires an
essay.

## Hints from Professor Love

This homework is challenging. So, here are a few hints.

1.  This is how my answer sketch file starts.

<!-- end list -->

``` r
knitr::opts_chunk$set(comment=NA)
options(width = 60)

library(here); library(janitor); library(broom)
library(PropCIs); library(exact2x2); library(Epi)
library(patchwork); library(magrittr); library(tidyverse)

source(here("R", "Love-boost.R"))

q1_raw <- read_csv(here("data", "hwG_q1.csv")) %>% 
  clean_names()

q2_raw <- read_csv(here("data", "hwG_q2.csv")) %>% 
  clean_names()
```

2.  You will have to do at least some rearrangement work (possibly
    including creating new variables, pivoting, transformation,
    rearrangement, etc.) in order to answer each of the first four
    questions. Each data set will require some management on your part.
    It’s up to you to figure out what needs to be done for each
    Question. Be sure you check for missingness in the data.

3.  The analyses you will do in Questions 1 and 2 relate to population
    means. Is that the case in Questions 3 and 4?

4.  There are some footnotes at the bottom of the page, which may be
    helpful.

5.  If I needed to set a seed in the answer sketch, I used
    `set.seed(431)`. You can use any seed you like (maybe you won’t even
    use one\!), but if you want to match up with the sketch, you
    probably want to use what I did.

# Setup for Questions 1 and 2

Questions 1 and 2 ask you to respond (in complete sentences) to several
sub-items for the studies described below.

  - \[A\] What is the outcome under study?
  - \[B\] What are the treatment/exposure groups?
  - \[C\] Were the data collected using matched / paired samples or
    independent samples? What do you need to do (if anything) to manage
    or rearrange the data for analyses?
  - \[D\] Are the data a random sample from the population(s) of
    interest? Is there at least a reasonable argument for generalizing
    from the sample to the population(s) or is there insufficient
    information provided on this point?
  - \[E\] What is the significance level (or, the confidence level) we
    require here?
  - \[F\] Are we doing one-tailed or two-tailed confidence interval
    generation?
  - \[G\] If we have paired samples, did pairing help (to reduce
    nuisance variation)? How do we know?
  - \[H\] If we have paired samples, what does the distribution of
    sample paired differences tell us about which inferential procedure
    to use?
  - \[I\] If we have independent samples, what does the distribution of
    each individual sample tell us about which inferential procedure to
    use?
  - \[J\] Finally, produce and interpret an appropriate confidence
    interval for a relevant population **mean** that addresses the key
    question from the study, following the requirements of the principal
    investigator. Be sure to show and describe the R code that led to
    your selected confidence interval, and then interpret that interval
    in context using complete English sentences.

# Question 1 (30 points)

Study 1 involves simulated data provided in [the `hwG_q1.csv`
file](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/G/data/hwG_q1.csv),
and based loosely on an article published by Lewis et al. on 2019-09-19
in *The Lancet: Psychiatry*. Quoting that article\[1\]:

> We included patients (from 179 clinics) aged 18 to 74 years who had
> depressive symptoms of any severity or duration in the past 2 years,
> where there was clinical uncertainty about the benefit of an
> antidepressant. This strategy was designed to improve the
> generalisability of our sample to current use of antidepressants
> within primary care. … Patients received one capsule (sertraline 50
> mg) daily for one week then two capsules daily for up to 11 weeks,
> consistent with evidence on optimal dosages for efficacy and
> acceptability.

A PDF of the Lewis et al. article is [posted at this
link](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/G/articles/hwG_q1_article_lancet_lewis_2019.pdf),
should you wish to review it.

Our Study 1 researchers designed their study to replicate some of the
findings of the Lewis group. They measured the Patient Health
Questionnaire, 9 item version (PHQ-9) scores of a set of 275
participating patients at six clinics at the start of the study, and
then after completion of a sertraline medication regimen similar to
those used with the patients in the original study. PHQ-9 scores range
from 0-27, and higher scores indicate more severe depression symptoms.
Our principal investigator prefers a maximum risk of type I error of
10%, and is interested in establishing both upper and lower bounds for
her estimates. Some of the subjects did not complete the regimen and
thus did not complete the follow-up PHQ-9 instrument at 12 weeks after
study entry. The analyses we plan here are “complete case” analyses,
including only those subjects who have provided both a baseline and
follow-up PHQ-9 assessment. The simulated data are described
below.

## Description of the `hwG_q1.csv` file

|     Variable | Description                                                       |
| -----------: | ----------------------------------------------------------------- |
| `subject_id` | Identification Code (S-001 through S-275)                         |
| `assessment` | Time at which PHQ-9 was obtained (start of study or at follow up) |
| `phq9_score` | Total score on PHQ-9 at that assessment for that subject          |

# Question 2 (30 points)

Study 2 involves simulated data provided in [the `hwG_q2.csv`
file](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/G/data/hwG_q2.csv),
based loosely on a research letter\[2\] by Joudrey et al. published
2019-10-01 in *JAMA*. Quoting that letter:

> Methadone for opioid use disorder can be dispensed only from US
> Substance Abuse and Mental Health Services Administration
> (SAMHSA)–certified opioid treatment programs (OTPs), creating access
> barriers in rural counties with a shortage of facilities. … \[W\]e
> examined drive times to the nearest OTP in urban and rural counties in
> 5 US states with the highest county rates of opioid-related overdose
> mortality.

A PDF of the Joudrey et al. letter is [posted at this
link](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/G/articles/hwG_q2_article_jama_joudrey_2019.pdf),
should you wish to review it.

In Study 2, researchers measured drive times (in minutes) to the nearest
certified opioid treatment program (OTP) from the population center for
each of 487 US counties in 5 states\[3\]. Each county was classified as
either **urban** (which included the 217 counties in those states
defined by the six-level National Center for Health Statistics
urban-rural county classification scheme as either *large central
metro*, *large fringe metro*, *medium metro*, or *small metro* counties)
or as **rural** (which included the 270 counties defined as either
*micropolitan* or *noncore* counties.)

You have been asked to provide a supplemental analysis of **simulated**
data (contained in the `hwG_q2.csv` file) in an effort to help address
the question of whether rural counties actually have detectably
**longer** drive times than urban counties. The principal investigator
asking for your help wants you to maintain the same level of confidence
as was used in the original paper\[4\]. The simulated data are described
below.

## Description of the `hwG_q2.csv` file

|           Variable | Description                                                |
| -----------------: | ---------------------------------------------------------- |
|    `county_number` | Identification Code for County (C-001 through C-487)       |
|      `county_type` | NCHS county classification (6 levels listed above)         |
| `drive_in_minutes` | Driving time (minutes) to certified OTP from county center |

# Question 3 (10 points)

Using the Question 1 data and scenario, estimate and interpret an
appropriate **99%** confidence interval comparison of the rate of
patients who have a PHQ-9 score of 10 or higher at the start of the
study to the same rate at follow-up\[5\]. Use a summary statistic of
your choosing that accomplishes this task. As in Question 1, your
analysis should focus on the complete cases, with data at both time
points.

# Question 4 (10 points)

Using the Question 2 data and scenario, estimate and interpret an
appropriate **99%** confidence interval comparison of the rates for
urban vs. rural counties of having a driving time to an OTP of 20
minutes or less.

# Question 5 (20 points)

In *The Signal and The Noise*, Silver writes (in several places prior to
Chapter 12, but especially there) that the goal of any predictive model
is to capture as much signal as possible and as little noise as
possible. What does this mean to you in your scientific and other
endeavours, going forward? Give a specific example. An answer of 150 -
300 words is what we’re looking for.

# Grading

Total score on this Homework ranges from 0 - 100.

Note that Question 1 and Question 2 are each worth 30 points. Parts A,
B, D, E and F are worth 2 points each. Parts C, G and H (if the samples
are paired) or C and I (if the samples are independent) are worth 10
points (together) and this includes any rearrangement or data management
tasks, and then Part J (specification and interpretation of an
appropriate confidence interval) is worth an additional 10 points.

A more detailed rubric will be provided with the answer sketch.

-----

1.  Lewis G Duffy L Ades A et al. [The clinical effectiveness of
    sertraline in primary care and the role of depression severity and
    duration (PANDA): A pragmatic, double-blind, placebo-controlled
    randomised
    trial](https://www.sciencedirect.com/science/article/pii/S2215036619303669).
    *The Lancet: Psychiatry*. Available online 2019-09-19.
    <https://doi.org/10.1016/S2215-0366(19)30366-9>

2.  Joudrey PJ, Edelman EJ, Wang EA. [Drive Times to Opioid Treatment
    Programs in Urban and Rural Counties in 5 US
    States](https://jamanetwork.com/journals/jama/fullarticle/2752051).
    *JAMA*. 2019;322(13):1310–1312.
    <https://doi.org/10.1001/jama.2019.12562>

3.  The five states were Indiana, Kentucky, Ohio, Virginia, and West
    Virginia. Data was unavailable for two counties, so those are
    excluded from the `hwG_q2` data set.

4.  The Joudrey et al. paper presented a mean drive time across all
    counties of 37.3 minutes, with a 95% confidence interval of (35.5,
    39.1) minutes. You should be able to verify that the simulated data
    in `hwG_q2` matches those results. The simulation mirrors this
    particular result, and it also mirrors the means by classification
    shown in the Table accompanying the original letter, but it does not
    mirror any other elements of that data set.

5.  A PHQ-9 score below 10 was taken in the Lewis et al. paper as an
    indicator of remission of depression symptoms.
