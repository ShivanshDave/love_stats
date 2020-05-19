# 431 Fall 2019 Class 17: 2019-10-29

## Today's Slides

- Class 17 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS17/431_class-17-slides_2019.pdf), as well as [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS17/431_class-17-slides_2019.Rmd) above. 
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`.

## Today's Agenda

- Comparing Proportions
    - based on Independent Samples
    - based on Paired Samples

- "[Not Even Scientists Can Easily Explain *p* Values](https://fivethirtyeight.com/features/not-even-scientists-can-easily-explain-p-values/)" from Christie Aschwanden at FiveThirtyEight.

--------------

## Introducing the Course Projects: Part 2 (CLASS 17)

Today, we'll meet the investigators working with data from 500 Cities, CDC Community Health Status Indicators, City Health Dashboard, County Health Rankings, and other government data repositories.

### County Health Rankings projects

Investigator(s) | Title | Outcome | Key Predictor(s)
:-----------------: | :-------------------------: |  :-------------------------: | :-------------------------: 
Wayne Tsuang | Are drug overdose deaths associated with access to prescribing physicians? | Drug Poisoning Death Rate | Residents per Primary Care Provider
Anirudh Kumar and Divyang Patel | Impact of Uninsurance on Alcohol-Impaired Driving Deaths in Texas Counties | Alcohol Related Driving Deaths | % of County that is Uninsured

### Other Government Sources

Investigator(s) | Title | Source | Outcome | Key Predictor(s)
:-----------: | :-------------------: |  :-------------------: | :-------------------: | :-------------------: 
Jing Zhang | Does projected employment change in an occupation influence annual wages? | Bureau of Labor Statistics Occupation Projections | Median Annual Wages in 2018 | Projected Employment % Change from 2018-2028
Jianhong Lin | Studying Osteopathic Physicians in the State of Washington | Washington State Department of Health and healthdata.gov | Total Patient Care Paid Hours | Years in Practice

### CDC Community Health Status Indicators / City Health Dashboard

Investigator(s) | Title | Outcome | Key Predictor(s)
:-----------------: | :-------------------------: |  :-------------------------: | :-------------------------: 
Jason Huang and Yufei Li | Do You Lose Years of Life Due to Obesity? | Average Life Expectancy | Prevalence of Obesity
Abigail Roche | Predicting life expectancy in cities from social, environmental and economic factors | Average Life Expectancy | HHs in the top 20% or bottom 20% of national income distribution

### 500 Cities projects:

Investigator(s) | Title | Outcome | Key Predictor(s)
:-----------------: | :-------------------------: |  :-------------------------: | :-------------------------: 
Victor Zhou | Is insufficient sleep associated with your mental health? | % reporting Mental Health not good for 14 or more of the past 30 days | Sleeping less than 7 hours among adults 18+
Will Wulftange | Exercise and cancer outcomes in adults | % who have been told they have cancer (other than skin) | % with no leisure-time physical activity
Jakob Woerner | Avoiding workouts and negative health outcomes | % who have been told they have high cholesterol | % with no leisure-time physical activity
Claire Sonneborn and Lauren Yeh | Predicting Tooth Loss in America’s 500 Largest Cities | Average No. of Teeth Lost among adults 65+ |  % who lack current health insurance among those 18-64
Erin Cohn and Jessica Scarborough | Does the Head Affect the Heart? Mental Health and Coronary Artery Disease in US Cities | Age-Adjusted "ever been told you have heart disease" | Age-adjusted % reporting Mental Health not good for 14 or more of the past 30 days

## Data Management and the "500 Cities" Data

I've done some things to make the 2018 version of the 500 Cities data easier to work with. I started with the [data download here](https://chronicdata.cdc.gov/500-Cities/500-Cities-Local-Data-for-Better-Health-2018-relea/6vp6-wxuq) and then I:

1. filtered the data to show only the geographic level of a city, rather than a census tract or the US as a whole or anything else. That gets us down to 28,000 rows (500 cities x 56 measurements = 28,000)
2. sorted the rows in a sensible order, first by StateDesc, then CityName, then Category, then MeasureId
3. Added a CityCode column which just runs from C-001 to C-500 in a rational way.
4. filtered the data to choose only the rows that show crude prevalence, rather than age-adjusted prevalence, as indicated in the Data_Value_Type variable which takes the data down to 14,000 rows.
5. changed the name of Measure to LongMeasureName and put it at the end of the file
6. and dropped the columns other than:

Variable | First Row's Value | Last Row's Value
----------: | :------------------------------------------: | :------------------------------------------:
`CityCode` | C-001 | C-500
`StateAbbr` | AL | WY
`StateDesc` | Alabama | Wyoming
`CityName` | Birmingham | Cheyenne
`DataSource` | BRFSS | BRFSS
`Category` | Health Outcomes | Unhealthy Behaviors
`Data_Value_Type` | Crude prevalence | Crude prevalence
`Data_Value` | 29.3 | 33.1
`MeasureId` | ARTHRITIS | SLEEP
`Short_Question_Text` | Arthritis | Sleep <7 hours
`LongMeasureName` | Arthritis among adults aged >=18 Years | Sleeping less than 7 hours among adults aged >=18 Years

and that's the [500-cities-raw-smaller-2018.csv file](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS17/data/500-cities-raw-smaller-2018.csv), which still requires pivoting in R, but is much more manageable than the raw download.

-----------

## Reminder of Upcoming Deadlines

1. There is no Minute Paper after Class 17.
2. [Study A Task 5 (Comparison Plan)](https://thomaselove.github.io/2019-431-project/task5a.html) is due at 2 PM Wednesday 2019-10-30. Details on everything you need to do this are at http://bit.ly/431-2019-studyA-codebook. 16/43 have submitted this form so far. 
    - For two variables to describe paired samples, they need to have the same units of measurement, so that taking a paired difference makes sense. **This is a problem for every single person who's submitted a planned paired samples analysis so far.**
    - The people planning on independent samples had more reasonable ideas, for the most part.
    - I have yet to review anything else submitted by those 16 people.
3. [Homework G](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/G) is due at 2 PM Friday 2019-11-01.
    - In some questions, you may want to modify or collapse levels of a factor. You can learn more about this in [the Modifying Factor Levels section of R for Data Science](https://r4ds.had.co.nz/factors.html#modifying-factor-levels).
4. [Study B Task 4 (Sharing the Raw Data)](https://thomaselove.github.io/2019-431-project/task4b.html) is due on 2019-11-04 at 9 AM via Canvas.
5. [Homework H](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/H) is due at 2 PM Friday 2019-11-08.

Reading: You should be through Silver Chapter 8 now, and through Chapter 11 by 2019-11-12.

- The Project Study A Survey Data will be made available to you on 2019-10-31, and we'll discuss that in Class 18. Everyone has completed Study A Tasks 2, 3, and 4 now.
- [Course Notes](https://thomaselove.github.io/2019-431-book/) were updated a little this weekend. 
    - The most substantial change is that Chapter 29 has a closing subsection devoted to three-way tables now.

## Reactions to the Study B Task 3 Submissions are now fully up to date on Canvas, and below...

1. Dr. Love **requires** a revision on Task 3 for these investigators. Submit it where you submitted the initial Study B Task 3 attempt by **5 PM Wednesday 2019-10-30** after reading the comments on Canvas.

- Rebeka Bordi 
- Anirudh Kumar and Divyang Patel 
- Claire Sonneborn and Lauren Yeh 

2. Dr. Love **does not** require a formal revision on Task 3 for the following people, although there are likely to be comments for them on Canvas that should be followed in subsequent tasks.

No Formal | Revision | of Task 3 | is | necessary.
:----------------------: | :----------------------: | :----------------------: | :----------------------: | :----------------------: 
Hussam Alqahtani and Kimberly Noriega | Ebtesam Alshehri and Carolyn Goldschmidt | Fatima Asad and Basma Dahash | -- | Noah Chernosky 
Erin Cohn and Jessica Scarborough | Sofija Conic | Lauren Cruz | Shivansh Dave and Troy Neptune | Joshua Froess and Rajeev Varkey
Shuai Fu and Dean Pontius | Kieran Gallagher and Corri Sept | Farrah Gao | Ahmet Hacialiefendioglu | Emily Hannon 
George Hoeferlin and Youjoung Kim | Jason Huang and Yufei Li | Lizzie Knauss and Kim Parker | -- | Jianhong Lin 
Shiying Liu and Yiheng Pan | Stephanie Merlino Barr | Anna Miller | Shayan Monabbati | Ryan Moore and Khaled Shorbaji 
Jasmine Olvany | Vineet Punia and Matthew Stewart | Abigail Rippin | Abby Roche | Seth Rotz 
Paola Saroufim | Matt Siuba | -- | Alena Sorensen and Emily Tyszka | Wayne Tsuang 
Vachan Vadmal | Anastasia Vassiliou | Timothy Walker | Jakob Woerner | Stephanie Wood
Will Wulftange | Jing Zhang | Victor Zhou

## In the Project Portfolio (Study A and Study B)

There are some things you'll need to do, and so you might as well get used to them.

1. You will need to use `code-folding: show` and you shouldn't hide any code at all, anywhere. You should hide unnecessary warnings and messages to make your output more attractive, but `echo = FALSE` is not permitted in your project R Markdown work.
2. You must load all of the packages you plan to load at the start of your R Markdown file. 
3. You must present NO code without an explanation, and every bit of your work should be preceded by an appropriate section heading or subheading to form an attractive table of contents.
4. You must use the `here` package and do so appropriately.
5. You must set `comment = NA` as I have done in every bit of R Markdown work I've shown you to date.
6. You must use an actual name (definitely not `data` or `data1` or anything generic like that) for each data set you generate in R.

----------

## One Last Thing

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS17/elitism.PNG)

## Also...

The play I am in, *Noises Off*, opens Friday night at Hudson Players, and will be performed on November 1, 2, 8, 9, 10, 15 and 16. It's suitable for **adult audiences**. For more details or to buy tickets, visit [this link](https://app.arts-people.com/index.php?ticketing=hudpl) or my [theater page](https://github.com/THOMASELOVE/theater).
