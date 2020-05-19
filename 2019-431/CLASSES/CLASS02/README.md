# 431 Fall 2019 Class 02: 2019-08-29

## Today's Slides

- Class 2 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/431_class-02-slides_2019.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/431_class-02-slides_2019.Rmd) if you want to see how I built them. We got through slide 37, essentially, today. I also fixed the typos we'd found. We'll get to the rest coding live in class 3.
- Audio recordings of all Class sessions are posted to http://bit.ly/431-2019-audio. This now includes Class 2. 

## Today's Announcements

1. **First Homework is Due Tomorrow** Your first Homework is due this Friday (tomorrow) 2019-08-30 at 2 PM. [Get started on it now](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/A). 
    - I added a link which should make it possible to complete the work even if you're having trouble using R for some reason.
2. **Audio recordings** If you are interested in or just capable of taking on the task of audio-recording the class, please let Dr. Love know. Thanks.
3. At any time, including now, if you have questions about the course, please ask us at **431-help at case dot edu**. 
4. **TA Office Hours** wil be held in either WG-56 (Computing Lab) or WG-67 (Student Lounge) on the ground floor of the Wood building, so be sure to look in both places. **If you need directions, let us know.** The schedule is now posted to the bottom of the [Course Calendar](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md), and below.

Mondays | Tuesdays | Wednesdays | Thursdays | Fridays
:----------: | :----------: | :----------: | :----------: | :----------: 
11:30 am to 12:45 pm | 11:30 to 12:45 | -- | 11:30 to 12:45 | 11:30 to 12:45
-- | -- | 12:45 pm to 2:00 pm | -- | 12:45 to 2:00
-- | 2:30 pm to 3:45 pm | -- | 2:30 to 3:45 | --
-- | 5:30 pm to 6:45 pm | -- | 5:30 to 6:45 | --

- Note that TA office hours begin Tuesday 2019-09-03, and end on Friday 2019-12-06, and are not held during the week of Thanksgiving. 
- Dr. Love is available to meet with you 15 minutes before class, as well as afterwards, and by appointment. His office is Wood WG-82J. Send him an email to set up an appointment.

## Links for Today 

1. The link to join the RStudio Cloud I've set up is http://bit.ly/431-2019-join-cloud.
2. Prior to the start of class, I asked you to fill out a survey online, at http://bit.ly/431-2019-welcome-survey. Today, we'll spend a little time [working through this summary](https://docs.google.com/document/d/1k5zLv31yDrpLn06F9Wady3wO5VfqXSiytVhrv8TEMwk/edit?usp=sharing), to help set expectations.

During Class 01, we engaged in several data collection activities:

3. You worked with a partner to complete a survey (on paper) that involved 15 questions. I've entered the data in the [`surveyday1_2019.csv` file](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/surveyday1_2019.csv) above, and we'll discuss those data a bit today.
4. Also, we made some group guesses about the age of people in a series of photographs. The data from that activity are now available in the Google Sheet at http://bit.ly/431-2019-day1-ageguess. I've also built a small summary of the data historically in the [`photo-age-history-2019.csv` file](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/photo-age-history-2019.csv).
5. Each of you also made two guesses at my age, which was just over 52.5 years on Tuesday. Those guesses are in the [`love-age-guess-2019.csv` file](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/love-age-guess-2019.csv).


## One Last Thing 

![](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS02/2019-08-24_NYT_fire.png)

- Source: "[What Satellite Imagery Tells Us About the Amazon Rain Forest Fires](https://www.nytimes.com/interactive/2019/08/24/world/americas/amazon-rain-forest-fire-maps.html)" by K. K. Rebecca Lai, Denise Lu and Blacki Migliozzi, at the *New York Times*, 2019-08-24.

### Didn't get to this stuff in Class 01, so it returns

- If you're interested in reading about a scientific model to explain the data analysis process, you might enjoy this article by Hadley Wickham and Garrett Grolemund called [A Cognitive Interpretation of Data Analysis](http://vita.had.co.nz/papers/sensemaking.html).
- Interested in something a little lighter? I recommend these pieces from [FiveThirtyEight](https://fivethirtyeight.com).
    - [We Can Predict Where Measles Will Happen. Why Don’t We?](https://fivethirtyeight.com/features/we-can-predict-where-measles-will-happen-why-dont-we/) by Maggie Koerth-Baker, 2019-06-24.
    - Or maybe [The Browns Are A Hot Super Bowl Pick For 2019. (Wait, What?)](https://fivethirtyeight.com/features/the-browns-are-a-hot-super-bowl-pick-for-2019-wait-what/) from Neal Paine on 2019-07-15.
        - Of course, last year I pointed students to Neal's article entitled: [The Browns’ Suckiness Defies Math And Reason](https://fivethirtyeight.com/features/the-browns-suckiness-defies-math-and-reason/) from 2018-08-20, so there's that.

Enjoy your weekend!
