# R Packages in 431

Note that these package instructions should be used after you've [followed these instructions and installed R and R Studio](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/installR.md).

## Installing All Necessary R Packages (Do once, at the start of the semester)

1. Copy and paste the following two lines of code into the **Console** window of R Studio to install the packages you'll need for this course.

<!-- -->

    pkgs <- c("aplpack", "arm", "babynames", "boot", "broom", "car", "cowplot", 
            "DataExplorer", "devtools", "Epi", "exact2x2", "faraway", "fivethirtyeight", 
            "foreign", "gapminder", "GGally", "ggforce", "ggridges", "gridExtra", "here", 
            "Hmisc", "infer", "janitor", "kableExtra", "knitr", "lme4", "magrittr", 
            "markdown", "MASS", "mice", "mosaic", "multcomp", "naniar", "NHANES", "pander", 
            "PropCIs", "psych", "pwr", "qcc", "rmarkdown", "rmdformats", "rms", 
            "sandwich", "simputation", "skimr", "survival", "tableone", 
            "tidyverse", "vcd")

    install.packages(pkgs)

2.  Execute those commands by hitting Enter.

3.  Now, add the `patchwork` package (which is not available on CRAN) by typing:

<!-- -->

    devtools::install_github("thomasp85/patchwork")

4.  Now, go to the **Packages** tab on the right side of your screen, and click on **Update**. 

5.  This will bring up a dialog box. I usually click **Select All**, then click **Install Updates**. 

    - A popup box may appear, asking "Do you want to install from sources the packages which need compilation?" to which I usually answer **No**. A **Yes** response leads to a slower installation, but can solve problems if you still have them after updating.
    - This may take a few minutes. As long as you're seeing activity in the Console window, things are progressing.
    - Eventually, you'll get a message that "The downloaded source packages are in ..." with a directory name. That's the sign that the updating is done.

6.  Finally, choose **File ... Quit Session** from the top menu, and accept R Studio's request to save your workspace. This will eliminate the need to re-do these steps every time you work in R.

### Note: A Windows Issue

If you are using Windows, and get messages during installation that the latest version of RTools needs to be installed, you can usually just ignore them. If you don't want to ignore them, [go here to download and install RTools](https://cran.r-project.org/bin/windows/Rtools/) for Windows.

## Installing a Single Package

If you want to install a single package, you can do so by finding the word **Packages** on the right side of your screen. 

1. Click on the **Packages** tab on the right side of your screen to start installing the packages you'll need. 
2. Click **Install**, which will bring up a dialog box, where you can type in the names of the packages that you need. These should be separated by a space or comma. Be sure to leave the Install dependencies box checked.
    - A popup box may appear, asking "Do you want to install from sources the packages which need compilation?" to which I usually asnwer **No**. A **Yes** response leads to a slower installation, but can solve problems if you still have them after updating.
    - This may take a few minutes. As long as you're seeing activity in the Console window, things are progressing.
    - Eventually, you'll get a message that "The downloaded source packages are in ..." with a directory name. That's the sign that the updating is done.


## Updating Your Packages (About once per week)

You should update your R packages about once a week, and also whenever you encounter a problem in R that you can't solve otherwise.

1.  Select the **Packages** tab on the right side of your screen, and click on **Update**. 

2.  This will bring up a dialog box. I usually click **Select All**, then click **Install Updates**. 

    - A popup box may appear, asking "Do you want to install from sources the packages which need compilation?" to which I usually asnwer **No**. A **Yes** response leads to a slower installation, but can solve problems if you still have them after updating.
    - This may take a few minutes. As long as you're seeing activity in the Console window, things are progressing.
    - Eventually, you'll get a message that "The downloaded source packages are in ..." with a directory name. That's the sign that the updating is done.

