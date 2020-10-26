Lab 07
================
Last Edited 2020-10-25 22:21:51

# General Instructions

There are ten questions on this assignment. Please make sure to respond
to all ten.

You are welcome (encouraged, really) to discuss Lab 07 with Dr. Love,
the teaching assistants and even your colleagues, but your answer must
be prepared by you alone. Don’t be afraid to ask questions, either via
[Piazza](https://piazza.com/case/fall2020/pqhs431) (use the lab07
folder), at [TA office
hours](https://thomaselove.github.io/431/contact.html) or before/after
class.

We have not provided a template for this Lab. Please include properly
numbered sections, a table of contents, and use an attractive theme
(such as `theme_bw()`) for your visualizations.

## Submitting your Response

Build your entire response as an R Markdown file. Then knit the file to
create an HTML document. Submit both your R Markdown file and the HTML
output file to [Canvas in the Lab 07 section of the Assignments
folder](https://canvas.case.edu) by the deadline specified in [the
Course Calendar](https://thomaselove.github.io/431/calendar.html).

# Question 1 (10 points)

Find an example of a visualization designed to support a comparison of
at least two population means or medians using either paired or
independent samples in a published work (online or not) for which you
can find the complete sourcing information, and which was built no
earlier than January 1, 2016. You want to pick a visualization that you
think you can improve, either because it’s not designed well, or because
it’s misleading with regard to the comparison it’s designed to support.

Provide the complete reference and a copy of the image itself (including
any captions or titles) and surrounding material for the visualization.

# Question 2 (10 points)

In a few sentences, describe the purpose of the comparison being made in
your example from Question 1. Explain its context and why it is
important. Specify the research question that this comparison (and the
accompanying p value or confidence interval based inference, if
available) is providing to the reader.

# Question 3 (10 points)

In a few sentences, describe the visualization that you found which
relates to the comparison being made in your example from Question 1.
Explain what you believe the visualization is trying to do. Specify why
it is or is not effective, in your view.

# Question 4 (10 points)

Provide your best suggestion as to how either the visualization or the
comparison that you found in Question 1 might be improved, and explain
why your change (or changes) would be an improvement.

## Setup for Questions 5-10

These questions and the simulated data you will use to answer them are
motivated in part by an article\[1\] in *Health Psychology* by Stephan
et al. Quoting from that article:

> Subjective age is a biopsychosocial marker of aging with a range of
> health-related implications.

In our (fake) study, three groups of adults were asked to specify, in
years, how old they felt (their subjective age or *felt* age), as well
as their actual (or chronological) age. They were also asked about their
level of physical activity. The `active` variable in the data is 0 if
they are not particularly active, and 1 if they are deemed to be active.
We also have categorical information as to whether the adults belong to
group A, B or C.

Group A had 378 participants, Group B had 321 and Group C had 342, for a
total of 1,041 participants.

A measure used by Stephan et al. is the proportional discrepancy score
(which we’ll refer to as the **PDS**.) The PDS is calculated by …

> subtracting chronological age from felt age, \[and then dividing the
> result\] by chronological age.

and we will use this PDS measure as a key outcome in the work below.
You’ll need to figure out the best way to calculate it.

# Question 5 (10 points)

The same data appear in the `lab07a.csv` and the `lab07b.csv` files.
What is the difference between the two files, and which of the two files
is more useful for fitting an ANOVA to compare the PDS means across the
three groups of study participants? Why?

## The `lab07a.csv` file includes 1041 rows on these five variables:

  - `subject` = subject ID code
  - `category` = group A, B or C
  - `age` = actual chronological age, in years
  - `subj_age` = subjective, or felt, age, in years
  - `active` = 1 if active, 0 if not

## The `lab07b.csv` file includes 2082 rows on these five variables:

  - `subject` = subject ID code
  - `category` = group A, B or C
  - `age_type` = Chronological or Subjective
  - `years` = age (as specified by age\_type) in years
  - `active` = 1 if active, 0 if not

# Question 6 (10 points)

Calculate and compare the sample PDS means across the three groups, and
specify the rank order (highest to lowest) of the sampled PDS means.

# Question 7 (10 points)

Produce a graphical summary to compare the three groups that allows you
to assess the Normality and Equal Variances assumptions of an ANOVA to
compare the PDS means across the three groups. What conclusion do you
draw about ANOVA assumptions in this setting?

# Question 8 (10 points)

Now do the actual comparison of the PDS means of the three groups (A, B
and C) using an analysis of variance. What conclusion do you draw, using
a **90%** confidence level?

# Question 9 (10 points)

This is a pre-planned comparison, but the sample sizes differ across the
groups being compared. Obtain the results from a Tukey HSD method and
then a Bonferroni approach for pairwise comparisons of the population
PDS means, in each case again using a 90% confidence level\[2\]. Do your
conclusions differ using these two approaches?

# Question 10 (10 points)

Specify the linear model regression equation used to predict our PDS
outcome on the basis of group membership, but now also adjusting for
whether or not the subject is `active`. What fraction of the variation
in PDS levels is explained by this model? How much more of that
variation is explained than by the model including group membership
alone? How do you know?

### Footnotes

1.  The motivating article is Stephan Y Sutin AR Terracciano A (2016)
    Feeling Older and Risk of Hospiatlization: Evidence from Three
    Longitudinal Cohorts, *Health Psychology*, [available as a PDF
    here](https://www.apa.org/pubs/journals/releases/hea-hea0000335.pdf).

2.  Note that the `TukeyHSD` function takes a `conf.level` argument to
    specify something other than the default 0.95. So, in fact, does the
    Bonferroni approach using `pairwise.t.test`, although it’s not
    actually necessary there, since that method only produces *p*
    values, not confidence intervals.
