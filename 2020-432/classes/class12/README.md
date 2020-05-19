# 432 Spring 2020 Class 12: 2020-02-25

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Class 12 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class12/432_2020_slides12.pdf) | [Class 12 Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class12/432_2020_slides12.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Key Topic

Today, we'll be talking about multiple imputation and cross-validation approaches when fitting a linear regression model with `lm` and when fitting a logistic regression model with `glm`, in each case without using `aregImpute` or the `Hmisc` package.

### A Few References on Multiple Imputation

- Thomas Leeper's [Tutorial](https://thomasleeper.com/Rcourse/Tutorials/mi.html) which covers methods using `mice`, but also the `Amelia` and `mi` packages.
- Sterne JAC, White IR, Carlin JB, Spratt M, Royston P, Kenward MG, Wood AM, and Carpenter JR [Multiple imputation for missing data in epidemiological and clinical research: potential and pitfalls](https://www.bmj.com/content/338/bmj.b2393) BMJ 2009;338:b2393
- Stef van Buuren and Karin Groothuis-Oudshoorn [mice: Multivariate Imputation by Chained Equations in R](https://www.jstatsoft.org/article/view/v045i03) *J Statistical Software* 2011, 45:3.
- UCLA Statistical Consulting R FAQ: [How do I perform multiple imputation using predictive mean matching in R?]( https://stats.idre.ucla.edu/r/faq/how-do-i-perform-multiple-imputation-using-predictive-mean-matching-in-r/)

## Today's Announcements

1. Please remember that we don't have class this Thursday 2020-02-27. 
2. There is a [Minute Paper after Class 12](http://bit.ly/432-2020-minute-12). Please complete it by 2 PM Wednesday 2020-02-26.
3. The [Answer Sketch for Homework 3](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw03) is available. We anticipate **grades** appearing at http://bit.ly/432-2020-grades soon.
4. **Calendar Updates**
    - I've committed since we last met to having a total of **6 Homeworks** this term, and I've specified the dates on [the Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md). There may be one additional (optional) bonus assignment. Homework 4 is due at 5 PM on Monday 2020-03-23, and Homeworks 5 and 6 are due 2020-04-13 and 2020-04-20, respectively. I'll post the instructions for each Homework at least one week in advance. We throw out your lowest grade on a Homework, and average the other 5.
    - I've committed to having **3 Quizzes**, in total, this semester, and I've [posted the dates to the Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md). Quiz 2 is at the end of March, and Quiz 3 is at the end of April. Quizzes 1 and 2 will each be worth 75 points, and I don't know if Quiz 3 will probably be worth 100.
5. **Project 1 Proposal Status**
    - Let's take a look at [where we are](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/approved_proposals.md).
6. Since we last met, there have been several updates to the [Project 1 Instructions](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1).
    - This includes [a set of portfolio templates](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1/templates) which can be very helpful to you in terms of getting the formatting to work well. Switching between these three templates is simply a matter of swapping out the YAML code at the start of the R Markdown document.
    - The newest arrival is a [posterdown template](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1/templates) which we'll talk about today, and which I'm expecting you to use in preparing your poster.
7. [Quiz 1](https://github.com/THOMASELOVE/2020-432/edit/master/quizzes/README.md) will be [fully available](https://github.com/THOMASELOVE/2020-432/edit/master/quizzes/README.md) at 5 PM Wednesday 2020-02-26. 
    - In a change, Quiz 1 is now due at 2 PM on 2020-03-02 instead of 9 AM that day.
    - In writing Quiz 1, I restricted myself to materials from Classes 1-11, from Chapters 1-14 in the Course Notes, and from Chapters 1-5 and 7-8 in Spiegelhalter's *Art of Statistics*. Subsequent quizzes will also include material from these sections of the course, as I wasn't able to cover everything that I think is important, so I didn't try. 
    - Quiz 1 has 14 questions and is worth 75 points.
    - Some preliminary information [is already available](https://github.com/THOMASELOVE/2020-432/edit/master/quizzes/README.md), including a link to the Shared Google Drive where I've posted the data you'll need for some questions on the Quiz.
    - At 5 PM Wednesday, I'll post the PDF of the Quiz, and I'll post a link to the Answer Sheet where you'll write your responses (it's a Google Form, like our Minute Papers.)
    - Quiz 1 took the TAs 2-3 hours to complete. 2-3 of the questions are clearly more time-consuming than the others. 
8. The next meeting of [the Cleveland R Users Group](https://www.meetup.com/Cleveland-UseR-Group) is Wednesday evening (2020-02-26). I've been to a few of the meetings in the past (though I won't be at this one) and found them useful/interesting.
9. The annual [Joint Biostatistics Symposium](https://u.osu.edu/biostatisticssymposium2020/), organized between The Ohio State University, Case Western Reserve University School of Medicine, and the Cleveland Clinic, will be held this year from 11 AM to 3 PM on 2020-04-09 at Ohio State. Sadly, we have class that day.

## Next Few Deliverables (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
----: | ---------------------------------------------------------------
02-26 | If necessary, the third version of your [Project 1 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1#new-some-additional-thoughts-after-reviewing-the-proposal-drafts) will be due at 9 AM.
02-26 | [Minute Paper after Class 12](http://bit.ly/432-2020-minute-12) is due at 2 PM.
02-26 | [Quiz 1](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) will be made available at 5 PM.
03-02 | [Quiz 1](https://github.com/THOMASELOVE/2020-432/tree/master/quizzes) is due at 2 PM.
03-09 | [Project 1 Posters/Portfolios](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) are due at 2 PM.

## One Last Thing

If you're tired of building boxplots with violins, you might want to consider beeswarm plots, using [the `ggbeeswarm` package](https://github.com/eclarke/ggbeeswarm). 

Here's an example, motivated by an example from [@WeAreRLadies](https://twitter.com/WeAreRLadies/status/1227213192385818624) with [code here](https://gist.github.com/ivelasq/2ef720fe7138d1399b3315265e61232a).

![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class12/box_violin.png)
![](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class12/beeswarm2.png)

Here's the code...

```{r, eval = FALSE}
library(ggbeeswarm)
library(viridis)
library(tidyverse)

spotify_songs <- 
    read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-01-21/spotify_songs.csv') 

# Boxplot with Violin 

spotify_songs %>% 
    filter(playlist_genre == "pop" & track_popularity > 50) %>% 
    ggplot(aes(x = playlist_subgenre, y = danceability, group = playlist_subgenre, fill = playlist_subgenre)) +
    geom_violin() +
    geom_boxplot(width = 0.1, fill = "white") +
    ggtitle("Is Dance Pop More Danceable?", 
            subtitle = "Track Popularity of 50+") +
    scale_fill_viridis(discrete = T) +
    theme_minimal() +
    theme(axis.title.x = element_blank(),
          legend.position = "none")

# Beeswarm with Violin

spotify_songs %>% 
    filter(playlist_genre == "pop" & track_popularity > 50) %>% 
    ggplot(aes(x = playlist_subgenre, y = danceability, group = playlist_subgenre, color = playlist_subgenre)) +
    geom_quasirandom(alpha = 0.4) +
    geom_boxplot(width = 0.1, fill = "white") +
    ggtitle("Is Dance Pop More Danceable?", 
            subtitle = "Track Popularity of 50+") +
    scale_color_viridis(discrete = T) +
    theme_minimal() +
    theme(axis.title.x = element_blank(),
          legend.position = "none")
```
