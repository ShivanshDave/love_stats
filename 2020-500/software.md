# Software Details for 500  

## The Software You'll Need

The course uses R, R Studio and R Markdown, as were used in 431-432. Get your software up to date on a laptop you can bring to class, for best results. We'll hope you have all of this done before the first class, but if you have problems, we can deal with them at that session. You'll need to have all of this accomplished in order to do your first homework assignment. If you need additional help, we recommend [Dr. Love's 431 instructions](https://github.com/THOMASELOVE/2019-431/tree/master/SOFTWARE), or [these Stat 545 instructions](https://stat545.com/block000_r-rstudio-install.html).

1. Download R (R 3.6.2 or later) from https://cran.case.edu/. R 4.0.0 is expected to be released during the semester.
2. Download R Studio Desktop (open source edition: version 1.2.5033 or later is OK) from https://www.rstudio.com/products/rstudio/download/#download.
3. Install the necessary R software packages we'll use, as listed below.

## R Packages for 500

Copy and paste the following lines of code into the Console window of R Studio to install the packages you'll need for this course.

<!-- -->

    pkgs <- c(  "afex", "aplpack", "arm", "babynames", "boot", "broom", "car", "CBPS", 
                "cobalt", "cowplot", "devtools", "ebal", "Epi", "ez", "faraway", 
                "fivethirtyeight", "foreign", "gapminder", "gee", "geepack", "GGally", 
                "ggforce", "ggrepel", "ggridges", "ggthemes", "glue", "gridExtra", "here", 
                "Hmisc", "infer", "janitor", "knitr", "lars", "lattice", "leaps", "lme4", 
                "lmerTest", "magrittr", "markdown", "MASS", "Matching", "MatchIt", "mice", 
                "mosaic", "multcomp", "naniar", "NHANES", "optmatch", "pander", "patchwork", 
                "pROC", "pscl", "psych", "pwr", "qcc", "QuantPsyc", "rbounds", "rgenoud",
                "rmarkdown", "rmdformats", "rms", "ROCR", "rstanarm", "sandwich", 
                "sessioninfo", "simputation", "skimr", "spelling", "styler", "survey", 
                "survival", "survminer", "tableone", "tidyverse", "twang", "usethis", 
                "vcd", "viridis")

    install.packages(pkgs)

1.  Now, go to the **Packages** tab on the right side of your screen, and click on **Update**. Select and install all available updates.

2.  Finally, choose **File ... Quit R** from the top menu, and accept R Studio's request to save your workspace. This will eliminate the need to re-do these steps every time you work in R.

Note: If you want to install a single package, you can do so by finding the word **Packages** on the right side of your screen. Click on the **Packages** menu to start installing the packages you'll need. Then click **Install**, which will bring up a dialog box, where you can type in the names of the packages that you need. these should be separated by a space or comma. Be sure to leave the Install dependencies box checked.
