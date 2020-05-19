# Materials After Quiz 1

- The [Quiz 1 answer sketch](https://github.com/THOMASELOVE/2020-432/blob/master/quizzes/postquiz1/quiz1_with_sketch.pdf) is available as a PDF file. The PDF includes the entire Quiz, followed by the Results, Sketch and Rubric for each question and overall. 
    - At noon on 2020-03-03, I modified the answer in Question 11 to fix a typo, and explain one of the common errors that I didn't understand previously. At 3 PM, I modified in again, as we figured out the other common mistake in Question 11.
- Your [responses to Question 2](https://github.com/THOMASELOVE/2020-432/blob/master/quizzes/postquiz1/quiz1_checkquestion2code.Rmd) are available as an R Markdown file if you want to see what code I received for you. This is also the place to find my specific comments on your coding.
- Grades have been emailed to all students as of 9 AM on 2020-03-03.

The only item I wasn't happy with (in terms of its performance as a question) was Question 7a, where there were clearly two possible interpretations of what I was asking, and the people who did best on the Quiz tended to select a more stringent interpretation than I had in mind. Since it was only worth 1 point, I left it alone.

There were several items where the class as a whole didn't do as well as I would have hoped, as indicated in the Sketch. Any items where less than 75% of credit was awarded are in this group. In preparing for subsequent Quizzes, items with poorer scores on this Quiz are better candidates for me to build related questions in Quizzes 2 and 3 than questions about things where the class in general has already done well, naturally. 

---

# Original Posting: Quiz 1 Details

All material for Quiz 1 is now posted to the [Shared Google Drive](http://bit.ly/432-2020-quiz1-folder). 

Quiz 1 is due at 2 PM on Monday 2020-03-02.

Quiz 1 is restricted to materials from Classes 1-11, from Chapters 1-14 in the Course Notes, and from Chapters 1-5 and 7-8 in Spiegelhalter's *Art of Statistics*. Subsequent quizzes will also include material from these sections of the course.

All questions about Quiz 1 must be directed to **431-help**. 

## The Data is already on the [Shared Google Drive](http://bit.ly/432-2020-quiz1-folder)

Two data sets are available to support your work on the Quiz. You'll find them in the [Shared Google Drive Folder for Quiz 1](http://bit.ly/432-2020-quiz1-folder) at http://bit.ly/432-2020-quiz1-folder.

- The `lind` data are provided to you in the **lind.Rds** file.
- The `riff` data are provided to you in the **riff.csv** file.

## Other Material You'll Need for Quiz 1 also appears on the [Shared Google Drive](http://bit.ly/432-2020-quiz1-folder)

I have posted [to that same folder](http://bit.ly/432-2020-quiz1-folder):

- a PDF file of the Quiz itself
- a link to the [Google Form Answer Sheet](http://bit.ly/432-2020-quiz1-answer-form) that you'll use to submit your answers to the Quiz.

## Packages I used to create Quiz 1 and its Answer Sketch

For your information, here are the packages and themes I loaded into R to help me complete the Quiz. I used R version 3.6.2. I do not guarantee that all of these packages are actually used, but I didn't need any other packages to complete my answer sketch.

```{r packages, message = FALSE}
library(here); library(knitr); library(magrittr); library(janitor)
library(patchwork); library(tableone); library(rms); library(leaps)
library(caret); library(simputation); library(naniar); library(broom)
library(tidyverse)

theme_set(theme_bw())
```

