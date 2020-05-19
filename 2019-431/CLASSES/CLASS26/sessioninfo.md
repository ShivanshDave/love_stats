Dr. Love’s Session Information for Quiz 3
================

``` r
knitr::opts_chunk$set(comment = NA)
```

``` r
library(broom); library(car); library(Epi)
library(exact2x2); library(here); library(janitor)
library(magrittr); library(patchwork); library(PropCIs)
library(vcd); library(sessioninfo)
library(tidyverse)
```

``` r
session_info()
```

    - Session info ---------------------------------------------------------------
     setting  value                       
     version  R version 3.6.1 (2019-07-05)
     os       Windows 10 x64              
     system   x86_64, mingw32             
     ui       RTerm                       
     language (EN)                        
     collate  English_United States.1252  
     ctype    English_United States.1252  
     tz       America/New_York            
     date     2019-12-04                  
    
    - Packages -------------------------------------------------------------------
     package     * version    date       lib source        
     abind         1.4-5      2016-07-21 [1] CRAN (R 3.6.0)
     assertthat    0.2.1      2019-03-21 [1] CRAN (R 3.6.1)
     backports     1.1.5      2019-10-02 [1] CRAN (R 3.6.1)
     broom       * 0.5.2      2019-04-07 [1] CRAN (R 3.6.1)
     car         * 3.0-5      2019-11-15 [1] CRAN (R 3.6.1)
     carData     * 3.0-3      2019-11-16 [1] CRAN (R 3.6.1)
     cellranger    1.1.0      2016-07-27 [1] CRAN (R 3.6.1)
     cli           1.1.0      2019-03-19 [1] CRAN (R 3.6.1)
     cmprsk        2.2-9      2019-10-09 [1] CRAN (R 3.6.1)
     colorspace    1.4-1      2019-03-18 [1] CRAN (R 3.6.1)
     crayon        1.3.4      2017-09-16 [1] CRAN (R 3.6.1)
     curl          4.3        2019-12-02 [1] CRAN (R 3.6.1)
     data.table    1.12.6     2019-10-18 [1] CRAN (R 3.6.1)
     DBI           1.0.0      2018-05-02 [1] CRAN (R 3.6.1)
     dbplyr        1.4.2      2019-06-17 [1] CRAN (R 3.6.1)
     digest        0.6.23     2019-11-23 [1] CRAN (R 3.6.1)
     dplyr       * 0.8.3      2019-07-04 [1] CRAN (R 3.6.1)
     Epi         * 2.40       2019-11-25 [1] CRAN (R 3.6.1)
     etm           1.0.5      2019-05-28 [1] CRAN (R 3.6.1)
     evaluate      0.14       2019-05-28 [1] CRAN (R 3.6.1)
     exact2x2    * 1.6.3.1    2019-10-16 [1] CRAN (R 3.6.1)
     exactci     * 1.3-3      2017-10-02 [1] CRAN (R 3.6.0)
     forcats     * 0.4.0      2019-02-17 [1] CRAN (R 3.6.1)
     foreign       0.8-72     2019-08-02 [1] CRAN (R 3.6.1)
     fs            1.3.1      2019-05-06 [1] CRAN (R 3.6.1)
     generics      0.0.2      2018-11-29 [1] CRAN (R 3.6.1)
     ggplot2     * 3.2.1      2019-08-10 [1] CRAN (R 3.6.1)
     glue          1.3.1      2019-03-12 [1] CRAN (R 3.6.1)
     gtable        0.3.0      2019-03-25 [1] CRAN (R 3.6.1)
     haven         2.2.0      2019-11-08 [1] CRAN (R 3.6.1)
     here        * 0.1        2017-05-28 [1] CRAN (R 3.6.1)
     hms           0.5.2      2019-10-30 [1] CRAN (R 3.6.1)
     htmltools     0.4.0      2019-10-04 [1] CRAN (R 3.6.1)
     httr          1.4.1      2019-08-05 [1] CRAN (R 3.6.1)
     janitor     * 1.2.0      2019-04-21 [1] CRAN (R 3.6.1)
     jsonlite      1.6        2018-12-07 [1] CRAN (R 3.6.1)
     knitr         1.26       2019-11-12 [1] CRAN (R 3.6.1)
     lattice       0.20-38    2018-11-04 [2] CRAN (R 3.6.1)
     lazyeval      0.2.2      2019-03-15 [1] CRAN (R 3.6.1)
     lifecycle     0.1.0      2019-08-01 [1] CRAN (R 3.6.1)
     lmtest        0.9-37     2019-04-30 [1] CRAN (R 3.6.1)
     lubridate     1.7.4      2018-04-11 [1] CRAN (R 3.6.1)
     magrittr    * 1.5        2014-11-22 [1] CRAN (R 3.6.1)
     MASS          7.3-51.4   2019-03-31 [1] CRAN (R 3.6.1)
     Matrix        1.2-17     2019-03-22 [2] CRAN (R 3.6.1)
     mgcv          1.8-28     2019-03-21 [2] CRAN (R 3.6.1)
     modelr        0.1.5      2019-08-08 [1] CRAN (R 3.6.1)
     munsell       0.5.0      2018-06-12 [1] CRAN (R 3.6.1)
     nlme          3.1-140    2019-05-12 [2] CRAN (R 3.6.1)
     numDeriv      2016.8-1.1 2019-06-06 [1] CRAN (R 3.6.0)
     openxlsx      4.1.3      2019-11-07 [1] CRAN (R 3.6.1)
     patchwork   * 1.0.0      2019-12-01 [1] CRAN (R 3.6.1)
     pillar        1.4.2      2019-06-29 [1] CRAN (R 3.6.1)
     pkgconfig     2.0.3      2019-09-22 [1] CRAN (R 3.6.1)
     plyr          1.8.4      2016-06-08 [1] CRAN (R 3.6.1)
     PropCIs     * 0.3-0      2018-02-23 [1] CRAN (R 3.6.0)
     purrr       * 0.3.3      2019-10-18 [1] CRAN (R 3.6.1)
     R6            2.4.1      2019-11-12 [1] CRAN (R 3.6.1)
     Rcpp          1.0.3      2019-11-08 [1] CRAN (R 3.6.1)
     readr       * 1.3.1      2018-12-21 [1] CRAN (R 3.6.1)
     readxl        1.3.1      2019-03-13 [1] CRAN (R 3.6.1)
     reprex        0.3.0      2019-05-16 [1] CRAN (R 3.6.1)
     rio           0.5.16     2018-11-26 [1] CRAN (R 3.6.1)
     rlang         0.4.2      2019-11-23 [1] CRAN (R 3.6.1)
     rmarkdown     1.18       2019-11-27 [1] CRAN (R 3.6.1)
     rprojroot     1.3-2      2018-01-03 [1] CRAN (R 3.6.1)
     rstudioapi    0.10       2019-03-19 [1] CRAN (R 3.6.1)
     rvest         0.3.5      2019-11-08 [1] CRAN (R 3.6.1)
     scales        1.1.0      2019-11-18 [1] CRAN (R 3.6.1)
     sessioninfo * 1.1.1      2018-11-05 [1] CRAN (R 3.6.1)
     ssanv       * 1.1        2015-06-23 [1] CRAN (R 3.6.0)
     stringi       1.4.3      2019-03-12 [1] CRAN (R 3.6.0)
     stringr     * 1.4.0      2019-02-10 [1] CRAN (R 3.6.1)
     survival      3.1-8      2019-12-03 [1] CRAN (R 3.6.1)
     tibble      * 2.1.3      2019-06-06 [1] CRAN (R 3.6.1)
     tidyr       * 1.0.0      2019-09-11 [1] CRAN (R 3.6.1)
     tidyselect    0.2.5      2018-10-11 [1] CRAN (R 3.6.1)
     tidyverse   * 1.3.0      2019-11-21 [1] CRAN (R 3.6.1)
     vcd         * 1.4-4      2017-12-06 [1] CRAN (R 3.6.1)
     vctrs         0.2.0      2019-07-05 [1] CRAN (R 3.6.1)
     withr         2.1.2      2018-03-15 [1] CRAN (R 3.6.1)
     xfun          0.11       2019-11-12 [1] CRAN (R 3.6.1)
     xml2          1.2.2      2019-08-09 [1] CRAN (R 3.6.1)
     yaml          2.2.0      2018-07-25 [1] CRAN (R 3.6.0)
     zeallot       0.1.0      2018-01-28 [1] CRAN (R 3.6.1)
     zip           2.0.4      2019-09-01 [1] CRAN (R 3.6.1)
     zoo           1.8-6      2019-05-28 [1] CRAN (R 3.6.1)
    
    [1] C:/Users/Thomas/Documents/R/win-library/3.6
    [2] C:/Program Files/R/R-3.6.1/library
