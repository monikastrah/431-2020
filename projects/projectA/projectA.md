Draft of Project A Instructions
================

This is a draft. A more complete version (with some changes, perhaps)
will appear before class on 2020-09-15.

# Your “Proposal” will be due 2020-10-02 at Noon

You will submit a short document providing the answers to a series of
questions related to your Data Development work. The TAs and Dr. Love
will review these results to ensure that your proposed plan meets the
requirements for this project, and either approve the plan, or request
changes. If changes are requested, you’ll have 48 hours to make those
changes and resubmit until your plan is approved.

## Working Alone vs. Working in a Group

You may work alone on this project, or in a group of two people. If you
decide to work in a pair, you will specify that in the “proposal” stage,
and you’re stuck with that choice for the rest of Project A.

# Your Final Submission involves Three Parts, all due 2020-10-20 at Noon

1.  **The Report** You will submit a report in both R Markdown and
    either HTML or PDF addressing all of the issues described in the
    Data Development and Analytic Tasks.

2.  **The Video** You will produce a video in the mp4 format of no more
    than 3 minutes in length if you’re working alone, and of no more
    than 5 minutes in length between you if you are working in a pair.
    In this video, you will describe what you believe to be the most
    important findings for your choice of two of the four analyses you
    will complete.
    
      - If you are working in a pair, each of you will present one of
        the two analyses.
      - Your video must include your face (so recording in Zoom is
        preferable) and must share graphs and results taken from the
        report you build.
      - The video must stand on its own, in the sense that it must be
        completely understandable to someone who has not read your
        report, but who is generally familiar with County Health
        Rankings and its measurements.

3.  **The Self-Evaluation** You will each (whether working alone or with
    a partner) submit a brief self-evaluation via a Google Form Dr. Love
    will make available.

All three elements are due at the Project A deadline.

# The Data

The data set for Project A is now available. The data are the 2020
version of the analytic data from County Health Rankings. In much of
what follows, we will abbreviate County Health Rankings as CHR.

