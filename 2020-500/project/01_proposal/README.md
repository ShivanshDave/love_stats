# Task 1: The Project Proposal

## Contents of this Page

- [Submission Specifications](https://github.com/THOMASELOVE/2020-500/blob/master/project/01_proposal/README.md#submission-specifications)
- [What should the proposal look like?](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#what-should-the-proposal-look-like)
    - [Overview (Title, Investigators, 8 key sections)](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#overview-title-investigators-8-key-sections)
    - [Detailed Instructions for each section of the proposal](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#detailed-instructions-for-each-section-of-the-proposal)
- [How does Dr. Love evaluate these Proposals?](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#how-does-dr-love-evaluate-these-proposals)
    - [Spreadsheet of Key Proposal Elements](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#spreadsheet-of-key-proposal-elements)
- [Frequently Asked Questions about the Proposal](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#frequently-asked-questions-about-the-proposal)
- [If you need ideas for a project in 500...](https://github.com/THOMASELOVE/2020-500/tree/master/project/01_proposal#if-you-need-ideas-for-a-project-in-500)

**ASK QUESTIONS EARLY. It's always easier to make adjustments when time pressure isn't a major issue.**

## Submission Specifications

The Proposal is submitted via [Canvas](https://canvas.case.edu/) in two versions, first an *initial draft* and then a *final proposal*. The deadlines for both the initial draft and the final version are specified on the [Course Calendar](https://github.com/THOMASELOVE/2020-500/blob/master/calendar.md). There is no substantial difference between the two versions, except that I am hopeful that you will have a final version of your data set the second time around, whereas in the first draft, you can get by with some uncertainty on some issues related to your data.

## What should the proposal look like? 

Your proposal will be a 3-4 page summary (moving towards an abstract) of your proposed study. 

- Begin with a good, interesting, thought-provoking title. You will work hard on this: please don't call it "Observational Studies Project."  A vast majority of your intended audience will never get past the title and abstract of the final report. Get off to a good start. Avoid deadwood like "The Study of..." or "An Analysis of..." and keep your caveats out of the title sufficiently that you can express the title in no more than 140 characters, including spaces.
- Next, provide your name and the names of any co-investigators (in which case you should indicate their role in this work.) If you're doing this work as part of your work at an institution other than CWRU, specify that, too.

### Overview (Title, Investigators, 8 key sections)

After your title and investigator information, there are eight sections I will be looking for, and I suggest you use the following headings:

1. Background
2. Objective and Research Question
3. Participants
4. The Exposure
5. The Outcome(s)
6. The Covariates
7. Getting the Data Set
8. Planned Methods

That should be sufficient for the first draft of your proposal, and in the final draft, you'll be reacting to my requests for improvements, and that may lead to some changes in how you decide to present the results.

### Detailed Instructions for each section of the Proposal

Your proposal should include all of the following...

1. No more than a paragraph (and, perhaps, one figure) of background information, meant to help me understand the study's objective. Use words I know.
2. An objective or list of study objectives, which leads directly to the research question or questions.
    - Be sure you specify the population, key outcome(s), and exposure/treatment (as well as, perhaps, some of the covariates of interest) in developing your objective.
    - This is a **SMALL** study. Do not boil the ocean.
    - Follow your objective with a careful statement of the research question(s), with indications about anticipated directions for any hypotheses. 
    - Please state research questions as questions. Questions end with question marks.
    - No more than two research questions, please.
3. A brief description of the participants, including key inclusion or exclusion criteria, as well as the size and style of the sample (i.e. 200 consecutive male patients between November and May with burns over more than 15% of their bodies)
    - Be sure also to tell me where the subjects come from, and how they're selected to be in the study, as well. You're specifying at the least the *setting* in which the data were collected.
    - Be sure to provide an appropriate classification of the type of research design (i.e. prospective cohort, etc.)
    - Your sample size should include somewhere between 250 and 2,500 subjects. You need at least 100 observations in each of the two exposure groups.
    - If your study begins with more than 2500 subjects, you will take a random sample of subjects so that your total sample size is around 2,500 or so for the project. You can always drop back to a more complete sample later, if you code this sensibly, but if you have more than about 2,500 observations, your R code development will get very slow for some of the things you need to do.
4. A brief but sufficient description of the intervention or exposure of interest. You need to tell me what the two groups of subjects are that you intend to compare, and how many subjects are in each of those groups.
    - The exposure group with smaller sample size should be your "intervention" group and membership in this group is what you will predict in your propensity score model.
    - If you have roughly equal numbers of subjects in your "intervention" and "control" groups, then 1:1 matching won't work very well (unless you do it with replacement) so you may wind up needing to consider other matching approaches. For purposes of this project, if you are in a setting where you can choose your sample sizes, make them imbalanced, perhaps with a ratio of 1 "intervention" subject for every 3-5 "control" subjects.
    - Subjects with missing data on either the key exposure (that divides the sample into groups) or the outcome of interest will need to be dropped from your work, and thus should not be counted here.
    - Be sure to describe how the exposure is allocated to participants. 
5. A listing of (at most two) outcome measures, which should be clearly linked to the objectives.
    - You must be comparing two groups/treatments/exposures on at most two outcomes, one of which must be identified in advance as primary.
    - Your outcomes must be either binary, quantitative or time-to-event. A single outcome is fine. Two is the maximum.
    - Make sure you tell me what the **primary** outcome is that you wish to compare subjects on, and how that variable is measured, and also specify what type of variable (binary/quantitative/time-to-event) it is.
    - This isn't a study where you will have time to "boil the ocean" - you're doing several analyses of one data set to look at one key relationship.
    - Hearing about a secondary outcome (or potential other options for the primary outcome) is welcome, but you will eventually need to  limit yourself to no more than two outcomes, total, in this study. Provide similar information for secondary outcomes as for primary ones.
    - Be sure to indicate clearly why these outcome measures are important. Do not assume that I know. 
    - Also, please indicate clearly how these outcome measures will be obtained and (one hopes) validated.
6. A list of the covariates you intend to use in building your propensity score models. Provide enough information so that I can easily understand the answers to the following questions:
    - What is the nature of the covariate information - what variables do you have, specifically, that you propose to include in your Table 1 comparing the two groups, and in the propensity model? 
    - Are they all measured PRIOR to the decision to apply or not apply the exposure of interest to patients?
    - Ideally, you'd prepare the necessary Table 1 that specifies this information broken down into your two treatment/exposure groups as part of your second draft of the proposal, if you have the data. We don't need the full thing in the first draft, though.
7. A paragraph or two describing the mechanism that allows you to access the data set, and confirming that you either have it or describing why you will certainly be able to have it well before the April 1 deadline for data acquisition. 
    - If you don't have the data, be sure to tell me what the steps are that need to happen to get the data in your hands. 
    - You should also specify the situation in terms of IRB/HIPAA concerns, briefly, or make it clear to me that this isn't an issue.
    - Include very specific information about how you got the data, and how I can get the data or why I cannot get the data.
8. A paragraph or two describing your planned statistical methodology for building outcome models answering your research questions. Obviously, you won't have developed a complete tool set here, but do the best you can. Here is a sample recipe for this last piece:
    - Statistical Methods: Appropriate graphical and numerical data summaries across *the exposure groups*, followed by propensity score matching and weighting methods to address selection bias. For outcomes analysis, our primary tool will be *primary tool* on propensity-matched pairs, as well as propensity-weighted (double robust) comparisons of *the exposure groups* on *our primary outcome*.
    - Note that you'll need to insert the information *in italics* yourself, including the specific exposure groups you're comparing and your primary outcome measure. In most cases your primary tool is determined by the type of outcome you are working with, as follows:
        - If your primary outcome is continuous, your primary tool will usually be linear regression.
        - If your primary outcome is binary (yes/no), your primary tool will usually be logistic regression. 
        - If your primary outcome is time-to-event, your primary tool will usually be Cox regression.
    - To clarify, all of you will be doing both propensity matching (one of several types) and an analysis using propensity score weighting (with a double robust adjustment included) to assess the impact of your treatment on your outcome. All analysis plans should indicate this clearly, as indicated above.

## How does Dr. Love evaluate these Proposals?

First, the plans for this project must look 100% feasible to me - the big problems I worry about are as follows.

1. getting the data too late to react well to problems, 
2. missing data that are not anticipated, 
3. limited covariate sets, in terms of either few covariates, or missing dimensions of the problem of interest
4. inappropriate study designs for the sorts of propensity score analysis we are focused on (I worry about case-referent/case-control studies more than I do retrospective or prospective cohorts, for instance) 
5. trying to do multiple studies at once, and 
6. covariates which essentially define the propensity score (for instance, all of the tall people got my treatment, and all of the non-tall people got my treatment B). 

Some people want to build their projects into more substantial work, but this is a class project, not a MS thesis in itself. Remember that you're going to have limited time to present your work, so some simplifying will be necessary.

### Spreadsheet of Key Proposal Elements

As part of my evaluation of your proposal drafts, I will be preparing a spreadsheet to share with the group. For each project, I am trying to identify the following elements. Please ensure that you have made my development of your row in that spreadsheet trivially easy to do. The sheet asks for:

1. your title
2. your collaborators (both team members in class and people outside of the class who are involved in the work or who provided you the data)
3. your data source, with specific information about how you got the data, and how I can get the data or why I cannot get the data
4. whether you have the data in hand, and if you don't, when you will get it and how you know that's when you will get it
5. what the sample size is overall (obviously this should exclude any subjects for whom you have missing treatment or outcome data), and what # and % of those people have the treatment/exposure that you will be building a propensity model for, and what # (%) have the alternative treatment/exposure. Note that you have to have a binary treatment/exposure. Not several exposures - just the one, with only two possibilities, clearly described.
6. what the population is that you intend to generalize to from your sample, with a clear indication as to why your sample is (or isn't) representative of that population, and how you know that
7. what the outcome is (you can look at a maximum of two outcomes, must designate one as primary and both outcomes can only be binary, quantitative or time-to-event. No multi-categorical outcomes, and no longitudinal outcomes, unless you're just looking at a change over time variable represented by a slope or difference
8. what the treatment/exposure is, and (again) how many people have it, and how many have the alternative in your sample
9. what the covariates are that you plan to include in your propensity model and how they are measured / categorized. I should easily be able to tell how many observations you have for each category of a categorical variable, and how many missing values you have for any kind of variable. Ideally, you'd be ready to prepare the necessary Table 1 that specifies this information broken down into your two treatment/exposure groups as part of your second draft of the proposal.

If you don't understand the answers to any of these nine questions yet, that's a problem with the data set you've selected that you need to resolve before submitting your proposal.

## Frequently Asked Questions about the Proposal

1. I want to run a project idea past you prior to doing a formal proposal. What information do you need to see immediately to understand whether or not a more complete proposal is likely to be successful?
    - There are four things I will need, at a minimum. 
        - What is the exposure - what are the two groups of patients you intend to compare, and how many patients are in each of those groups (it's also helpful to tell me where the patients come from, and how they're selected to be in the study.) Ideally, you will have substantially more patients (at least twice as many) in your "control" group as in your "intervention" group.
        - What is the primary outcome you wish to compare them on, and how is that variable measured? Hearing about secondary outcomes is also helpful, but you should limit yourself to no more than two outcomes, total, in this study.
        - What is the nature of the covariate information - what variables do you have, specifically, that you propose to include in your Table 1 comparing the two groups, and in the propensity model? Are they all measured PRIOR to the decision to apply or not apply the exposure of interest to patients?
        - Do you have the data in hand? What are the steps that need to happen to get the data in hand? Are there any IRB/HIPAA concerns worth mentioning at this point?
        
2. What are the characteristics of a data set that makes it highly appropriate for this project?
    - You have the data, and can prove to me that you can present it to the class without drawing the ire of any regulatory body or review board.
    - You know how the data were gathered, and can investigate problems in the data yourself. You are capable of cleaning and managing the entire data set that you plan to use, yourself.
    - The data have not previously been analyzed using propensity scores, though it is possible that you have new data and wish to partially replicate an existing study.
    - The data compares two groups of subjects, some of whom received an exposure of interest and some of whom did not (or received an alternative exposure) for reasons that are not directly related to a random allocation.
    - There are multiple covariates which can help explain why the subjects did or did not receive the exposure of interest.
    - There is at least one well-measured outcome of interest, which you believe to be both important to learn about and to potentially be causally linked to the exposure, usually on the basis of both a logical argument, some (biological or other) theory and some prior empirical evidence.
    - You have sufficient numbers of subjects and covariates for propensity score methodology to be plausible. On some level, the more observations you have, the better, but not if you're still collecting or cleaning the data. If you have more than a half-dozen covariates you wish to include in the propensity score, and have at least 100 patients in the smaller of your two exposure groups, I am not likely to be especially concerned about the size of your data set. If you cannot meet these standards with a data set in which you have a serious interest, contact me to discuss the matter, soon.

3. I have multiple outcomes I'm interested in - it's hard to pick a primary one in advance - will I have time to look at multiple outcomes in the presentation?
    - You may build models looking at multiple outcomes - expect to wind up only presenting some of those outcomes, and perhaps only one in detail, for the class. You should explain to me in your proposal what the other outcomes of interest might be. If you have all of the data, you can easily re-run things with a series of different outcomes once you've set up the main propensity analyses.

4. Will you help me find a data set to use?
    - That's your job and it can be a difficult one. I will happily help you decide whether a particular observational study is likely to work well for this project, but I am not going to find data for you.
    - Below, I list some available free options you might consider.

## If you need ideas for a project in 500...

You might consider these possibilities...

1.  Use [County Health Rankings](http://www.countyhealthrankings.org/explore-health-rankings/rankings-data-documentation) data. 

> As of 2016, there were 3,007 counties, 64 parishes, 19 organized boroughs, 10 census areas, 41 independent cities, and the District of Columbia for a total of 3,142 counties and county-equivalents in the 50 states and District of Columbia. There are an additional 100 county equivalents in the territories of the United States. (Wikipedia). 

- I could imagine, for instance, your pulling down data from a series of states until you have a reasonable cross-section of information from the most recent County Health Rankings for, say, 1500 counties, for which you have a quantitative outcome like age-adjusted years of potential life lost per 100,000 population, or percentage of adults reporting fair or poor health, an exposure variable that you develop from the data - like whether the income inequality ratio was above or below a certain threshold (or, perhaps better, whether it was in the top quarter or the bottom half of counties as a whole so you'd have something like a 1:2 ratio between exposed (to, for instance, high income inequality) and control). Then, as covariates you would have a lot of county specific information.

2. Use [NHANES](https://www.cdc.gov/nchs/nhanes/index.htm) data. The National Health and Nutrition Examination Survey is an excellent source of potential data for you, with lots of interesting outcomes, treatments and covariates to explore. You would certainly want to use more than one survey's worth of data, if possible, and several different questionnaires, rather than relying on just one. If you're interested in genomics, you might take a look at Patel, Chirag J. et al. (2016), [Data from: A database of human exposomes and phenomes from the US National Health and Nutrition Examination Survey](https://datadryad.org/stash/dataset/doi:10.5061/dryad.d5h62) and the associated materials linked there, to see if that might prove suitable.

3. Use [500 Cities](https://www.cdc.gov/500cities/index.htm) data. This is a pretty easy download, and there are lots of approaches you could take that would be interesting. Again, the hard work would be identifying a treatment, outcome and covariates that make sense.




