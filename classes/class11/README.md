# 431 Class 11: 2020-09-29

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

> You can observe a lot by just watching (Yogi Berra)

## Today's Slides

- Class 11 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class11/431_class-11-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class11/431_class-11-slides_2020.Rmd).

## Who Will We Meet Today?

- **Modong Yang**, **Wail Yar**, **Kaan Yorgancioglu**, **Danny Lam**, **Jeff Kovach**, and **Arsh Kochar** (64-66 and 19-21 from the Introductory Student Videos in our Shared Google Drive)

## Announcements

1. The [Answer Sketch for Lab 04](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04/README.md) is now available.

2. The [Minute Paper after Class 11](https://github.com/THOMASELOVE/431-2020/blob/master/minutepapers) is open for responses, which are due tomorrow (2020-09-30) at noon.

3. Grades + TA Comments on Lab 03 are now at http://bit.ly/431-2020-grades.

4. **Project A Proposal** 

- Several students met my Noon 2020-09-27 deadline for an initial review of their proposal. Most of them were quite good, and needed only some small changes. 
- A couple of students tried to use R to do all of the ingestion work, including dropping the first row from the data set and to pull it from the website directly. The best way I know how to do that is shown below. All it requires is `library(tidyverse)` and an active Internet connection to work.

```
data_url <- "https://www.countyhealthrankings.org/sites/default/files/media/document/analytic_data2020_0.csv"
chr_raw <- read_csv(data_url, skip=1, guess_max = 4000)
```

On 2020-09-27, I adjusted the Project Proposal Example to incorporate this idea, and to incorporate several other good ideas, like...

- carefully specifying which variable will be your outcome
- separating out the codebook, some data checks and the proposal requirements from the data development
- fixing a typo or two

So I encourage you to use [that version (Rmd here)](https://raw.githubusercontent.com/THOMASELOVE/431-2020/master/projects/projectA/example_projectA_proposal/love-example-projectA-proposal.Rmd). HTML is still at https://rpubs.com/TELOVE/projA-proposal-example-431-2020. Links now fixed.

5. Some [Quiz 1 information is available now](https://github.com/THOMASELOVE/431-2020/blob/master/quizzes/quiz1/quiz1.md).

6. I updated the [Course Notes](https://thomaselove.github.io/431-notes/) to fix some typos in Chapters 11, 21 and 22. Thank you!

7. Thomas Mock had a post 2020-09-26 on "[Functions and Themes for gt tables](https://themockup.blog/posts/2020-09-26-functions-and-themes-for-gt-tables/)" which includes some beautiful work, if you're interested, including ways to mimic some of ESPN's and FiveThirtyEight's tables.

8. [Big Book of R](https://www.bigbookofr.com/) from Oscar Baruffa is a reference containing links to about 100 freely-available R-related programming books, including many of my favorites.

## What Should I Be Working On?

1. [Minute Paper after Class 11](https://github.com/THOMASELOVE/431-2020/blob/master/minutepapers) is due Wednesday 2020-09-30 at Noon.
2. [Project A](https://thomaselove.github.io/431-2020-projectA/), in particular the Proposal, which is due 2020-10-02. You want [this version](https://raw.githubusercontent.com/THOMASELOVE/431-2020/master/projects/projectA/example_projectA_proposal/love-example-projectA-proposal.Rmd).
3. Reading: by 2020-10-02, you'll need to have finished the Leek text and chapters 8-9 of Spiegelhalter.

## One Last Thing

We'll look for a moment at [the FiveThirtyEight 2020 Senate Election Forecast](https://projects.fivethirtyeight.com/2020-election-forecast/senate/). 

- If you're interested in more of the details of how these state-wide models work, [visit the methodology here](https://fivethirtyeight.com/methodology/how-fivethirtyeights-house-and-senate-models-work/).

### Other Organizations

Other organizations have predictive models for the 2020 Election.

- *The Economist* is analysing polling, economic and demographic data to predict America’s elections in 2020
    - [Presidential forecast](https://www.economist.com/us-election-2020) and an [explanation of how the model works](https://projects.economist.com/us-2020-forecast/president/how-this-works).
    - [Senate forecast](https://projects.economist.com/us-2020-forecast/senate) and [explanation of how the Senate model works](https://projects.economist.com/us-2020-forecast/senate/how-this-works).
    - [House forecast]() and [explanation of how their House forecast works](https://projects.economist.com/us-2020-forecast/house/how-this-works).
- [270 to Win](https://www.270towin.com/2020-election-forecast-predictions/) aggregates forecasts from several other organizations. [Here are the Senate forecasts, for instance](https://www.270towin.com/2020-senate-election-predictions/), most of which are ratings, rather ther than probabilistic.
- The *New York Times* Upshot provides [analysis of the day in polls](https://www.nytimes.com/live/2020/presidential-polls-trump-biden)


### More from FiveThirtyEight

- There are a LOT of polls in the field right now. Here's an [update on the latest polls](https://projects.fivethirtyeight.com/polls/) from FiveThirtyEight.
- FiveThirtyEight's podcasts are helpful to me, too. In particular, the [politics podcast](https://fivethirtyeight.com/tag/politics-podcast/) has occasional Model Talk sessions where Nate discusses the models in a lot of detail in what I find to be a compelling way.
    - from 2020-09-18: "[Why Our Forecast Says Democrats Are Slightly Favored To Win The Senate](https://fivethirtyeight.com/videos/why-our-forecast-says-democrats-are-slightly-favored-to-win-the-senate/)" is most directly relevant to what we'll look at today.
- A few tweets from Nate Silver this morning: [this one](https://twitter.com/NateSilver538/status/1310936019370471426) is about how the presidential forecast reacts to debates, and [this one](https://twitter.com/NateSilver538/status/1310946004041191430) is about the idea that the election could come down to the Supreme Court. 
- Included in that last stream of tweets is a list of the issues 538 sees now as most likely to dominate the final month of the campaign in addition to the debates, quoted below.

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class11/images/538_issues.png)
