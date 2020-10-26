Lab 08
================
Last Edited 2020-10-25 23:35:10

## General Instructions

Lab 08 includes 8 questions. Be sure to respond to each question by the
deadline posted on the [Course
Calendar](https://thomaselove.github.io/431/calendar.html).

You are welcome (encouraged, really) to discuss Lab 08 with Dr. Love,
the teaching assistants and even your colleagues, but your answer must
be prepared by you alone. Don’t be afraid to ask questions, either via
[Piazza](https://piazza.com/case/fall2020/pqhs431) (use the lab08
folder), at [TA office
hours](https://thomaselove.github.io/431/contact.html) or before/after
class.

We have not provided a template for this Lab. You are encouraged to
include numbered sections, a table of contents, and use an attractive
theme (such as `theme_bw()`) for your visualizations.

## Submitting your Response

Build your entire response as an R Markdown file. Then knit the file to
create an HTML document. Submit both your R Markdown file and the HTML
output file to [Canvas in the Lab 08 section of the Assignments
folder](https://canvas.case.edu) by the deadline specified in [the
Course Calendar](https://thomaselove.github.io/431/calendar.html).

# Question 1 (10 points)

Suppose you plan to study whether surgery can prolong life among men
suffering from prostate cancer, which typically develops and spreads
very slowly. Men diagnosed with prostate cancer will be randomly
assigned to either undergo surgery or not. Suppose you believe that
approximately 10% of men diagnosed with prostate cancer but do not have
surgery will eventually die from prostate cancer, and you want to do the
study using a sample size that will retain at least 80% power to detect
a drop down to 5%, using a two-sided approach with a 95% confidence
level.

What is the smallest number of men (including both the surgery and
non-surgery groups) that you will need to enroll in this new study to
meet these specifications, using a balanced design? Provide the details
of your calculation, and also provide a complete sentence or two
interpreting the meaning of the results in context.

# Question 2 (10 points)

In 2003, the *New England Journal of Medicine* published the results of
a Scandinavian study of the issue described in Question 1. In [that
report](http://www.nejm.org/doi/10.1056/NEJMoa012794), among 347 men
randomly assigned to surgery, 16 eventually died of prostate cancer,
compared with 31 of the 348 men who did not have surgery.

With 95% confidence, what can you conclude about a comparison of the
odds of death due to prostate cancer for those who did NOT have surgery
as compared to the odds of death for those who did have surgery? Provide
appropriate details of your calculations, including a sentence or two
interpreting the meaning of the results in context.

# Question 3 (10 points)

In a 2014 [follow-up
report](http://www.nejm.org/doi/full/10.1056/NEJMoa1311593#t=article)
describing results from Question 2 but now updated through the end of
2012, a total of 63 men assigned to surgery and 99 men not assigned to
surgery had died of prostate cancer. In a sentence or two, explain how
an analysis of these new results compares to the conclusions you drew in
Question 2.

# Data Description for Questions 4-8

Low dietary intake or low plasma concentrations of retinol,
beta-carotene, or other carotenoids might be associated with increased
risk of developing certain types of cancer. However, relatively few
studies have investigated the determinants of plasma concentrations of
these micronutrients. A cross-sectional study was designed to
investigate the relationship between personal characteristics and
dietary factors, and plasma concentrations of beta-carotene. Study
subjects (*n* = 290) were patients who had an elective surgical
procedure during a three-year period to biopsy or remove a lesion of the
lung, colon, breast, skin, ovary or uterus that was found to be
non-cancerous.

|      Variable | Description                                                                |
| ------------: | -------------------------------------------------------------------------- |
|     `subj_ID` | Subject identification code (S-1001 to S-1290)                             |
|         `age` | Subject’s age (in years)                                                   |
|         `sex` | Subject’s sex (M = male, F = female)                                       |
|     `smoking` | Smoking Status (Never, Former, or Current)                                 |
|         `bmi` | Body-Mass Index ( weight in kilograms / \[height in meters\]<sup>2</sup> ) |
|     `vitamin` | Vitamin Use (1 = Often, 2 = Sometimes, 3 = Never)                          |
|    `calories` | Number of Calories consumed (per day)                                      |
|         `fat` | Number of grams of fat consumed (per day)                                  |
|       `fiber` | Number of grams of fiber consumed (per day)                                |
|     `alcohol` | Number of alcoholic drinks consumed (per week)                             |
| `cholesterol` | Number of milligrams of cholesterol consumed (per day)                     |
|  `betaplasma` | Plasma beta-carotene (in ng/ml)                                            |

The `plasma8.Rds` data set is available [on our web
site](https://github.com/THOMASELOVE/431-2020/tree/master/labs/lab08/data)
for download. It contains 290 observations on the 12 variables described
in the table above. You will use a particular subset of 240 of those
observations (details on how you’ll pull this random sample follow so we
all pull the same one) to fit your models, and the remaining 50
observations to validate your model selection.

In questions 4-8, you will build and evaluate a pair of multiple
regression models for plasma beta carotene levels. To get started, I
suggest this approach to loading the data, if you’ve stored the
`plasma8.Rds` file in the data subdirectory of your R Project for Lab
08.

``` r
knitr::opts_chunk$set(comment = NA)

library(knitr)
library(janitor)
library(magrittr)
library(patchwork)
library(broom)
library(tidyverse)

plasma8 <- readRDS("data/plasma8.Rds")
```

Then use the following code to select a training sample from the data
set (to be used in questions 4-7) and a test sample (to be used in
question 8). Use `2020431` as your seed as we have done here - that is
what we’ll do in the Answer Sketch.

``` r
set.seed(2020431)
plas_train <- plasma8 %>% sample_n(240)
plas_test <- anti_join(plasma8, plas_train, 
                      by = "subj_ID")
```

If you want to check that you’ve done this in the way you’ll see it in
the sketch, here are the first few rows of the `plas_train` and
`plas_test` data sets.

``` r
head(plas_train) %>% kable()
```

| subj\_ID | age | sex | smoking |   bmi | vitamin   | calories |   fat | fiber | alcohol | cholesterol | betaplasma |
| :------- | --: | :-- | :------ | ----: | :-------- | -------: | ----: | ----: | ------: | ----------: | ---------: |
| S-1230   |  44 | F   | Current | 29.11 | Sometimes |   1446.2 |  63.2 |   9.5 |     3.2 |       208.8 |         79 |
| S-1192   |  35 | F   | Former  | 34.08 | Often     |   3114.0 | 160.2 |  14.9 |     0.2 |       432.3 |         43 |
| S-1102   |  55 | M   | Former  | 21.64 | Often     |   1896.1 |  82.2 |   9.3 |    10.0 |       296.8 |         39 |
| S-1058   |  74 | F   | Never   | 23.35 | Never     |   1512.1 |  73.8 |   8.7 |     5.7 |       182.8 |        324 |
| S-1163   |  69 | M   | Current | 27.23 | Often     |   2654.9 | 126.0 |  23.3 |     0.0 |       248.0 |        112 |
| S-1077   |  67 | M   | Former  | 24.74 | Often     |   2021.2 |  94.8 |  13.3 |     8.0 |       417.6 |         95 |

``` r
head(plas_test) %>% kable()
```

| subj\_ID | age | sex | smoking |   bmi | vitamin   | calories |   fat | fiber | alcohol | cholesterol | betaplasma |
| :------- | --: | :-- | :------ | ----: | :-------- | -------: | ----: | ----: | ------: | ----------: | ---------: |
| S-1002   |  56 | M   | Former  | 24.46 | Often     |   2433.6 | 127.6 |  19.9 |     7.1 |       271.2 |         74 |
| S-1005   |  65 | M   | Current | 23.38 | Often     |   6662.2 | 164.3 |  11.3 |   203.0 |       603.0 |         96 |
| S-1009   |  56 | F   | Never   | 32.08 | Often     |   1566.5 |  95.2 |   6.5 |     7.2 |       408.0 |         53 |
| S-1010   |  70 | F   | Never   | 20.16 | Often     |   2017.2 | 136.0 |   7.6 |     0.0 |       195.8 |        494 |
| S-1016   |  36 | F   | Former  | 42.89 | Often     |    798.2 |  30.6 |   7.9 |     2.4 |        46.3 |         51 |
| S-1030   |  39 | F   | Former  | 21.94 | Sometimes |   1719.3 |  49.7 |  18.4 |    11.0 |       164.6 |        357 |

# Question 4 (15 points)

Use the `plas_train` data frame to plot the distribution of the outcome
of interest, which is `betaplasma`, and then plot the natural logarithm
of `betaplasma`. Specify which of the two distributions better matches
the desirable qualities of an outcome variable in a regression model.
Whichever choice you make about the outcome – either `betaplasma` or
`log(betaplasma)` – stick with it for the rest of this Lab.

# Question 5 (10 points)

Use the `plas_train` tibble to build a model for your outcome (as
decided in Question 4) using four predictors: `age`, `sex`, `bmi`, and
`fiber`. Call that model `model_4`.

Summarize `model_4` and write a sentence or two to evaluate it. Be sure
you describe the model’s R-square value, and the model’s residual
standard error, sigma, in context.

# Question 6 (10 points)

For your `model_4`, what is the estimated effect of being **female**,
rather than male, on your outcome, holding everything else (age, bmi and
fiber) constant. Provide and interpret a 95% confidence interval for
that effect on your outcome.

# Question 7 (15 points)

Now use the `plas_train` tibble to build a new model for your outcome
(as decided in Question 4) using the following 10 predictors: `age`,
`sex`, `smoking`, `bmi`, `vitamin`, `calories`, `fat`, `fiber`,
`alcohol`, and `cholesterol`. Call that model `model_10`.

Compare `model_10` to `model_4` in terms of **adjusted** R<sup>2</sup>,
and residual standard error. Which model performs better on these
summaries, in the `plas_train` sample?

# Question 8 (20 points)

Compare the prediction errors made by the two models (`model_10` and
`model_4`) you have generated. In particular, you will need to:

  - Calculate the prediction errors from each model,
      - **Note**: If you chose to transform the outcome variable back in
        Question 4, then you will need to estimate the predictions here
        back on the original scale of `betaplasma`, rather than on the
        logarithmic scale. That involves making predictions on the log
        scale, and then back-transforming them with the `exp` function
        before calculating the residuals and eventually the summary
        statistics.
  - Visualize the prediction errors in each model, to let you compare
    them, and then
  - Form a table comparing the model predictions, in terms of MAPE (mean
    absolute prediction error), MSPE (mean squared prediction error) and
    maximum prediction error.

Based on your results, what conclusions do you draw about which model
(`model_10` or `model_4`) is preferable? Is this the same conclusion you
drew in Question 7?

# Add the Session Information

Adding a `sessionInfo()` chunk at the end of your document helps with
reproducibility.

``` r
sessionInfo()
```

``` 
R version 4.0.2 (2020-06-22)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 10 x64 (build 19041)

Matrix products: default

locale:
[1] LC_COLLATE=English_United States.1252 
[2] LC_CTYPE=English_United States.1252   
[3] LC_MONETARY=English_United States.1252
[4] LC_NUMERIC=C                          
[5] LC_TIME=English_United States.1252    

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] forcats_0.5.0   stringr_1.4.0   dplyr_1.0.2     purrr_0.3.4    
 [5] readr_1.3.1     tidyr_1.1.2     tibble_3.0.3    ggplot2_3.3.2  
 [9] tidyverse_1.3.0 broom_0.7.1     patchwork_1.0.1 magrittr_1.5   
[13] janitor_2.0.1   knitr_1.30     

loaded via a namespace (and not attached):
 [1] tidyselect_1.1.0 xfun_0.17        haven_2.3.1      snakecase_0.11.0
 [5] colorspace_1.4-1 vctrs_0.3.4      generics_0.0.2   htmltools_0.5.0 
 [9] yaml_2.2.1       blob_1.2.1       rlang_0.4.7      pillar_1.4.6    
[13] withr_2.3.0      glue_1.4.2       DBI_1.1.0        dbplyr_1.4.4    
[17] modelr_0.1.8     readxl_1.3.1     lifecycle_0.2.0  munsell_0.5.0   
[21] gtable_0.3.0     cellranger_1.1.0 rvest_0.3.6      evaluate_0.14   
[25] fansi_0.4.1      highr_0.8        Rcpp_1.0.5       backports_1.1.10
[29] scales_1.1.1     jsonlite_1.7.1   fs_1.5.0         hms_0.5.3       
[33] digest_0.6.25    stringi_1.5.3    grid_4.0.2       cli_2.0.2       
[37] tools_4.0.2      crayon_1.3.4     pkgconfig_2.0.3  ellipsis_0.3.1  
[41] xml2_1.3.2       reprex_0.3.0     lubridate_1.7.9  assertthat_0.2.1
[45] rmarkdown_2.4    httr_1.4.2       rstudioapi_0.11  R6_2.4.1        
[49] compiler_4.0.2  
```
