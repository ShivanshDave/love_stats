# Things I Won't Get to in 432 This Semester (Spring 2020)

## Other Logistic Regression Methods

One of the many things I'm not going to get to this semester is the notion of **exact logistic regression**, which is an idea that is could be used to build models when some combinations of an outcome and a categorical predictor do not occur in the data ("separation"), but which is extremely computationally intensive and I've only actually done it with very small problems.

One good old example of doing exact logistic regression using R and the `elrm` package is [found here at UCLA](https://stats.idre.ucla.edu/r/dae/exact-logistic-regression/), but it's a limited tool.

I might suggest that instead using **penalized maximum likelihood logistic regression using the Firth method** and the `logistf` package may be more suitable, especially if your data display "separation" as identified above. [Here's a YouTube Video](https://www.youtube.com/watch?v=fVbrUz6V_uk), and here's [an example using Firth logistic regression](https://www.r-bloggers.com/example-8-15-firth-logistic-regression/).

## Censored and Truncated Regression

The Course Notes talk a bit about tobit regression, but you may also be interested in UCLA's examples for [tobit regression](https://stats.idre.ucla.edu/r/dae/tobit-models/), [truncated regression](https://stats.idre.ucla.edu/r/dae/truncated-regression/) and [interval regression](https://stats.idre.ucla.edu/r/dae/interval-regression/).

## Geographic Data Analysis, Visualization and Modeling

- I recommend [Geocomputation with R](https://geocompr.robinlovelace.net/) by Robin Lovelace, Jakub Nowosad and Jannes Muenchow
- I also strongly recommend the [sociome package](https://github.com/NikKrieger/sociome) written by Nik Krieger (a graduate of this class) to help researchers to operationalize social determinants of health data.

## Time Series Models and Forecasting

By far the best source on the subject in my view is Rob Hyndman and George Athanasopoulos' Forecasting: Principles and Practice book, at https://otexts.com/fpp2/.

## Text Analysis and Text Mining

I recommend [Text Mining with R: A Tidy Approach](https://www.tidytextmining.com/) by Julia Silge and David Robinson

## Using tidymodels instead of caret

Rebecca Barter has a great post on [tidymodels](http://www.rebeccabarter.com/blog/2020-03-25_machine_learning/) which in some ways is the successor to the `caret` package to help you do machine learning things within the tidyverse. Next year's course will use this approach, certainly. Other key references Rebecca cites include...
    - [A Gentle Introduction to tidymodels](https://rviews.rstudio.com/2019/06/19/a-gentle-intro-to-tidymodels/) by Edgar Ruiz
    - Alison Hill's slides on [Introduction to Machine Learning with the Tidyverse](https://education.rstudio.com/blog/2020/02/conf20-intro-ml/).