The data are gathered at [the County Health Rankings Data &
Documentation
site](https://www.countyhealthrankings.org/explore-health-rankings/rankings-data-documentation).

The key links for you are provided as part of the National Data &
Documentation section of that site for the **2020 County Health
Rankings**. Do not use data from previous editions of the CHR, and do
not use the trends data in this project.

Specifically, you’ll need three files:

  - [the 2020 CHR CSV Analytic
    Data](https://www.countyhealthrankings.org/sites/default/files/media/document/analytic_data2020_0.csv)
    (a .csv file)
  - [the 2020 CHR Analytic Data
    Documentation](https://www.countyhealthrankings.org/sites/default/files/media/document/2020%20Analytic%20Documentation_0.pdf)
    file (PDF), and
  - [the 2020 Data
    Dictionary](https://www.countyhealthrankings.org/sites/default/files/media/document/DataDictionary_2020_2.pdf)
    (PDF)

These files are also available in the [data folder for Project
A](https://github.com/THOMASELOVE/431-2020/blob/master/projects/projectA/data/README.md)
on Github, and in the Google Drive folder Dr. Love has shared with you.

# Cleaning the Data

Cleaning the data will be a time-consuming effort but you can begin it
immediately. Before you complete any of the required analyses in R,
you’ll need to complete the following steps.

1.  Remove the first row of the csv file to leave the second row as the
    top row before ingesting the data into R (I suggest you do this in
    Excel or perhaps Google Sheets, and then resave a new version of the
    file without this top row as a .csv before ingesting into R)
2.  Select variables (there will be 8) that you actually need to use and
    rename them into useful formats instead of the default names
    provided by CHR.
3.  Filter to the subset of observations (counties) that you actually
    want to study, and note that each of these counties will have to
    have a `county_ranked` value of 1, and in addition, you will be
    working with a subset of the available `state`s, which should
    include the 88 counties of Ohio, plus counties from 3-5 other states
    you will select.
4.  Make some transformations to obtain categorical versions (factors)
    of selected variables and add them to your tibble.

# Data Development Task List

1.  **Identify a set of 4-6 states, containing 200-400 counties.** This
    must include the 88 counties of Ohio, and all of the counties within
    a subset of 3-5 additional states in the US, not including the
    District of Columbia, and also not including the five states
    (Connecticut, Delaware, Hawaii, New Hampshire and Rhode Island) with
    fewer than 12 counties. The number of counties associated with each
    state (specified using its two-letter postal abbreviation code) is
    listed below, for your convenience.

## States with fewer than 12 counties are italicized below.

| `state` |           Name | Counties |  | `state` |            Name | Counties |
| :-----: | -------------: | -------: | -: | :-----: | --------------: | -------: |
|  `AK`   |         Alaska |       25 |  |  `AL`   |         Alabama |       67 |
|  `AR`   |       Arkansas |       75 |  |  `AZ`   |         Arizona |       15 |
|  `CA`   |     California |       58 |  |  `CO`   |        Colorado |       60 |
|  `CT`   |  *Connecticut* |      *8* |  |  `DE`   |      *Delaware* |      *3* |
|  `FL`   |        Florida |       67 |  |  `GA`   |         Georgia |      159 |
|  `HI`   |       *Hawaii* |      *4* |  |  `IA`   |            Iowa |       99 |
|  `ID`   |          Idaho |       42 |  |  `IL`   |        Illinois |      102 |
|  `IN`   |        Indiana |       92 |  |  `KS`   |          Kansas |      104 |
|  `KY`   |       Kentucky |      120 |  |  `LA`   |       Louisiana |       64 |
|  `MA`   |  Massachusetts |       14 |  |  `MD`   |        Maryland |       24 |
|  `ME`   |          Maine |       16 |  |  `MI`   |        Michigan |       83 |
|  `MN`   |      Minnesota |       87 |  |  `MO`   |        Missouri |      115 |
|  `MS`   |    Mississippi |       82 |  |  `MT`   |         Montana |       48 |
|  `NC`   | North Carolina |      100 |  |  `ND`   |    North Dakota |       48 |
|  `NE`   |       Nebraska |       80 |  |  `NH`   | *New Hampshire* |     *10* |
|  `NJ`   |     New Jersey |       21 |  |  `NM`   |      New Mexico |       32 |
|  `NV`   |         Nevada |       15 |  |  `NY`   |        New York |       62 |
|  `OH`   |           Ohio |       88 |  |  `OK`   |        Oklahoma |       77 |
|  `OR`   |         Oregon |       35 |  |  `PA`   |    Pennsylvania |       67 |
|  `RI`   | *Rhode Island* |      *5* |  |  `SC`   |  South Carolina |       46 |
|  `SD`   |   South Dakota |       61 |  |  `TN`   |       Tennessee |       95 |
|  `TX`   |          Texas |      244 |  |  `UT`   |            Utah |       28 |
|  `VA`   |       Virginia |      133 |  |  `VT`   |         Vermont |       14 |
|  `WA`   |     Washington |       39 |  |  `WI`   |       Wisconsin |       72 |
|  `WV`   |  West Virginia |       55 |  |  `WY`   |         Wyoming |       23 |

So, including `OH`, you will need a total of 200-400 counties, from 4-6
states. For example,

  - one possible combination would be the states of `TX` (244 counties),
    `AZ` (15 counties) and `NM` (32 counties) in addition to `OH` (88
    counties), which would yield 379 counties in 4 states
  - another combination would be the states of `WA` (39 counties), `WI`
    (72 counties), `WV` (55 counties) and `WY` (23 counties) to join
    `OH` (88 counties) yielding 277 counties in 5 states
  - and yet another would be `PA` (67), `NY` (62), `NJ` (21), `MD` (24)
    and `VA` (133) in addition to `OH` (88) yielding 395 counties in 6
    states

**Note 1**: You can choose your subset of states in any way you like,
keeping in mind that some variables in the CHR data are not available
for some counties, and that each state you select should have more than
12 counties. You should have some reason for selecting the states that
you do, and you should describe that reason in a complete sentence or
two in your report.

2.  **Identify Your Variables**: Identify variables from the data for
    your selected sample of counties that will allow you to develop a
    data set that includes:

<!-- end list -->

  - the five-digit fips code for the county, which will be a convenient
    ID variable
  - the name of the county, which will be useful for labeling and
    identifying the counties
  - the `state`, which will be a multi-categorical (with 4-6 categories)
    variable
  - and a total of five variables selected from the 107 variables in the
    CHR data set that are listed as `vXXX_rawvalue` (note: to select the
    entire group of 107 variables, you might try
    `select(ends_with("rawvalue"))` as part of a pipe of the data.)

**Note 2**: Each of the five variables you select must have data for at
least 75% of the counties in each state you plan to study. This is
something you will have to check on.

**Note 3**: Across your complete set of 4-6 selected states, the raw
versions of each of your five selected variables must have at least 10
distinct non-missing values. Again, you’ll need to show that you have
checked this to be true.

3.  **Create Modified Variables**: Create your actual variables. Your
    five selected quantitative variables, selected by you from the 107
    available “raw value” CHR variables, will need be treated as
    follows:

<!-- end list -->

  - variable 1 will be treated as quantitative, and as an outcome of
    interest
  - two others (variables 2 and 3) will also be treated as quantitative
    predictors of interest for variable 1
  - variable 4 will be categorized into 2 mutually exclusive and
    collectively exhaustive levels to create a binary categorical
    variable of interest in predicting variable 1
  - variable 5 will be categorized into 3-5 mutually exclusive and
    collectively exhaustive levels to create a multi-categorical
    variable of interest in predicting variable 1
  - there will also be a seventh analytic variable, specifically the
    `state`, which will serve as another multi-categorical (with 4-6
    categories) predictor of variable 1

<!-- end list -->

4.  **Create your Main Tibble**: Your main data set for analysis then
    should be gathered into a tibble containing the following
    information:

<!-- end list -->

  - the identifying variables for each county, specifically:
      - `fipscode` = the five-digit fips code for the state and county,
      - `county` = the name of the county
      - `state` = the postal abbreviation code for the state
  - renamed versions of the original “raw value” versions of the five
    variables you’ve chosen, renamed to be more descriptive, and
    appended with `_raw` so that, for example, if you choose to use
    variable `v009_rawvalue` which is about adult smoking, your variable
    name should be `adult_smoking_raw`
  - your six “clean” versions of the data as described above, with your
    variables 2, 5 and 6 categorized appropriately using R code, and all
    of them renamed to be useful, so, for instance, if you’ve
    categorized the adult smoking variable, you might name that
    `adult_smoking_cat`, and if you’ve treated it as quantitative, you
    might name it `adult_smoking`.

Each row in this tibble should contain all of the counties within the
4-6 states you are studying, and no other counties should be included in
your tibble. If data for some counties are missing in the raw data for
one or more of your variables, then these data should be indicated as
missing (using NA) in the tibble.

In your R Markdown file, you will need to present all code necessary to
take the original .csv data file (with the top row removed outside of R)
and wind up with this tibble.

## Evaluating Your Tibble Numerically

You will then prove that your tibble is in fact a tibble and not just a
data frame by listing it, so that the first 10 rows are printed, and the
columns are appropriately labeled.

You will then provide a codebook as a table in your R Markdown file (and
HTML/PDF output) that specifies the name of each variable in your tibble
and its definition.

You will then demonstrate main numerical summaries from the tibble by
running the following three summaries:

1.  `Hmisc::describe` on the whole data set
2.  `mosaic::favstats` on each of your final (not raw) versions of the
    quantitative variables (so variables 1, 2, and 3)
3.  `janitor::tabyl` on your categorical variables 4 and 5 as well as on
    `state`.

# Your Project “Proposal” due 2020-10-02 at noon

Your project proposal requires you to create the tibble you plan to use
and then send (via Canvas) an R Markdown file and HTML (or PDF) result
that contains:

1.  A list of the states you chose, and the number of counties you are
    therefore studying.
2.  A list of the five variables (including their original raw names and
    your renamed versions) you are studying, with a clear indication of
    how you’re planning to create the categories in variables 4 and 5.
3.  A print-out of your tibble, to prove it is a tibble.
4.  The `Hmisc::describe` result for your tibble

Be sure that your proposal includes your name as the author in R
Markdown.

Dr. Love will provide an R Markdown template for the project “proposal”
document to you.

## Working with a partner?

Be sure that your proposal includes your name and that of your partner
(if you have one.) If you are working with a partner, exactly one of you
should submit the materials, and the other partner should submit a text
document (Word or PDF is fine) that reads

“My name is \[YOUR NAME\]. I am working on Project A with \[INSERT FULL
NAME OF YOUR PARTNER\], and they will submit the materials for the
proposal.”

# Analytic Task List for your Report

Using the tibble you’ve developed, you will then create the remainder of
your report by performing the four analytic tasks specified below.

1.  **Simple Linear Regression Model**: Provide evidence regarding the
    question of how well variable 1 can be predicted using one of the
    other quantitative variables (your choice of either variable 2 or
    variable 3). This should include a report on the effectiveness of a
    simple linear regression model, and an appropriate plot of the
    relationship. Important steps to include in your analytic report
    are:

<!-- end list -->

  - A visualization of the relationship between the outcome (Y-axis) and
    the predictor (X-axis) and a written description of what you learn
    about the association (which should include its direction, shape and
    strength along with identification of any substantial outliers). The
    addition of a loess smooth and/or a fit line to the plot should be
    important.
  - A specification of any transformations you choose to apply to the X
    or Y variable in order to obtain a better fit with a simple linear
    regression, along with some justification for the choice (or for the
    decision not to apply a transformation.)
  - A specification of the actual prediction equation created by the
    model, and an interpretation of what the coefficients mean, and how
    they should be interpreted in light of their estimated standard
    errors.
  - A specification of summary measures of goodness of fit, at a minimum
    the residual standard deviation (sigma) and the r-squared value. The
    quality of fit is not a consideration in the grading of this work.
  - Identification of the two counties (by name and state) where the
    model is least successful at predicting the outcome.

All of these elements should include R code that creates the information
you need, and complete English sentences that interpret those results.

2.  **Comparing Groups on a Quantitative Outcome using Independent
    Samples**: Provide evidence regarding the question of how well your
    variable 1 can be predicted using one of your categorical variables
    (you may select either the binary (variable 4) or the
    multi-categorical (variable 5) here.) This should include a report
    on the effectiveness of the resulting model following the
    suggestions from the first task, and an appropriate plot of the
    relationship between your quantitative and categorical variable.
    Consider a transformation of the quantitative outcome should that
    prove useful, and be sure to provide evidence regarding the impact
    of the assumptions of a linear model on your conclusions.

3.  **Adjusting for the impact of a categorical variable on your linear
    model**: Provide evidence regarding the question of how well
    variable 1 can be predicted using one of the other quantitative
    variables (your choice of either variable 2 or variable 3 and this
    doesn’t have to be the same one you chose in task 1) after adjusting
    for the effect of one of your categorical variables (variable 4 or
    5.) This should include a report on the effectiveness of the
    resulting model following the suggestions from the first task, and
    an appropriate plot of the relationship that shows the impact of the
    categorical variable through an attractive plot that helps us
    understand the inter-relationship of the three variables under
    study.

4.  **Adjusting for the impact of state on your linear model**: Provide
    evidence regarding the question of how well variable 1 can be
    predicted using one of the other quantitative variables (your choice
    of either variable 2 or variable 3) after adjusting for the `state`
    effect. This should include a report on the effectiveness of the
    resulting model following the suggestions from the first task, and
    an appropriate plot of the relationship that shows the impact of the
    `state` through an attractive plot that helps us understand the
    inter-relationship of the three variables under study.

# How Much Help Will You Get?

By 2020-09-22, Dr. Love will provide an R Markdown template for the
project “proposal”, as well as an (incomplete but useful) sample project
report, in each case using a previous year’s CHR data.

The Teaching Assistants are ready to help you with every stage of the
project, and you can ask them questions during office hours or via
Piazza starting 2020-09-15.
