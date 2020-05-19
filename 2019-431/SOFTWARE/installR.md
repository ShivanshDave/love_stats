# Installing R and RStudio for 431 in Fall 2019

There will be many people in the course for whom R is a new experience. We assume no prior R work in the course. You will know a fair amount of R (and some other things, too) after taking the course, though.

## R, RStudio and R Packages

The steps here involve:

1. Installing R
2. Installing RStudio
3. Installing a series of R packages so we can more successfully use R.
4. Install some data and code specific to 431.

You'll need to install these programs on either a Windows PC, or Macintosh PC (or, if you are adventurous and self-supporting, a Linux box). They cannot be run in the way we need them on an iPad or Android tablet or on a Chromebook.

### What is R?

R is a freely available computer language and environment for statistical computing and graphics, available for Windows PCs and for Macintosh. The R Project's [Frequently Asked Questions page](https://cran.r-project.org/faqs.html) is some help, but a very dry read.

### What is RStudio?

RStudio is an integrated development environment for R, that includes a number of useful tools that will help us develop our R code and produce useful results. We'll use the (free) Desktop version of RStudio.

### What is an R Package?

An R package is a collection of functions, data, and documentation that extends the capabilities of base R. Using packages is key to the successful use of R.

### Versions and Upgrading

We highly recommend you install R version 3.6.1 (or later) and RStudio version 1.2.1335 (or later). If you have a pre-existing installation of R and/or RStudio, we highly recommend that you reinstall both and get as current as possible. 

You are welcome to install the [preview version of RStudio](https://www.rstudio.com/products/rstudio/download/preview/) if you like, to get the coolest new features, but Dr. Love will stick to the [official release](https://www.rstudio.com/products/rstudio/download/#download) in his work for this class.

# Step-by-Step Installation of R, RStudio and R Packages

## Instructions for Windows Machines

### Windows: Installing R

1.  Close all other programs and point your Internet browser to https://cran.case.edu/.
    -   Try https://cloud.r-project.org/ if the Case site is busy or slow to respond. That link automatically chooses a fast, nearby mirror for you.
    
2.  In the **Download and Install R** box of precompiled binary distributions, click on **Download R for Windows**.

3.  Select the **base** subdirectory on the next screen, to install R for the first time.

4.  You will then see a link to **Download R 3.x.x for Windows**. (As I write, we're on version `3.6.1` but you may see a later version number.) Select this link, and, if given the option, **save** the resulting file.

5.  Once R has downloaded, close all other programs (including your browser), then double-click the downloaded file and follow the instructions to start the setup process.

6.  During the setup, click **Yes** when asked if you want a **customized startup** and select **SDI** (separate windows) instead of MDI (one big window.) Otherwise, select all of the default options.

7.  This will (eventually) produce an icon labeled R on your desktop that says something like **R i386 3.x.x** (32-bit R) or **R x64 3.x.x** (64-bit R) or (and this is most common) both icons. It doesn't matter to me whether you use 32-bit or 64-bit R, and the setup program should automatically identify the better choice for your machine.

8.  Once you see the R icon on your desktop, you are ready to install **RStudio**.

### Windows: Installing RStudio

1.  Close all other programs and point your browser to the download page for the desktop version of RStudio, at https://www.rstudio.com/products/rstudio/download/#download
    - If you prefer, you can instead [download the preview version](https://www.rstudio.com/products/rstudio/download/preview/) so as to be able to take advantage of the latest and greatest things available from RStudio. This isn't necessary for our course, though.

2.  R Studio will display a link to **Desktop Version Installers**. Select the version of R Studio (likely to be `1.2` followed by some additional numbers, at the moment it is `1.2.1335` but you may see a later number) which is recommended for your operating system (most probably this is **Windows 7+** and is listed at the top. Click to download.

3.  Once the package has been downloaded to your desktop, close all other programs (including your browser), then double-click the package, and follow the instructions to start the setup process.

4.  Accept all default settings, and when your machine is done, you should now have an icon on your desktop (and an available program) labeled RStudio.

5.  Double-click on the R Studio icon to open it. This will connect your newly installed R to R Studio, and you will be ready to install some **R packages**.

### Windows: Installing R Packages

1.  Now, you're ready to install some of the packages you will need. Visit our [Packages page](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/PACKAGES.md) for an up-to-date list of the R packages we are using in this course, and complete installation instructions. 

### Windows: Install Data and Code for 431

1.  Exit R Studio, being sure to agree that the workspace should be saved if you are asked, and then open a browser to our [Data page](https://github.com/THOMASELOVE/2019-431-data).

2.  Click on the green **Clone or download** button.

3.  Select Download ZIP on the bottom right, and this will download a zip file of relevant data and code for the course. Put this in a directory you can find later.

4.  You should now be all set! Our discussion of R, RStudio, working with data, scripts and Markdown files continues elsewhere.

## Instructions for Apple / Macintosh Machines

### Mac: Installing R

1.  Close all other programs and point your Internet browser to https://cran.case.edu/.
    -   Try https://cloud.r-project.org/ if the Case site is busy or slow to respond. That link automatically chooses a fast, nearby mirror for you.

2.  In the **Download and Install R** box of precompiled binary distributions, click on **Download R for (Mac) OS X**.

3.  Click on the package containing the latest version (most likely **R-3.x.x.pkg**, where the version as of `Sys.Date()` is `3.6.1`, but you may see a later number) on the next screen. Download the package, to install R for the first time.

4.  Follow the installation instructions, and select all of the default options.

5.  Eventually, your Mac will tell you that the installation was successful. Hit **Close**.

6.  You can check to see that the installation worked, if you like, by looking for the R (and, likely, R64) programs under the Launchpad. But you shouldn't have a problem. You should now be ready to install **R Studio**.

### Mac: Installing RStudio

1.  Close all other programs and point your browser to the download page for the desktop version of RStudio, at https://www.rstudio.com/products/rstudio/download/#download
    - If you prefer, you can instead [download the preview version](https://www.rstudio.com/products/rstudio/download/preview/) so as to be able to take advantage of the latest and greatest things available from RStudio. This isn't necessary for our course, though.

2.  R Studio will display a link to **Desktop Version Installers**. Select the version of RStudio (likely to be `1.2` followed by some additional numbers, at the moment it is `1.2.1335` but you may see a later number) which is recommended for your operating system (most probably this is **macOS 10.12+** and is listed near the top. Click to download.

3.  Once the package has been downloaded to your desktop, double-click on the download to show the folder where the `.dmg` file was placed. Then double-click it to install RStudio.

4.  Click on the R Studio icon (when it appears) to open it. This will connect your newly installed R to R Studio, and you will be ready to install some **R packages**.

### Mac: Installing R Packages

1.  Now, you're ready to install some of the packages you will need. Visit our [Packages page](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/PACKAGES.md) for an up-to-date list of the R packages we are using in this course, and complete installation instructions. 

### Mac: Install Data and Code for 431

1.  Exit R Studio, being sure to agree that the workspace should be saved if you are asked, and then open a browser to our [Data page](https://github.com/THOMASELOVE/2019-431-data).

2.  Click on the green **Clone or download** button.

3.  Select Download ZIP on the bottom right, and this will download a zip file of relevant data and code for the course. Put this in a directory you can find later.

4.  You should now be all set! Our discussion of R, R Studio, working with data, scripts and Markdown files continues elsewhere.




