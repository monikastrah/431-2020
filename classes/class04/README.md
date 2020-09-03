# 431 Class 04: 2020-09-03

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

> **Without data, you're just another person with an opinion.** (W. Edwards Deming)

## Today's Slides

- Class 04 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class04/431_class-04-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class04/431_class-04-slides_2020.Rmd).

## Announcements

1. Dr. Love will present some [reactions to the Minute Paper after Class 03](https://github.com/THOMASELOVE/431-2020/tree/master/minutepapers).
    - Depending on when you completed the Minute Paper, you may have been asked about Leek twice and Spiegelhalter not at all. Sorry about that mistake.
2. **What should I do if an emergency arises?**
    - If an emergency arises that will keep you from timely completion of work that has a deadline, like a lab, minute paper, or the like, send an email directly to Dr. Love saying "I have an emergency that will keep me from completing (*list things you're worried about completing*) in a timely fashion. I will contact you again when I am able to make plans." 
    - Dr. Love will respond with "OK" and temporarily excuse you from things until **you** send a "re-connection" email to make plans for making up the work you missed, at which time he'll evaluate the situation and together you can make that plan. At no time do you owe us any information about your health or the nature of the emergency.
    - Essentially, doing this will press PAUSE on Dr. Love worrying or pestering you about deadlines until you email him again. 
    - Dr. Love's email address remains `Thomas dot Love at case dot edu`.
    - This information is now also available in our [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) thanks to the most recent revision.
3. The best cheat sheets for working with our tools, in my opinion, are the [R Studio Cheatsheets](https://rstudio.com/resources/cheatsheets/).  The ones I use most often are (all are PDF downloads):
    - [Data Visualization](https://github.com/rstudio/cheatsheets/raw/master/data-visualization-2.1.pdf) with `ggplot2`, 
    - [Data Transformation](https://github.com/rstudio/cheatsheets/raw/master/data-transformation.pdf) with `dplyr`, 
    - [R Markdown](https://github.com/rstudio/cheatsheets/raw/master/rmarkdown-2.0.pdf), and the [R Markdown Reference Guide](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf), 
    - [Factors with forcats](https://github.com/rstudio/cheatsheets/raw/master/factors.pdf), 
    - the [RStudio IDE](https://github.com/rstudio/cheatsheets/raw/master/rstudio-ide.pdf), and 
    - [Data Import](https://github.com/rstudio/cheatsheets/raw/master/data-import.pdf).
4. Don't forget about the other great resources provided by [RStudio Education](https://education.rstudio.com/) including [this Beginner pathway](https://education.rstudio.com/learn/beginner/).
    - The [RStudio Primers](https://rstudio.cloud/learn/primers) are especially helpful for those of you for whom R or the tidyverse are new things, and who like interactive tutorials. 
        - The ones I would recommend most strongly are: [The Basics](https://rstudio.cloud/learn/primers/1), [Work with Data](https://rstudio.cloud/learn/primers/2), [Visualize Data](https://rstudio.cloud/learn/primers/3) and [Tidy Your Data](https://rstudio.cloud/learn/primers/4), all of which would be helpful to review before our first Quiz.
    - I strongly recommend the book [R for Data Science](https://r4ds.had.co.nz/) which is incredibly helpful in thinking about how to do data science effectively.
5. The [R Bootcamp for the tidyverse](https://r-bootcamp.netlify.app/) looks very useful. 
    - Chapters include [The magic of ggplot2](https://r-bootcamp.netlify.app/chapter1), [ggplot2 and categorical data](https://r-bootcamp.netlify.app/chapter2), [Introduction to dplyr](https://r-bootcamp.netlify.app/chapter3), [The Whys and Hows of Tidy Data](https://r-bootcamp.netlify.app/chapter4), and [Simple Stats and Modeling with broom](https://r-bootcamp.netlify.app/chapter5), all of which should be helpful in the early stages of 431 (classes 1-14 or so.)
6. You might also be interested in the series of modules on statistics and R found at [Teacups, Giraffes and Statistics](https://tinystats.github.io/teacups-giraffes-and-statistics/index.html). Included are modules on the Normal distribution, measures of center and spread, covariance and correlation and standard error.
7. You might be interested in a new video series entitled "[The Philosophy of Data Science](https://www.podofasclepius.com/philosophy-of-data-science)" sponsored by Pod of Ascelepius (which is a health care technology podcast.)  The series is aimed at early-career statisticians and data scientists, to provide an in-depth understanding of how scientific reasoning is essential to good practical data science. It is open to anyone interested in improving their scientific skills as a data scientist or is just generally interested in critical scientific reasoning.

## What Should I Be Working On?

- The [Course Syllabus](https://thomaselove.github.io/431-2020-syllabus/) includes a small task that needs to be completed by NOON **Friday** 2020-09-04. 
    - As of 11:30 AM on 2020-09-03, I have this from 51 people, and I've responded via email to each of you who've completed this task.
- [Lab 01](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab01/lab01.md) is due on Monday 2020-09-07 at 9 PM (Be sure to complete all four parts.)
    - As of 11:30 AM on 2020-09-03, I have:

Lab 01 | Part 1 (video) | Part 2 & 3 (essays) | Part 4 (survey)
:------: | :------: | :----------------: | :---------:
Responses | 14 | 13 | 25

- [Lab 02](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab02/lab02.md) is due 2020-09-14 (You should be able to do all 7 parts now.)
- Readings: check the [Calendar](https://thomaselove.github.io/431/calendar.html) to be sure that you're up to date with Leek and also with Spiegelhalter (see Lab 02, question 7.)
    - In the [Course Notes](https://thomaselove.github.io/431-notes/), you should read as you like. We're covering material in class that is also covered in Chapters 1-6.
- TA office hours are available every day of the week (see the Announcements folder in [Canvas](https://canvas.case.edu) for schedule and zoom information) and that [Piazza](https://piazza.com/case/fall2020/pqhs431) is always open. We want to help you!
- When asking a question of a TA or on Piazza, be sure to provide enough information so we can help you. 
    - For an R question, this will usually mean including your entire R Markdown file (not just a part of it), and a screenshot of the error you're getting, for example.
- As of 11:30 AM on 2020-09-03, just one student is still unconnected to the Piazza forum for the course. If you have any questions, please let me know.

## OPTIONAL: The [COVID-19 page](https://github.com/THOMASELOVE/covid19)

I will occasionally post links to things at a page about COVID-19 and news related to it that you might be interested in. I won't discuss this material in regular class sessions, and it's completely optional. Visit the page at https://github.com/THOMASELOVE/covid19.

## One Last Thing

![https://xkcd.com/2341/](https://imgs.xkcd.com/comics/scientist_tech_help.png) [Scientist Tech Help, from XKCD](https://xkcd.com/2341/)
