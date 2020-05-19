# A Few Additional Hints for Homework I

Since we won't hold office hours between 2019-11-23 and 2019-11-30, and we will be responding infrequently to 431-help during that time, I want to be sure that Homework I goes smoothly. So here are some thoughts in that direction:

1. Question 1 is an essay. You've seen those. 
2. Questions 2-6 involve working with a data set we have provided to fit and evaluate a few multiple regression models.
    - The first hint is already in the R Markdown template. 
        - The strategy for importing the data that it uses requires that you create a subdirectory called R within your project for Homework I. In that data subfolder, put the hwI_plasma.csv data set we have provided.
        - Once you open your R project for Homework I, use here() to figure out where the directory is that R is looking for things, and create the data subdirectory there.
    - Question 2 involves pulling in the data, and then plotting the `betaplasma` variable and then the logarithm of `betaplasma`.
        - We did something just like this in Class 23
    - Question 3 involves building a model with several predictors, and interpreting its R-square and residual standard error.
        - Again, the Class 23 slides can help
    - Question 4 involves estimating the effect of an indicator for female (as compared to male) on your outcome, with a 95% confidence interval.
        - This was largely skimmed over in the slides, but, not to worry, examples abound in other material (see below.)
    - Question 5 asks you to compare two models in terms of adjusted R-square and residual standard error.
        - Again, we did this in Class 23
    - Question 6 provided you with a link to code to compare the prediction errors made by the two models you've fit.
        - We will do this today in Class 24
3. On finding code examples for Questions 2-6.
    1. Use the code in the [Study B Example Portfolio](https://github.com/THOMASELOVE/2019-431/blob/master/PROJECT/STUDY_B/EXAMPLE/README.md) to help you do what you need to do in Homework I Questions 2-6.
        - Question 2: look at section 9 (step 3), especially sections 9.1 and 9.2 to think about the distribution of the outcome, and section 10 discusses some transformation checking ideas. You don't need Box-Cox in Homework I, specifically, since we won't consider any potential transformations other than the log, but you're welcome to run it and see what it suggests.
        - Question 3: Sections 11 and 12, for instance, discuss and demonstrate model-building.
        - Question 4: Section 11.3, for example, provides ample information on this topic.
        - Question 5: take a look at section 13 (step 7) for some ideas here
        - Question 6: as mentioned in the homework itself, section 14 is the place to go.
    2. Look at the code provided in Classes 22-24 in the Slides to help you do that work, as indicated above. I'd probably work directly from the [Class 24 slides](https://github.com/THOMASELOVE/2019-431/tree/master/CLASSES/CLASS24), since that contains all of the information in one place.
    3. Look closely at the [Course Notes](https://thomaselove.github.io/2019-431-book/), where the most relevant Chapters for this work are probably 34-37 and 40.
