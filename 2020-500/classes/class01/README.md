# 500 Class 01: 2020-01-16

## Today's Slides

- The slides I'll present in class today are [available in PDF](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/500_2020_slides01.pdf) as well as [in R Markdown](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/500_2020_slides01.Rmd).
- Audio recordings of our classes will be maintained in [this Google Drive folder](http://bit.ly/500-2020-audio).

## What the course is (sort of) about ...

![](https://imgs.xkcd.com/comics/correlation.png)  https://xkcd.com/552/

## Announcements

1. If someone is interested in **audio recording** the class, I would be willing to post those recordings for all to use. Please let me know.

2. Please review [the Google Doc roster](http://bit.ly/500-2020-roster-check) (you'll need to be logged in to Google via your CWRU account) and: 
    - Make sure the information I've provided there is correct and complete. If it's not, edit what you see until it is.
    - Tell me the name by which you want me to call you.
    - Specify your preferred email address.
    - If you're not on the roster, add yourself, please! And let me know.
    - **Click** the Checked? box, please, to indicate that you've checked this over.

3. If you haven't already, please fill out the [Getting To Know You survey](http://bit.ly/500-2020-day1-survey) as soon as you can, please.

4. Check [Canvas](https://canvas.case.edu) to be sure that you are connected to the course, which is likely listed as PQHS 500. If you're not listed, let me know.

## Getting Help

- To get help with the course, email Dr. Love and Mr. Persaud at **500-help at case dot edu**.
- Harry Persaud has agreed to volunteer as a TA for the class this term. Harry will be available to answer questions (mostly about coding in R, propensity scores and data management) either in person (by arrangement) or via email.
- My email address, for personal communication, is `thomas dot love at case dot edu`. 
- *Office Hours*: I'm available after class from 11 - 11:30 at least, either here or in my office Wood WG82-J, but email is otherwise the best way to get help.

## Everything is on the web...

- [Course Home Page](https://github.com/THOMASELOVE/2020-500)
    - Most of the traditional role of a [Syllabus](https://thomaselove.github.io/2020-500-syllabus/) has moved elsewhere, but I still build one.
    - The [Course Calendar](https://github.com/THOMASELOVE/2020-500/blob/master/calendar.md) is the place to go for all deadlines and deliverables information.
    - Details on [Homework](https://github.com/THOMASELOVE/2020-500/tree/master/homework) including "[Homework 0](https://github.com/THOMASELOVE/2020-500/tree/master/homework/hw0)" and [Homework 1](https://github.com/THOMASELOVE/2020-500/tree/master/homework/hw1) due next Thursday.
    - Details on [Observational Studies in Action (OSIA) Assignments](https://github.com/THOMASELOVE/2020-500/tree/master/osia)
    - Details on the [Course Project](https://github.com/THOMASELOVE/2020-500/tree/master/project)
    - [Software page](https://github.com/THOMASELOVE/2020-500/blob/master/software.md), including key R packages 
    - [R-basics Materials](https://github.com/THOMASELOVE/2020-500/tree/master/r-basics)
    - [Sources page](https://github.com/THOMASELOVE/2020-500/tree/master/sources)
    - [Data and Code](https://github.com/THOMASELOVE/500-data) Site
- We're reading Paul Rosenbaum's *Observation and Experiment: An Introduction to Causal Inference*. I'd hope you'd read the Preface and Chapters 1-4 soon, but in particular we'll be discussing Chapters 1 and 2 next time. The readings are scheduled on the [Calendar](https://github.com/THOMASELOVE/2020-500/blob/master/calendar.md).

## Is there more to come?

Yes, mostly in the form of additional slides, and additional coding examples. 

## Today's Extra Reading

- Lucy D'Agostino McGowan wrote [this February 2017 blog post](https://www.kdnuggets.com/2017/02/hill-data-scientist-xkcd-story.html) "[Causation or Correlation: Explaining HIll Criteria using `xkcd`](https://www.kdnuggets.com/2017/02/hill-data-scientist-xkcd-story.html)."
    - It was inspired by Roger Peng and Hilary Parker's [Not So Standard Deviations podcast, Episode 28](http://nssdeviations.com/episode-28-writing-is-a-lot-harder-than-just-talking).

## Podcast Recommendations

- Roger Peng and Hilary Parker's [Not So Standard Deviations](http://nssdeviations.com/) is also about statistical issues, and is relevant to both academics and people working (or looking to work) in industry.
- Roger Peng and Elizabeth Matsui produce [The Effort Report](http://effortreport.libsyn.com/) which is about academic life in medicine, as much as anything else, framed through the lenses of a statistician and a clinician who do research together.
- The [Casual Inference](https://casualinfer.libsyn.com/) podcast, with Lucy D'Agostino McGowan (Wake Forest) and Ellie Murray (Boston U) has been recommended to me by several people and they have some great guests to talk about core concepts in epidemiology and biostatistics. I've only listened to one episode, but it was great. 
- David Spiegelhalter appeared on a [recent episode of *The Guardian's* Science Weekly podcast](https://www.theguardian.com/science/audio/2019/apr/05/cross-section-david-spiegelhalter-science-weekly-podcast) to discuss statistics and its importance to medical scientist.
- [FiveThirtyEight](https://fivethirtyeight.com/tag/fivethirtyeight-podcasts/) runs both a sports and a political podcast. The "Model Talk" episodes are particularly great for me.
- Of special interest this morning is [Episode 691 (2020-01-12) of This American Life](https://podcasts.apple.com/us/podcast/this-american-life/id201671138?i=1000462305611), entitled [Gardens of Branching Paths](https://podcasts.apple.com/us/podcast/this-american-life/id201671138?i=1000462305611) which is (according to my Twitter friends) a great series of examples related to the notion of [potential outcomes and the Rubin Causal Model](https://en.wikipedia.org/wiki/Rubin_causal_model).

## From Twitter, in response to Gerstein et al. 2019-01-19 at *The Lancet*

![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/images/lancet-tw01.PNG)
![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/images/lancet-tw02.PNG)
![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/images/lancet-tw03.PNG)

Maybe we should get some more people to read Miguel Hernan? For instance, try [The C-Word: Scientific Euphemisms Do Not Improve Causal Inference From Observational Data](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5888052/).

## After today's class, you should be moderately well-equipped to:

1. Do [Homework 1](https://github.com/THOMASELOVE/2020-500/tree/master/homework/hw1), perhaps with some help from the [r-basics] page or from the [Homework 0] example or, if that fails, and googling doesn't help, email us at **500-help at case dot edu**.
2. Start work on your [Project Proposal](https://github.com/THOMASELOVE/2020-500/tree/master/project), at least in terms of reading through the materials and seeing what's ahead of you. 
3. Start identifying a good article or two using propensity scores for your [Observational Studies in Action](https://github.com/THOMASELOVE/2020-500/tree/master/osia) assignment.
4. Read at least the Preface and Chapters 1-2 of Rosenbaum, in anticipation of our discussion next time. Were I you, I'd continue on to read through Chapter 4 if you have the time.
5. Remember to ask us for help at **500-help at case dot edu**!

![](https://github.com/THOMASELOVE/2020-500/blob/master/classes/class01/images/phd_staring.PNG) http://phdcomics.com/comics/archive.php?comicid=1479

That's plenty. 

## One Last Thing

Remember that in honor of the late Dr. King, the following Cleveland institutions will be offering free admission Monday...

- The [Cleveland Botanical Garden](https://cbgarden.org/) (10am-5pm)
- [Cleveland History Center](https://www.wrhs.org/cleveland-starts-here/) (10am-5pm)
- [Cleveland Metroparks Zoo](https://www.clevelandmetroparks.com/zoo) (10am-5pm)
- [Cleveland Museum of Natural History](https://www.cmnh.org/) (10am-5pm)
- [Great Lakes Science Center](https://greatscience.com/) (10am-5pm)
- [Maltz Museum of Jewish Heritage](https://www.maltzmuseum.org/) (11am-5pm)
- [Rock & Roll Hall of Fame](https://www.rockhall.com/) (10am-5:30pm).

to say nothing of the [Cleveland Museum of Art](https://www.clevelandart.org/), which is closed Mondays but is free to the public, and just around the corner...
