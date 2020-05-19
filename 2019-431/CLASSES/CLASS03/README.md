# 431 Fall 2019 Class 03: 2019-09-03

## Today's Slides

- Class 3 slides are available in [PDF format](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS03/431_class-03-slides_2019.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/CLASSES/CLASS03/431_class-03-slides_2019.Rmd) above. We followed these closely in the live coding in RStudio Cloud.
- Audio recordings of all Classes are posted to http://bit.ly/431-2019-audio as they become available.
    - Someone asked about this: we provide audio recordings for all classes, but not video.
- To get help, [visit TA office hours](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours), visit with Dr. Love before or after class, or email `431-help at case dot edu`. Thanks!

## Upcoming Deliverables

1. Please [join the RStudio Cloud](http://bit.ly/431-2019-join-cloud) as soon as possible. Visit http://bit.ly/431-2019-join-cloud to do so.
    - One of the best parts of RStudio Cloud is the set of primers available there. We heartily recommend **all of them** for those of you who have specific areas where you're looking for help.
2. At http://bit.ly/431-2019-minute-03 is a *Minute Paper*, as there will be most weeks. Please [submit the form](http://bit.ly/431-2019-minute-03) by 2 PM on Wednesday **2019-09-04** for class participation credit. It is designed to take no more than 5 minutes, and ideally you would fill this out immediately after class. 
    - Completing the form boosts your Class Participation grade, which starts at 60% and increases through the semester.
    - It will ask you whether you've joined the RStudio Cloud, and if so, it will ask for your RStudio Cloud user name.
3. [Homework B](https://github.com/THOMASELOVE/2019-431/tree/master/HOMEWORK/B) is due on Friday 2019-09-06 at 2 PM.

## Get help at any time by emailing **431-help at case dot edu**.

1. Apply the 15-minute rule. If you can't solve a problem in 15 minutes, **ask for help** either from us or from Google.
    - You are **absolutely supposed** to use Google and the TAs (and Dr. Love) to improve your code.
2. When asking for help with an R problem from **431-help at case dot edu**, we ask you to try to make it easier for us to help you. Specifically...
    - attach a copy of the R Markdown file you are working on, (or better still, point us to it on RStudio Cloud.)
    - include a screenshot or copy-and-paste listing of the error you are generating, if that's the problem.
    - attach a copy of the data set (if it's not about a homework assignment or other data set that we gave you),
    - attach a copy of the HTML result (if you can create it).

With the R Markdown file, and a detailed explanation of the problem you see, we can often solve the problem in a single email. Without the R Markdown file, we can rarely do anything except ask more questions.

3. When you get a response from one of us on **431-help at case dot edu** you'll notice we REPLY ALL so that all of the TAs (and Dr. Love) can see the result. If you need to respond, please fight your usual urge and **REPLY ALL** as well so that we can all still help. You want to be sure that `431-help at case dot edu` is in the list of recipients of each of your emails, even though replies will come from individuals.

4. The most common problem I see with people using their downloaded version of RStudio is that they need to update their packages, which is something I do at least once a week. Visit the Packages window in RStudio, and click Update.

## Announcements

1. Teaching Assistant Office Hours began this morning and are held in WG-56 (Computing Lab) or WG-67 (Student Lounge) on the ground floor of the Wood building, so be sure to look in both places. The schedule is posted at [the bottom of the Course Calendar](https://github.com/THOMASELOVE/2019-431/blob/master/calendar.md#ta-office-hours).
2. I have changed the name "Deliverables" to "Homeworks" because that's more sensible, but it's an ongoing process.
    - If you find old (or dead) links, please email us at `431-help` for a bit of class participation credit.
    - In a similar vein, Please help us **kill typos**, by emailing 431-help (or Dr. Love directly) whenever and wherever you find them.
3. The [Answer Sketch for Homework A](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/A/post-deadline.md) (formerly called Deliverable A) is now available, in both PDF and R Markdown formats. There was a substantial revision posted Monday evening.
    - You should receive your grades and some feedback on your paragraph from Homework A on Thursday.
    - In Homework A, you answered some questions on a Google Form, too. 
        - Some of the questions were taken from the Attitudes Toward Statistics scale, and those results are now part of [the Answer Sketch](https://github.com/THOMASELOVE/2019-431/blob/master/HOMEWORK/A/post-deadline.md). I also demonstrate some useful early ideas regarding visualizing and summarizing (numerically) a batch of data there.
        - Separately, I've responded to your [comments on the rest of the Homework A Form](http://bit.ly/431-2019-hwa-survey-comments).
4. In our Software materials (also Data and Code) is **Getting Started with R**, available [in R Markdown](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/431-getting-started-with-R.Rmd) and [in PDF](https://github.com/THOMASELOVE/2019-431/blob/master/SOFTWARE/431-getting-started-with-R.pdf) formats. We'll spend a little time with it today, but it's meant to be something you can work through on your own. 
    - This provides a worked example of using R Markdown to process a document (the R Markdown version) into a knitted file (HTML or PDF, for instance) combining results and code.
    - The examples explore (1) some data from an experiment on the growth rate of chickens in response to several different feed supplements, and then (2) some data on the growth of orange trees.
5. I now expect to get complete [Course Project](https://github.com/THOMASELOVE/2019-431/tree/master/PROJECT) information to you by Tuesday 2019-09-10. If you have questions in the interim, please ask them at 431-help.

## Other Things

1. *Numlock* is a daily morning news brief about numbers in the news that sometimes has some interesting stuff. Visit https://numlock.substack.com/subscribe to check it out and sign up to get the emails, if you're interested. There is also a paid subscription option if you're interested.
    - In this morning's issue (2019-09-03), I read about [X-rays](https://undark.org/article/problem-mris-lower-back-pain/) (Americans spend $100 billion on diagnostic imaging each year, but lots of that is unnecessary, and 80 medical societies have called out 540 wasteful interventions (many for low back pain) that led to $241 billion in wasted over-treatment) and [Weight Loss Surgery](https://www.bloomberg.com/news/articles/2019-09-02/for-diabetics-weight-loss-surgery-slashes-the-risk-of-death?srnd=premium) (2287 patients with diabetes at the Cleveland Clinic from 1998-2017 who had surgery were compared to 11435 who didn't. After 8 years, the chance of dying was reduced by 41% among patients with diabetes who pursued the suregery, and the risk of heart or kidney disease fell roughly 60%. 48% of people who didn't have the surgery had a serious complication, as compared to 31% of those who had the surgery.)
    - Other topics this morning included: (1) Box office in China and the success of the film *Ne Zha* there, (2) Wealth in the US (the top 1% hold $30 trillion, the next 9% hold $40 trillion, and the remaining 90% hold the remaining $30 trillion,) and this inequality has worsened substantially from 2007 to 2016, (3) Taylor Swift's latest album sold 27% of all albums sold in the US last week, (4) Ryan Kaji's Toy Review Videos, which suggests that for kids ages 6-8 in the UK, Ryan is 1.75 times as popular as Disney, and that his YouTube videos earned $22.5 million last year, (5) a company made hornless cows by swapping out 200 genetic letters but (it seems) also added genetic material from antibiotic-resistant lab material in the process, and (6) high school sports costs more than ever before, but the rate of Division I college athletes that are first generation college students has dropped a lot in the past few years.
2. You may also be interested in *Significant Digits* from FiveThirtyEight - it's one of the newsletters at https://fivethirtyeight.com/newsletter/ - they also have a weekly newsletter which I subscribe to, along with other more specialized pieces.
    - Today, the digest included stories about 13,000 homes severely damaged by Hurricane Dorian, 45 years of age (and its association with fast-growing start-up companies), the $90 million DoorDash, Uber and Lyft are spending in California to get around a bill that would make them treat their workers as employees, No. 1 seeds at the U.S. Open, 65 cliche-riddled college football fight songs, and 13 straight weekends of protest in Hong Kong.
3. Someone asked "Have you ever been called Dr. Strangelove?" I am torn as to the best reply (other than "not yet".)
    - "You can’t fight in here. This is a war room."
    - Love is something of a strange name to grow up with, certainly, or at least it was in the US in the 1970s, but it’s a good thing to be named for. 
    - From http://howmanyofme.com/search/, there are 663 people in the U.S. named Thomas Love.
    - The most famous Thomas E. Love is the [billionaire owner and founder of Love’s Travel Stops and Country Stores](https://en.wikipedia.org/wiki/Tom_Love). No relation, that I know of.
4. Someone asked "I just wonder why do people use R very much in stats and not matlab and python." 
    - R is designed and maintained for data science and statistics, mainly. 
    - Python, for instance, is a very appealing general purpose programming language. It's not a competition. In class, I want you to demonstrate your facility with R, but in life, use what works.

![](https://github.com/THOMASELOVE/links_teaching/blob/master/images/2017-06-30_bryan.png)
- Source: Jenny Bryan [@JennyBryan 2017-06-30](https://twitter.com/jennybryan/status/880922371225288709)

## One Last Thing

- Do you know about [RStudio Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)?
