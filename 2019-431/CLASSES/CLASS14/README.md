# 431 Fall 2019 Class 14: 2019-10-10

## Today's Slides

- Class 14 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS14/431_class-14-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS14/431_class-14-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Quiz 1

- You will receive [Quiz 1](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ1) by 5 PM. It's due at noon on Monday 2019-10-14 (and there's no grace period, so we mean noon, and not 1 PM). 
- When Quiz 1 is posted (after class today, and by 5 PM), you'll find links to everything you need in the [Key Links section at the bottom of the Quiz 1 page.](https://github.com/THOMASELOVE/2019-431/tree/master/QUIZZES/QUIZ1).
- If you have questions while taking the Quiz, submit them to 431-help. We will not necessarily respond to questions received after 9 AM Monday, but we'll keep up until that point.

## Upcoming Project Deliverables:

- Study A revisions are due TODAY (Thursday 2019-10-10) at 5 PM. You should have already received an email telling you about those revision requests.
- Study B revisions in reaction to either the TA on Canvas or Dr. Love directly will be due on the Wednesday AFTER the Quiz, or 2019-10-16, also at 5 PM. 
- The Study A Task 3 (Review of Items) is still due at 2 PM on 2019-10-18.
- The Study B Task 3 (Data Update) Deadline has been moved back to 2019-10-25 at 2 PM.
- When I make a change, I first update the [Calendar](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md), so that is the most up-to-date thing.

## Reactions to Study B Project Proposals

1. I think everyone has some feedback now on Canvas, from a TA. We've accepted one proposal so far. Congratulations to those folks. Everyone else needs to redo their proposal, sometimes for just a few small things, and sometimes a new data set may be needed.
2. I have provided additional detailed feedback on Canvas to these investigators.
    - Hussam Alqahtani and Kimberly Noriega
    - Fatima Asad and Basma Dahash
    - Rebeka Bordi
    - Erin Cohn and Jessica Scarborough
    - Lauren Cruz
    - Shuai Fu and William ("Dean") Pontius
    - Ahmet Hacialiefendioglu
    - Ziyu ("Jason") Huang and Yufei Li
    - Stephanie Merlino Barr
    - Claire Sonneborn and Lauren Yeh
    - Alena Sorensen and Emily Tyszka
    - Wayne Tsuang
    - Vachan Vadmal
    - Timothy Walker
    - Huasheng ("Victor") Zhou
3. Other projects on my list to review as soon as possible include:
    - Ebtesam Alshehri and Carolyn Goldschmidt
    - Kieran Gallagher and Corrienne ("Corri") Sept
    - Emily Hannon
    - George Hoeferlin and Youjoung Kim
    - Shiying Liu and Yiheng Pan
    - Abigail ("Abby") Roche
    - Seth Rotz
    - Paola Saroufim
4. The remaining 20 projects have detailed reviews from the TAs posted to Canvas, and I don't know that I'm going to provide any additional guidance before you embark on a revision.

A few specific comments:

- If you're working with NHANES data, we want you (if possible) to use at least two panels of data (not just 2015-16 data, but also 2013-14 data so you'll need to combine them.) 
- If the data allow it in any way, if you have more than 2000 observations in your data set (and even if you don't) we also want you to be describing 6-10 predictors in this revision, and not just 4. Of those, at least one must be binary, one must be multi-categorical (with, ideally, 3-7 categories, but no more than 10) and at least one must be quantitative.
- Your outcome must be clearly and obviously quantitative, with units. A count that for all subjects will be between 0 and 10 is not a suitable candidate for an outcome in a linear regresssion model, and we don't want you fitting Poisson or negative binomial regressions in 431.
- If you've got more than 2500 observations after cleaning/management/dealing with missing data, we want you to sample down to 2500, not to something smaller than that.
- In your revision, you need to talk about how you'll handle missing data. The reasonable options are: 
    - use complete cases only (in which case you'll need to specify what that will do to the size of your sample),
    - use the imputation methods we'll study later this term, specifically, you'll certainly be able to use the simputation package to impute missing data (in which case you'll need to specify how much missingness there is in each of the variables you're planning to use).

--------------

## Some Interesting Tests

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS14/nowak_2019-09-20.png)

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS14/psyguy_2019-09-21.PNG)

## Data Analysis: A Next Step (Infographic 2)

- From [@StephStammel](https://twitter.com/StephStammel/status/929904072093720576) How I approach data analysis: infographic style.

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS14/2017-11-12_stammel_2.png)


