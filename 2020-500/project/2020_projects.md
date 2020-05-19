# Projects for 2020 (now with Updates!)

[Amy Attaway](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#amy-attaway) | 
[Wyatt Bensken](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#wyatt-bensken) | 
[Sofija Conic](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#sofija-conic) | 
[Weichuan Dong](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#weichuan-dong) | 
[Joshua Froess](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#joshua-froess) |
[Jesus Gutierrez](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#jesus-gutierrez)

[Joseph Hnath](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#joseph-hnath) |
[Jason Huang](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#jason-huang) |
[Morgan McGrath](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#morgan-mcgrath) |
[Laurie Ann Moennich](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#laurie-ann-moennich) |
[Amin Saad](https://github.com/THOMASELOVE/2020-500/blob/master/project/2020_projects.md#amin-saad)

## General Reminders

1. Be sure that your exposure groups aren't completely determined by any of your covariates (for instance, if you have a multi-level categorical covariate, be sure that each exposure group appears at each level of the covariate at least a few times.)
2. If your covariates can possibly include Age, Sex, Race/Ethnicity, Severity of illness and Insurance, they probably should.

## Amy Attaway

### Hand grip strength and severity of chronic obstructive pulmonary disease: an analysis of the UK Biobank

- Objective: Compare handgrip strength in patients with COPD and those without COPD. 
- Research Question: Are reductions in handgrip strength associated with COPD (as compared to those without COPD)?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | 2500 subjects from the UK Biobank, ages greater than 40. (*Unclear whether all subjects must also be former smokers*)
Exposure | 500 COPD versus 2000 (randomly sampled) non-COPD.
Outcome | Handgrip Strength (quantitative). (**units of measurement?**)
Covariates | Age, sex, ethnicity, BMI, cirrhosis, heart failure, renal failure, cancer, and diabetes (**Are there other relevant covariates to explore?**)

### Update

1. The grip strength recorded in both hands but is supposed to be taken from the dominant hand. So I have to select for the dominant hand and then use that value. For people who are ambidextrous, I am taking the average of right and left handgrip strength. Is that okay? 

2. There are a lot of activity parameters in my dataset (such as amount of exercise per day) but I don’t think matching for that will be helpful as those with a higher activity level likely have a higher grip strength. 

## Wyatt Bensken

### Are Patients Who Undergo Emergency General Surgery More Likely to End Up at Care Facilities?

- Objective: To examine outcomes for older adults (ages 65 and older) who undergo emergency general surgery (EGS). 
- Research Question: Are older adults who undergo EGS more likely to no longer live at home (be moved to a care facility) than adults who do not undergo EGS?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Medicare Current Beneficiary Survey (MCBS) respondents (1992-2013) ages 65+, with fee-for-service Medicare
Exposure | 740 who had a diagnosis and procedure for EGS vs. random sample of those with neither diagnosis nor procedure (**many available - how many will you select**)
Outcome | Residence (Community-dwelling or transferred to a facility) (**all people are community-dwelling at the start, and exposed are when they have their EGS, but how will you identify comparators at similar risk?**) Binary.
Covariates | Age, sex, race, body mass index, frailty (deficit-accumulation frailty index,) multimorbidity, and each of the 29 individual conditions of the Elixhauser Comorbidity Index (**may be wise to also look at time in panel survey**)

### Update

1. The only problem I have at the moment is feeling confident in the random sample approach. As I have over 39,000 controls compared to 481 cases (the numbers dropped due to additional criteria restrictions), I have decided that for the matching I will utilize all of the controls as potential matches, but for the ATT weighted analyses I have decided that a 10% random sample of these 39,000 is appropriate. To overcome my unease, I will conduct stability analyses at 5% and 15% to see if there is any observable change and work these findings into my discussion and presentation.

## Sofija Conic

### Impact of College Education on Health Outcomes Based on County Health Rankings Data

- Objective: To assess the impact of obtaining some college education on two health outcomes, age-adjusted years of potential life lost per 100,000 individuals and preventable hospitalizations.
- Research Question: Do counties in the top quartile of some college education have better health outcomes compared to those in the bottom half of some college attainment?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Counties of the United States (those with information on the exposure and outcome in the 2019 County Health Rankings)
Exposure | 780 counties in the top 25 percent of "residents obtaining some college education" nationally as compared to 1557 counties in the bottom 50 percent.
Outcome | Years of potential life lost before age 75 per 100,000 population (age-adjusted, primary and quantitative). Hospital stays for ambulatory-care sensitive conditions among fee-for-service Medicare enrollees (rate per 100,000 enrollees, secondary and quantitative)
Covariates | see list below...

- County Demographics: % below 18 years of age, % 65 and older, % Non-Hispanic African-American, % American Indian and Alaskan Native, % Asian, % Native Hawaiian/Other Pacific Islander, % Hispanic, % Non-hispanic white, % Females, % Rural. (**there's a problem here with the race/ethnicity information**)
- Health Behaviors: Adult obesity, food environment index, food insecurity, limited access to healthy foods
- Clinical Care: Uninsured adults, uninsured children (**what are these? rates?**)
- Social and Economic Factors: median household income, income inequality (**how is this measured**)
- Family and Social Support: Children in single parent households, residential segregation (nonwhite and white) (**measurement approach?**)

### Update 

1. Some issues with wide variations in scale in the predictors. See Table 1.

![](https://github.com/THOMASELOVE/2020-500/blob/master/project/sofija.PNG)

## Weichuan Dong 

### Not Close to A Mammography Facility? Better Chance to Be Diagnosed With Late-Stage Breast Cancer

- Objective: To determine whether distance from patient residential location to the nearest mammography facility (distance to facility) is associated with Late Stage Breast Cancer (LSBC) diagnosis
- Research Question: Does a woman living farther away from her nearest mammography facility have causal effect of being diagnosed with late-stage breast cancer?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Women (**newly**) diagnosed with local, regional or distant stages of breast cancer between the ages of 45 and 70 in 2016 in Ohio, recorded in the Ohio Cancer Incidence Surveillance System (OCISS)
Exposure | Distance to facility (**approximately** 1440 in the "shortest" three quintiles vs. 480 in the "longest" quintile)
Outcome | Breast Cancer Stage at Diagnosis (Late = Regional or Distant, Early = Local) Binary.
Covariates | Age, Race, Hispanic Ethnicity, Marital Status, Primary Payer (**number of levels**), Area Deprivation Index of Census Block, rural-urban commuting area (RUCA) code (1 = metropolitan, 10 = very rural) (**Are there other available and relevant covariates?**)

### Update

1. My major concern is that this study could be more or less like a natural experiment because the treatment (distance to facility and vehicle availability of households) is not assigned by investigators based on certain criteria. As a result, the covariates may not be significantly different between the treated and control groups, which is a good thing but the propensity score may be less useful in this study. 

## Joshua Froess 

### Health Care Access in Urban vs. Rural Counties throughout the Northeastern and Mid-western United States

- Objective: To compare urban vs rural areas uninsured rates and ratio ofprimary care physicians in the northeastern and midwestern United States.
- Research Question 1: Is the uninsured rate higher in rural counties compared to urban counties?
- Research Question 2: Is the ratio of primary care physicians higher inurban counties compared to rural counties?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Counties within states that are classified in the northeastern and mid-western United States with relevant information in 2019 County Health Rankings
Exposure | 420 urban counties and 881 rural counties. Following a U.S. Census Bureau definition, an urban county has a population of 50,000 or more.
Outcome | Uninsured rate (primary) and the ratio of primary care physicians (secondary) (**details**)
Covariates | age-adjusted mortality, median income, percentages of ... poor or fair self-reported overall health, high school graduates (**details**), some college (**details - do you need both?**), adult smoking, non-hispanic white, female, unemployed, adult obesity, low birthweight, infant mortality, diabetes prevalence, coronary heart disease hospitalizations (**details on this measure - is it a percentage?)**, food insecurity, diabetes prevalence, and (**prevalence of?**) frequent mental health distress.

### Update

1. Is the warning `NAs introduced by coercion` anything to worry about? I looked it up and it happens where character variables are turned into numeric which I am doing to make a factor variable numeric.

## Jesus Gutierrez 

### The effect of "superspreaders" on the transmission of *M. tuberculosis* among household contacts in Kampala, Uganda

- Objective: To provide further evidence for the presence of superspreaders.
- Research Question: Will the exposure of a household to a superspreader lead to a higher percentage of infected persons (higher rate of transmission)?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Households located in the Kawempe division of Kampala that were home to an index case (adults (18 or older) who had an initial diagnosis of pulmonary TB). Household contacts were defined as individuals who resided in the household of the TB index case for at least 7 consecutive days during the previous 3 months. (**Are the index cases all male?**)
Exposure | 124 households exposed to superspreaders and 748 households not exposed to superspreaders. A superspreader is a male index TB case between the ages of 15 and 45 with a positive sputum smear (evidence of infectiousness) and an abnormal chest x-ray. 
Outcome | % of household contacts infected with latent TB infection (LTBIs) – positive tuberculin skin test (TST) result throughout the study but no active TB disease (primary, quantitative) % of household contacts who are new pulmonary TB cases (in addition to the index case) diagnosed at least (**do you mean within?**) 3 months after enrollment (secondary, quantitative). (**I continue to have serious concerns about the use of percentages/proportions here given the small denominators in most households, and I'm also wondering why a combined outcome isn't relevant.**)
Covariates | Characteristics of the index case and of the household - see list below

- Characteristics of index case
    - Age, HIV status (**need to do something about the 1 unknown here**), Symptoms including fever, weight loss, night sweats, etc., Smear positivity grade based on how many bacteria are visible in a sputum sample under light microscopy.  Findings on a chest x-ray including cavities, consolidations, pleural effusions
    
- Characteristics of household
    - Size of household during initial census of enrolled household, Number of persons per room, Number of windows used during the day, Cooking method (categorical - for this analysis, a binary variable “cooking inside the house” or “cooking method outside the house”, Distance from nearest health center in km.

### Updates

1. I am still deciding on which outcome variable(s) to use.  The main issue here is how to address the instability of the continuous outcomes. Given that both of these outcomes represent different stages of infection (one latent and one active), I could combine both continuous outcomes into a single one.  The other possibility is to transform the individual outcomes into binary outcomes (zero vs. non-zero).  This could also be done with the combined continuous outcome.  I wonder if it would be appropriate to complete all of this different analyses and then chose the best one or if I would have to choose one before starting the analysis.

![](https://github.com/THOMASELOVE/2020-500/blob/master/project/jesus.png)

## Joseph Hnath 

### Evaluating the efficacy of school-based learning of coping mechanisms

- Objective: To determine if school programs teaching about stress affect students’ abilityto relax and/or their risk of suicidal ideation.
- Research Question 1: Do students in grades 7-12 not learning about stress and coping mechanisms in school have more trouble relaxing?
- Research Question 2: Do students in grades 7-12 not learning about stress and coping mechanisms in school have an increased risk of suicidal ideation?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | National Longitudinal Study of Adolescent to AdultHealth (Add Health) respondents in 1995
Exposure | 919 students that did not learn about stress in a class at school and 1,664 students that did.
Outcome | How often you’ve had trouble relaxing in the last 12 months? (primary, binarized to Never vs. Ever from five-category scale), Did you ever seriously think about committing suicide? (secondary, binary)
Covariates | Age, Sex, Race, Ethnicity, Happiness with current school, Cleanliness of home, Total family income, Decision to live in this neighborhood because of the relative strength of the schools (**details?**), General perception of health (**details?**), Amount of time spent in the last week ... (1) on hobbies (2) playing sports (3) with friends, Average sleep hours per night, Number of times skipping school without an excuse this year, How many evening meals did you have with at least one parent present in the last week, How close do you feel to your mother / father, How much they agree with a statement about never getting sad (**details - and is this really a covariate or an outcome?**) 

### Updates

1. The major problem I am still facing is dealing with the timing of the exposure and covariates, along with including additional covariates. The initial draft spreadsheet mentioned 10 more covariates that you think that should be added, but I could not find them.

2. A minor problem is determining how to collapse the different ordinal variables.


## Jason Huang 

### Will We Have Happier Older Lives With Kids Living Nearby?

- Objective: To examine the effect of having any children around on the mental well-being of an elderlypopulation with any children
- Research Question: For older Americans who have any children and said children do not live with them, are they more likely to feel sad or depressed for two weeks in a row within the past 12 months if their children live more than 10 miles away from them than if they live closer?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Adults over age 50 participating in the National Health and Retirement Study 2016. People without living children who they are in contact with, and people who have children living with them (in the same household or nursing home), are excluded.
Exposure | 5302 answering No and 6532 answering Yes to "Do any of your children live within 10 miles of you?" (**how will you reduce this sample size?**)
Outcome | During the last 12 months, was there ever a time when you felt sad, blue, or depressed for two weeks or more in a row? (Binary)
Covariates | Number of adults people living in the same household, Number of living children, Race, Educational attainment, Financial stability (Assets and Income) (**need more details**) Physical health (self-rated health, chronic conditions, etc. - **need more details**), Insurance type (**details?**) Retirement status, Ever served in the military, Mode of Interview: (Telephone or Face to Face) (**are age and sex unavailable?**)

### Updates

1. The HRS data seems to have masked values for race and thevariables are confusing in the code book. For example, there are multiple responses recorded,which, I suppose, is for when a subject mentions a few different race categories. But, even themain variable for race contains nearly all blank responses. It’s odd that I’m seeing this but I’myet to figure out why. Once I do, if race is just unavailable to me, I’ll have to drop it.

2. There are 40 data files, each containing some of the variables. I have merged and filtered some of the variables to recode. But, I haven’tfinished merging everything yet.

3. Also, financial stability is hard to define using the rather comprehensive information that’s in thedata sets. I am struggling to find a good summary measure for it.

## Morgan McGrath

### The Metabolic Consequences of Poor Sleep

- Objective: To investigate the relationship between poor sleep (in quality or quantity) and glucose intolerance in a population of adolescent and adults with no history of clinically diagnosed diabetes.
- Research Question: Among individuals age 16+ living in the United States without a clinical diagnosis of diabetes, does poor sleep increase the risk of glucose intolerance?

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | 1623 NHANES 2015-16 participants (ages 16 - 80+) who completed an oral glucose tolerance test and a sleep disorders questionnaire who did not report a history of clinically diagnosed diabetes.
Exposure | 518 with poor and 1165 with good self-reported sleep quality (binarized from 5 NHANES questions - see below)
Outcome | Oral Glucose Tolerance Test (binarized, with > 140 mg/dl indicating glucose intolerance) and may also look at OGTT as a quantitative outcome.
Covariates | Age, Sex, Race, BMI, Living with partner, Children in household below age 5, ratio of family income to poverty level, family history of diabetes, diet quality (E-VG-G-F-P), meals not home prepared in last 7 days (**you indicate this is right-censored?**), physical activity at work and in recreation, generalhealth status, alcoholic drinks per day (**also right-censored?**), frquency of feeling anxious, depressed, (**is insurance status available?**)

![](https://github.com/THOMASELOVE/2020-500/blob/master/project/figures/mcgrath_exposure.PNG)

### Update

1. My only minor problem since the proposal is how to make the best use of the health insurance data available in NHANES. The data available include: 1) Are you covered by health insurance?; 2) In the past 12 months, was there any time when you did not have health insurance coverage?; and 3) Type of insurance coverage. My plan was to use the type of insurance, split into 4 categories (Private, Medicare, Medicaid, and Other). After looking at the data though, a large number of subjects have > 1 insurance type, in all different combinations. I’m not sure how I would recode that into a reasonable number of categories, e.g. what if someone has both private insurance and Medicare? Instead, I opted to use the binary information available from question #1 listed above, but it seems like I’m missing out an opportunity to include more rich data. Any suggestions are welcome. 

## Laurie Ann Moennich 

### Comparative Effects of Diabetes Mellitus in Patients Undergoing Endovascular Aortic Aneurysm Repair

- Objective: To explore the effect of diabetes mellitus (DM) treated with insulin on length of stay and hospital readmission after Endovascular Aortic Aneurysm Repair (EVAR).
- Research Question 1: Do patients living with insulin-dependant DM have a longer length of stay than patients **who have DM but don't require insulin**? (**revised to match your specified exposure below**)
- Research Question 2: Do patients living with insulin-dependant DM have a higher incidence of postoperative complications requiring hospital readmission than **who have DM but don't require insulin**? (**revised to match your specified exposure below**)

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Adults 18 and over undergoing EVAR in 2013-17 (*or is it 2013-18?*) in the American College of Surgeons National Surgical Quality Improvement Program (ACS NSQIP) database.
Exposure | 938 who have DM requiring therapy with insulin vs. 3334 who have DM but do not require insulin therapy (excluding those without DM) (**you discussed random sampling, but I encourage you to use these complete groups**)
Outcome | Days from Admission to Discharge after EVAR procedure (Quantitative), Readmission to Hospital (Binary - **within 30 days? other time frame?**)
Covariates | Age, Sex, Race, Discharge Destination (**number of levels**), Height, Weight, History of COPD, Congestive Heart Failure in the 30 days prior to surgery, Hypertension, Acute Renal Failure, Disseminated Cancer, Open wound/wound infection (**not sure I understand the last of these**), (**is insurance available?**)

### Update

1. Nothing to remark on at this time.


## Amin Saad

### Do Patients with Hemorrhagic Blunt Abdominal and Pelvic Trauma Benefit from the Use of Tranexamic Acid?

- Objective: Examine the current utilization of tranexamic acid (TXA) (an anti-fibrinolytic agent) to trauma patients in Michigan
- Research Question: Is the administration of TXA associated with improved patient outcomes in abdominal and pelvic trauma, mainly in-hospital mortality.

Component | Description
-------------: | --------------------------------------------------------------------------------------
Participants | Trauma patients ages 18+ reported to Michigan Trauma Quality Improvement Program, admitted with hemorrhagic blunt abdominal or pelvic trauma between 2013 and 2019-06-30. Some exclusions, as well, described in a flow chart (see below).
Exposure | 241 TXA or 338 Non-TXA during the hospitalization (**at any time, or just in the first 24 hours of the hospitalization?**)
Outcome | In-hospital mortality (primary - binary) and length of hospital stay (secondary - quantitative). 
Covariates | Age, Sex, Trauma Activation (full/partial/consult), Pulse, SBP, BMI, Glasgow Coma Scale, CPR received, Hematocrit, NISS (injury severity score), Operation performed, Baseline comorbidities (**need the details here**), (**are insurance and race/ethnicity unavailable?**)

![](https://github.com/THOMASELOVE/2020-500/blob/master/project/figures/saad_flowchart.PNG)

### Update

1. I have multiple outcomes that I am interested in examining for the purpose of publishing the results such as surgical complications and thrombotic complications (including stroke, myocardial infarction and deep venous thrombosis since TXA induces coagulation and thrombosis). Do I repeat the propensity score analysis for each outcome separately to produce appropriate estimates/odds ratio and then report that in a separate table?
2. In table 1, my understanding is that we report comparisons between groups before doing any kind of imputation in addition to summary stats after imputation and matching is conducted. Is it good practice to report missingness? 
3. Would it be appropriate to report in Table 1 summaries of variables not included in the analysis such as liver disease for example, just so that the reader has a better understanding of the patient population? 

