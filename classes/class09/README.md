# 431 Class 09: 2020-09-22

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class09/images/normalitytesttweet.png)

## Today's Slides

- Class 09 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class09/431_class-09-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class09/431_class-09-slides_2020.Rmd).

## Meeting Our Colleagues

1. I've created a true Shared Drive on Google called **431 Fall 2020 Dr Love and Students** that you should now all have access to (but only when logged into Google via CWRU). Let us know if you have any trouble accessing that material.
    - Among other things, you should find a folder of **Introductory Student Videos**. Starred videos feature the people we've already met. 
    - Today, we'll meet students numbered 70-72 and 13-15, specifically **Peng Zhang, Chenya Zhao, Lin Zhu, Jane Hinkle, Leila Hojat and Natasha Ingles**.

## Announcements

1. There will be a [Minute Paper after Class 09](https://github.com/THOMASELOVE/431-2020/tree/master/minutepapers). Please complete it by Noon Wednesday 2020-09-23.
2. [Grades for Lab 02](https://bit.ly/431-2020-grades) are now posted. They are part of the shared Google Drive, so you'll have to log in via CWRU to see them.
3. The [Lab 03 answer sketch](https://github.com/THOMASELOVE/431-2020/tree/master/labs/lab03/sketch) is now available in R Markdown and PDF.
4. We welcome a new Teaching Assistant, Claudia Cabrera, who has extensive experience as a TA for 431-432. Read more about Claudia in [the Syllabus](https://thomaselove.github.io/431-2020-syllabus/), and look for her in our new Monday 3-4:30 PM TA Office Hours, and on Piazza.
5. For those of you looking for a paper you can cite if you need a reference about "not testing for Normality" being an OK idea, I recommend [The importance of the Normality assumption in public health data sets](https://pubmed.ncbi.nlm.nih.gov/11910059/) by Thomas Lumley, Paula Diehr, Scott Emerson and Lu Chen.
    - I also recommend [this blog post](https://notstatschat.rbind.io/2019/02/09/what-have-i-got-against-the-shapiro-wilk-test/) specifically about the problems inherent in one particular type of test (the Shapiro-Wilk test.) 
6. You can still [sign up for the mailing list for The Philosophy of Data Science Series](https://docs.google.com/forms/d/1YDZUkLmzIiujcaEVl3JkjIffKSwK_orFMjEkkyLvFUQ/), which now has [a welcome video on YouTube](https://www.youtube.com/watch?v=yeHEfHN39Cc). The next session is about "Critical Reasoning in Medical Machine Learning".
7. [Better Health Partnership](http://betterhealthpartnership.org/), where I was founding Data Director, and now serve as Chief Data Scientist, has a webinar Wednesday 2020-09-23 at Noon entitled [Addressing Bias within Health Care Systems](http://betterhealthpartnership.org/convening_2020_date5.asp) about some of its work with [First Year Cleveland](https://www.firstyearcleveland.org/). If you're interested, please [register or learn more at this link](http://betterhealthpartnership.org/convening_2020_date5.asp). 
8. I've added **NEW** [Course Notes](https://thomaselove.github.io/431-notes/) Chapters 11-18, and edited earlier sections (especially Section 5.4.3 regarding kurtosis) to clean up some additional errors. I expect the complete 431 Notes to include about 30 Chapters, eventually.
9. I've added two very important pieces to the [Project A examples](https://thomaselove.github.io/431-2020-projectA/examples.html) page.
    - This includes a 30-minute video about **getting the data ready and using RStudio projects and R Markdown most effectively**, and 
    - An **example of a proposal**, using 2019 data, and including the R Markdown to produce [this HTML result](https://rpubs.com/TELOVE/projA-proposal-example-431-2020).

## What Should I Be Working On?

1. Please complete the [Minute Paper after Class 09](https://github.com/THOMASELOVE/431-2020/tree/master/minutepapers) by Wednesday 2020-09-23 at Noon. Thank you.
2. Your [Lab 03](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab03/lab03.md) submission needed to include:
    - a working R Markdown file, produces
    - the submitted HTML file, in which we can see all of your code (so that you have not used `echo = FALSE`).
    - so if yours doesn't meet that standard, please fix it and resubmit today.
3. Reading: The most urgent thing is reading [Jeff Leek's article: Finally, a Formula for Decoding Health News](https://fivethirtyeight.com/features/a-formula-for-decoding-health-news/) from FiveThirtyEight which is a big part of [Lab 04](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04/lab04.md). By the time you turn in your project proposal and receive the Quiz on 2020-10-02, you'll need to have finished the Leek text and chapters 8-9 of Spiegelhalter.
4. [Lab 04](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04/lab04.md) requires some searching through the literature in Questions 1-5. Questions 6-8 are about the [Palmer Penguins](https://github.com/allisonhorst/palmerpenguins), from [Chapter 2 of the Course Notes](https://thomaselove.github.io/431-notes/looking-at-the-palmer-penguins.html).
5. The [Project A](https://thomaselove.github.io/431-2020-projectA/) Proposal, which is due 2020-10-02. I suggest a visit to [the Examples page](https://thomaselove.github.io/431-2020-projectA/examples.html) to watch the video (if you like) and use the R Markdown Example I've provided as a template. Those two tools should be just about all you need to get your proposal moving well.
    - If you are interested in working with a partner, getting that figured out soon will be helpful. We'll ask about it on [today's Minute Paper](https://github.com/THOMASELOVE/431-2020/tree/master/minutepapers).

## One Last Thing

Let's take a first look today at the [2020 US Election Forecast at FiveThirtyEight.com](https://projects.fivethirtyeight.com/2020-election-forecast/).
