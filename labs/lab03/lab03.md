431 Lab 03
================
Last Edited 2020-09-21 12:01:30

# General Instructions

Lab 03 is divided into 10 questions (including a short essay in Question
10.)

Be sure to respond to each question by the deadline posted on the
[Course Calendar](https://thomaselove.github.io/431/calendar.html). You
are welcome (encouraged, really) to discuss Lab 03 with Dr. Love, the
teaching assistants and even your colleagues, but your answer must be
prepared by you alone. Don’t be afraid to ask questions, either via
[Piazza](https://piazza.com/case/fall2020/pqhs431) (use the lab03
folder), at [TA office
hours](https://thomaselove.github.io/431/contact.html) or before/after
class.

**PLEASE NOTE**: Your response to **every** question, whether we
explicitly ask for it or not, should include a complete English sentence
responding to the question. Code alone is not a sufficient response,
even if the code is correct. Some responses might not need any code, but
every response needs at least one complete sentence.

## An R Markdown Template for Lab 03

We have provided a useful R Markdown document template for this
assignment called `YOURNAME-Lab03.Rmd` that you are welcome to use to
help guide your work, but this is not mandatory.

  - The `YOURNAME-Lab03.Rmd` file is available in the [main folder for
    Lab 03](https://github.com/THOMASELOVE/431-2020/tree/master/labs/lab03),
    and also on the [Data and Code
    repository](https://github.com/THOMASELOVE/431-data) for the course.

The minimal setup for this assignment involves loading two relevant R
packages, as shown below.

``` r
library(MASS); library(tidyverse)
## make sure these libraries are installed in R
## always need tidyverse, also need MASS for Lab 03
```

## Data Description for Questions 1-7

The data come from the `faithful` data frame contained in the base
installation of R, specifically, within the `datasets` package. These
data describe the duration of an eruption for the Old Faithful geyser in
Wyoming’s Yellowstone National Park, as well as the waiting time until
the next eruption.

The commands below place the `faithful` data frame in a tibble called
`lab03`, then display the tibble. We encourage you to use this `lab03`
tibble to develop your answers to Questions 1-10.

    lab03 <- tibble(faithful)
    lab03

Use the command `?faithful` to see some additional details about these
data. The `lab03` tibble contains observations on two variables:

  - `eruptions` = eruption time in minutes
  - `waiting` = waiting time to next eruption, also in minutes

# Question 1

Plot a histogram or other summary plot which meaningfully describes the
distribution of the waiting times. Be sure it is very clearly labeled.

# Question 2 (on the center of the distribution)

What appears to be a typical waiting time? Compare the mean, median and
80% trimmed mean (mean of the middle 80% of the observed waiting times.)

# Question 3 (on the spread of the distribution)

What is the inter-quartile range of the waiting times, and how does it
compare to the standard deviation of the waiting times?

# Question 4 (on the shape of the distribution)

Describe the shape of the waiting times distribution in a few complete
sentences. You are welcome to use the histogram you built to help
address these issues, and you may also be interested in building an
additional plot or two - that’s your choice. You should address the
following questions in your response.

  - Is the distribution multi-modal or unimodal? How do you know?
  - Is the distribution skewed (and if so, in which direction) or is it
    essentially symmetric? How do you know?
  - Are there any unusual (outlier) values in the distribution, and if
    so, what are they?

# Question 5

In light of your work in Questions 1-4, would a model using the Normal
distribution be an appropriate way to summarize the waiting time data?
Why or why not?

# Question 6

Plot a scatterplot of the waiting times (y-axis) vs. the eruption
durations (x-axis) and be sure your plot is very clearly labeled.
Include the result of fitting a straight line regression model in your
plot. Then describe your general impression of the plot in a sentence or
two: what sort of relationship do you see?

# Question 7

Does a linear model seem like an appropriate thing to use in attempting
to predict the waiting time given the most recent eruption duration,
based on these data? Why or why not?

  - Your response should specify the regression line you fit for
    Question 6 and also provide a relevant summary statistic (or two)
    that provide an indication about how well that line fits the data.
  - For full credit, your response should describe the appearance of the
    plot in addition to stating what you learn from your summary
    statistic.

# Question 8

Investigate question 6 again, but now use the `geyser` data in the
`MASS` package, and compare your results to what you obtained
originally, in an appropriate way.

# Question 9

Investigate question 7 again, but now use the `geyser` data.

## Important Hints for Questions 8-9

1.  Be sure to use the command `?MASS::geyser` to see some additional
    details about these data, and to learn more about how they differ
    from the data in our original data set.
2.  There is at least one key difference between the variables available
    in `geyser` and those which you dealt with in the `faithful` data.
    For full credit, you must specify that difference (and describe its
    impact) in your response.
3.  The commands below will place the relevant data for Questions 8 and
    9 in the `lab03extra` tibble.

<!-- end list -->

    lab03extra <- tibble(MASS::geyser)
    lab03extra

# Question 10

In your reading of Jeff Leek’s book so far (you should have completed at
least Sections 1-5 and 9-12), what is the most important thing you’ve
learned?

  - This could be an idea that has stuck with you, a phrase or sentence
    that clarified something of importance, or a tip for working with
    data that you want to remember.

In a short essay (or perhaps 100-150 words), identify the relevant
passage from Leek’s book appropriately (be sure to specify the section
of the book and perhaps provide a short quotation), and then provide a
brief argument as to why this particular thing is something you value,
and how it might apply to your work.

# Add the Session Information

Adding a `sessionInfo()` chunk at the end of your document helps with
reproducibility. Just take a look to see what it produces in my case.

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
 [9] tidyverse_1.3.0 MASS_7.3-52    

loaded via a namespace (and not attached):
 [1] Rcpp_1.0.5       cellranger_1.1.0 pillar_1.4.6     compiler_4.0.2  
 [5] dbplyr_1.4.4     tools_4.0.2      digest_0.6.25    lubridate_1.7.9 
 [9] jsonlite_1.7.0   evaluate_0.14    lifecycle_0.2.0  gtable_0.3.0    
[13] pkgconfig_2.0.3  rlang_0.4.7      reprex_0.3.0     cli_2.0.2       
[17] rstudioapi_0.11  DBI_1.1.0        yaml_2.2.1       haven_2.3.1     
[21] xfun_0.16        withr_2.2.0      xml2_1.3.2       httr_1.4.2      
[25] knitr_1.29       fs_1.5.0         hms_0.5.3        generics_0.0.2  
[29] vctrs_0.3.3      grid_4.0.2       tidyselect_1.1.0 glue_1.4.2      
[33] R6_2.4.1         fansi_0.4.1      readxl_1.3.1     rmarkdown_2.3.3 
[37] modelr_0.1.8     blob_1.2.1       magrittr_1.5     backports_1.1.7 
[41] scales_1.1.1     ellipsis_0.3.1   htmltools_0.5.0  rvest_0.3.6     
[45] assertthat_0.2.1 colorspace_1.4-1 stringi_1.4.6    munsell_0.5.0   
[49] broom_0.7.0      crayon_1.3.4    
```

# Submitting your Response

Build your entire response as an R Markdown file (if you like you are
free to use the `YOURNAME-lab03.Rmd` template we have provided but this
is not mandatory.) Then use the Knit button in RStudio to create the
resulting HTML document. Submit both your revised R Markdown file and
the HTML output file to [Canvas in the Lab 03 section of the Assignments
folder](https://canvas.case.edu) by the deadline specified in [the
Course Calendar](https://thomaselove.github.io/431/calendar.html).

# On Grading

Lab 03 will be graded on a 0-100 scale, with question 10 weighted more
heavily than the other questions. You will receive some credit for
making a reasonable effort to build a good response to each question,
and then additional credit if your response is (essentially) correct,
your code is clean and you’ve written any text using complete English
sentences.

A more detailed grading rubric will accompany the answer sketch.
