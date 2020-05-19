432 Homework 1
================

# Answer Sketch for Homework 1 is now available.

- [PDF](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw01/sketch/sketch_hw1.pdf)
- [R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw01/sketch/sketch_hw1.Rmd)
- Homework 1 grades are now posted to http://bit.ly/432-2020-grades. Check your email for your HW-Code.

# General Instructions

Submit your work via [Canvas](https://canvas.case.edu/). The deadline is
specified on [the Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md).

Your response should include an R Markdown file and an HTML document
that is the result of applying your R Markdown file to the `hbp432.csv`
data, available in the data subfolder for this homework, as well as on
our Data and Code page. Start a separate R Project for Homework 1, as
your first step, and place the data in that project’s directory or
(perhaps better) in a data sub-directory.

## The `hbp432` data

The (simulated) data describe 432 patients with hypertension (high blood
pressure) diagnoses who receive primary care in one of two practices.
The data are based on real clinical information describing a year’s
worth of data, but with a small amount of noise included in every
variable.

|    Variable | Description                                                                                                                                                          |
| ----------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   `subject` | separate code for each subject (A001 = first patient in practice A)                                                                                                  |
|  `practice` | primary care practice, labels are A, B, C and D                                                                                                                      |
|  `provider` | primary care provider (multiple levels, each practice has multiple providers in these data)                                                                          |
|       `age` | subject’s age as of the start of the one-year reporting window                                                                                                       |
|      `race` | subject’s race (4 levels: Asian/P\[acific\] I\[slander\], Black / A\[frican\]-A\[merican\], White, Multi-Racial)                                                     |
|  `eth_hisp` | is subject of Hispanic/Latino ethnicity? Yes or No                                                                                                                   |
|       `sex` | subject’s sex (F or M)                                                                                                                                               |
| `insurance` | subject’s primary insurance (Medicare, Commercial, Medicaid, Uninsured)                                                                                              |
|    `income` | estimated median income of subject’s home neighborhood (via American Community Survey, to nearest $100)                                                              |
|    `hsgrad` | estimated percentage of adults living in the subject’s home neighborhood who have graduated from high school (via American Community Survey, to the nearest percent) |
|   `tobacco` | tobacco use status (Current, Former, or Never)                                                                                                                       |
|   `depdiag` | does subject have depression diagnosis? Yes or No                                                                                                                    |
|    `height` | subject’s height in meters, rounded to two decimal places                                                                                                            |
|    `weight` | subject’s weight in kilograms, rounded to one decimal place                                                                                                          |
|       `ldl` | subject’s LDL cholesterol level, in mg/dl                                                                                                                            |
|    `statin` | does subject have a current prescription for a statin medication? 1 = Yes or 0 = No                                                                                  |
|     `bpmed` | does subject have a current prescription for a blood pressure control medication? 1 = Yes or 0 = No                                                                  |
|       `sbp` | subject’s most recently obtained systolic blood pressure, in mm Hg                                                                                                   |
|       `dbp` | subject’s most recently obtained diastolic blood pressure, in mm Hg                                                                                                  |

Here’s a quick glimpse of the data.

``` r
hw1 <- read_csv(here("data", "hbp432.csv"))

mosaic::inspect(hw1)
```

``` 

categorical variables:  
       name     class levels   n missing
1   subject character    432 432       0
2  practice character      4 432       0
3  provider character     34 432       0
4      race character      4 426       6
5  eth_hisp character      2 428       4
6       sex character      2 432       0
7 insurance character      4 432       0
8   tobacco character      3 428       4
9   depdiag character      2 432       0
                                   distribution
1 A001 (0.2%), A002 (0.2%) ...                 
2 B (29.4%), A (26.9%), D (23.8%) ...          
3 B06 (7.2%), A02 (6.2%), B07 (6.2%) ...       
4 Black/AA (69%), White (26.3%) ...            
5 No (93.2%), Yes (6.8%)                       
6 M (51.4%), F (48.6%)                         
7 Medicare (49.1%), Commercial (25.2%) ...     
8 Former (37.1%), Never (34.8%) ...            
9 No (81.7%), Yes (18.3%)                      

quantitative variables:  
     name   class     min      Q1   median       Q3       max         mean
1     age numeric   24.00    54.0    62.00    71.00     89.00 6.242130e+01
2  income numeric 7200.00 24650.0 33000.00 42100.00 102500.00 3.550422e+04
3  hsgrad numeric   38.40    74.2    83.00    87.60     98.30 8.122365e+01
4  height numeric    1.42     1.6     1.68     1.78      1.93 1.684186e+00
5  weight numeric   41.50    73.0    86.60   101.10    205.30 8.927796e+01
6     ldl numeric   26.00    74.0    92.00   120.00    226.00 9.913861e+01
7  statin numeric    0.00     0.0     1.00     1.00      1.00 5.578704e-01
8   bpmed numeric    0.00     0.0     1.00     1.00      1.00 7.245370e-01
9     sbp numeric   94.00   122.0   133.00   144.00    210.00 1.352807e+02
10    dbp numeric   48.00    70.0    78.00    83.00    136.00 7.733411e+01
             sd   n missing
1  1.315333e+01 432       0
2  1.657816e+04 427       5
3  8.665504e+00 427       5
4  1.079699e-01 430       2
5  2.400086e+01 431       1
6  3.485697e+01 404      28
7  4.972155e-01 432       0
8  4.472652e-01 432       0
9  1.878464e+01 431       1
10 1.131020e+01 431       1
```

## Question 1. (50 points)

Build a Table 1 to compare the subjects in practice A to the subjects in
practice C on the following nine variables: age, race, Hispanic
ethnicity, sex, primary insurance, body mass index, BMI category, and
systolic and diastolic blood pressure. Make the Table as well as you can
within R Markdown, and display the result as part of your HTML file.
**Include a description of the important results from your Table 1 that
does not exceed 100 words, using complete English sentences**.

1.  Be sure that your table specifies the number of subjects in each
    practice. **Note that you’ll have to do something so that your work
    focuses on the comparison of practice A to practice C, leaving out
    (for this question only) the other practices.**
2.  You’ll have to deal with some missingness in the data, in an
    appropriate way. Be sure to specify what you did with the missing
    data (and how much you had to deal with) in a footnote to the table.
    Specifically, list the notes as a bulleted list in the Markdown
    file, and never leave Markdown during the entire enterprise. It’s
    not usually appropriate to report results that include imputation in
    a Table 1, so I expect the best choice is to build a note specifying
    the amount of missing data.
3.  Some variables will present as characters in the data if you import
    it as I did above, but you’d instead prefer them to appear as
    **factors**. Be sure to include code in your response to make these
    changes (the `forcats` package is your friend here,) and then
    (perhaps using the `fct_relevel` function in the `forcats` package)
    be sure to move the levels of those factors into an order that
    facilitates interpretation.
4.  Be sure, too, to make reasoned choices about whether means and
    standard deviations or instead medians and quartiles are more
    appropriate displays for the quantitative variables, and whether or
    not to use exact tests for categorical ones. Include your reasons in
    your bulleted list of footnotes at the end of your table.
5.  Note that body mass index (BMI) and BMI category are not supplied in
    the data, although you do have height and weight. **So, you’ll have
    to calculate the BMI and add it to the data set.** If you don’t know
    the formula for BMI, you have Google to help you figure it out.
6.  For BMI categories, use the four groups specified in the [How is BMI
    interpreted for Adults section of this
    description](https://www.cdc.gov/healthyweight/assessing/bmi/adult_bmi/index.html)
    of Adult BMI by the Centers for Disease Control. **Again, you’ll
    need to use your calculated BMI values and then create the
    categories in your data set, and you’ll need to figure out a way to
    accurately get each subject into the correct category.**
7.  Do not include R output without complete sentences describing what
    you are doing in each step, and what you conclude from that work.

## Question 2. (25 points)

Now, look at the complete data, describing practices A, B, C and D. Does
which **insurance** status a person has seem to have a meaningful impact
on their **systolic blood pressure**, adjusting for whether or not they
are on a **blood pressure medication**? Decide whether your model should
include an interaction term sensibly, and then fit your choice of model
and interpret and display the coefficients and other findings carefully.
Be sure to provide a written explanation of your findings, in complete
sentences. Responses without graphs are not complete.

1.  As a hint, one graph you might use would be one to assess the need
    for an interaction term. Another graph of value would provide
    insight into the relationship between **insurance** and **blood
    pressure medication** status.
2.  Do not include R output without complete sentences describing what
    you are doing in each step, and what you conclude from that work.

## Question 3. (25 points)

How does the sage advice provided by George Box (and echoed by David
Spiegelhalter, especially in Chapter 5 of *The Art of Statistics*) that
“all models are wrong, but some are useful” apply to the results you
have obtained in Question 2? Write an essay of 150-250 words (using
complete sentences, and examples derived from your modeling) that
explains how this advice is connected to your thinking about presenting
your results.

## Please add the session information.

Finally, at the end of this homework and all subsequent assignments
(including the projects), please add the session information. My
preferred way for you to do this is…

``` r
sessioninfo::session_info()
```

### End of Homework 1
