431 Project Advice: Combining Data Sets
================
Thomas E. Love
2019-10-29

# This Example

To try to help you, I'm sharing the approach I used to merge data last year, when I also had five files, called 

- `sur2018_01.csv`, which contained items 0 - 20 for the first 25 respondents (ID01 - ID39)
- `sur2018_02.csv`, which contained items 0 - 20 for the remaining 24 respondents (ID41 - ID99)
- `sur2018_03.csv`, which contained items 0 and 21 - 90 for all 49 respondents (ID01 - ID99)
- `sur2018_04.xls`, which is an **Excel** (`.xls`) file (and not our usual `.csv` text file) containing data on items 0 and 91 - 156 and the scales for the first 25 respondents (ID01 - ID39)
- `sur2018_05.xls`, which is an Excel file containing data on items 0, 91 - 156 and the scales for the remaining 24 respondents (ID41 - ID99)

I'm just showing you what I did last time, so I'm not sharing the data files. Instead, adjust these instructions to work with the needs of your 2019 data, as all of the commands you'll need to use are present here.

# R Packages We’ll Use

I’ll load two packages to do this work.

``` r
library(readxl)
library(tidyverse)
```

# Read in the data

## Read in the data from the comma-separated text (`.csv`) files

Note that I’m using `read_csv` here deliberately, rather than any other
approach. This will make the merging easier later, even though it will
leave us with the problem of (eventually) changing the class of many
variables from `character` to `factor`.

  - Note that I used `message = FALSE` in this chunk heading to suppress
    some very detailed (but not critical for us to look at) output.

<!-- end list -->

``` r
surv2018_01 <- read_csv("surv2018_01.csv")
surv2018_02 <- read_csv("surv2018_02.csv")
surv2018_03 <- read_csv("surv2018_03.csv")
```

Each of these results in a `tibble` of data. The numbers of rows and
columns in each of these can be obtained, to check your work so far.

``` r
dim(surv2018_01)
```

    [1] 25 19

``` r
dim(surv2018_02)
```

    [1] 24 19

``` r
dim(surv2018_03)
```

    [1] 49 70


## Read in the data from the Excel files

Note that I’m using `read_xls` here, which is part of the `readxl`
package, which is why I loaded that earlier. This will make the merging
with the things I’ve already created easier later, even though it will
also leave us with the problem of (eventually) changing the class of
many variables from `character` to `factor`.

  - Note that I had to specify here that a value of either a blank or
    `NA` in the Excel sheet means “missing”, which I didn’t have to do
    for `read_csv`. `read_csv`, by default, recognizes both blank cells
    and NA cells as missing, but `read_xls` only recognizes blanks by
    default. 
  - Note also that since you have no missing data in our 2019 survey, 
    this will be a little simpler.
  - Note that I again used `message = FALSE` in this chunk heading to
    suppress some very detailed (but not critical for us to look at)
    output.

<!-- end list -->

``` r
surv2018_04 <- read_xls("surv2018_04.xls", na = c("", "NA"))
surv2018_05 <- read_xls("surv2018_05.xls", na = c("", "NA"))
```

Each of these results in a `tibble` of data. The numbers of rows and
columns in each of these can be obtained, to check your work so far.

``` r
dim(surv2018_04)
```

    [1] 25 78

``` r
dim(surv2018_05)
```

    [1] 24 78

Make sure that your dimensions match mine.

# Merge the tibbles you have created

## Merge the data in `surv2018_01` with `surv2018_02`, forming `temp12`

This next bit of code will produce a data frame containing what we need
from data sets 1 and 2, putting together the first 25 respondents (in
`surv2018_01`) and the remaining 24 (in `surv2018_02`) all together.
Since `surv2018_01` and `surv2018_02` contain the same columns of
information, and just different rows, we can do this easily with the
`bind_rows` function from the `tidyverse`.

Again, I’ll output the dimensions of the result, so that we can check
that you and I get the same results.

``` r
temp12 <- bind_rows(surv2018_01, surv2018_02)

dim(temp12)
```

    [1] 49 19

## Merge the data in `surv2018_04` with `surv2018_05`, forming `temp45`

This will produce a data frame containing what we need from data sets 4
and 5, putting together the first 25 respondents (in `surv2018_04`) and
the remaining 24 (in `surv2018_05`) all together. Since `surv2018_04`
and `surv2018_05` contain the same columns of information, and just
different rows, we can do this easily with the `bind_rows` function from
the `tidyverse`.

As before, I’ll output the dimensions of the result, so that we can
check that you and I get the same results.

``` r
temp45 <- bind_rows(surv2018_04, surv2018_05)
dim(temp45)
```

    [1] 49 78

## Merge the data in `temp12` with `surv2018_03`

This will produce a data frame containing what we need from data sets 1,
2 and 3, all together.

``` r
temp123 <- left_join(temp12, surv2018_03, by = "response_id")
dim(temp123)
```

    [1] 49 88

## Merge the data in `temp123` and `temp45`

This will produce a data frame containing what we need from data sets 1,
2, 3, 4 and 5 all together.

``` r
temp12345 <- left_join(temp123, temp45, by = "response_id")
dim(temp12345)
```

    [1]  49 165

# Create the `surv2018_full` tibble we all need

## Create the `surv2018_full` tibble

Here, we change all of the variables of “character” class to factor so
they will do what we expect in analyses, and then back out of that for
`response_id` which we’d like to keep as a “character”.

``` r
surv2018_full <- temp12345 %>%
    mutate_if(is.character, funs(as.factor(.))) %>%
    mutate(response_id = as.character(response_id))
```

## Remove the temporary data sets you built from your environment

``` r
rm(temp12, temp45, temp123, temp12345)
```

## Remove the raw data sets you initially imported from your environment

``` r
rm(surv2018_01, surv2018_02, surv2018_03, surv2018_04, surv2018_05)
```

We won’t need these again. 

The last step for you is to be sure that your data matches the results 
I have provided in the Codebook when you run `Hmisc::describe()` and, 
if so, you're all set.
