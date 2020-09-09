# 431 Class 06: 2020-09-10

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

> **Quote to come.** 

## Today's Slides

- Class 06 slides will be available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class06/431_class-06-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class06/431_class-06-slides_2020.Rmd).

## For Today's Breakouts

- I've created a small data set (`movies_2020.csv`) containing the list of movies people listed in response to [my request in Section 17 of the syllabus](https://thomaselove.github.io/431-2020-syllabus/movies.html) and several characteristics of those films gathered from the [Internet Movie Data Base](https://www.imdb.com/) (IMDB). For instance, for my favorite film this is the screen I would use to gather the data...

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class06/images/godfather2_imdb.png)

and here are the results that would produce:

Description | Variable | Value
----------: | -------- | ---------:
Film Name | `film` | The Godfather, Part II
Students selecting this film | `mentions` | 0
Year of release | `year` | 1974
Film Categories (up to 3) | `imdb_categories` | Crime, Drama
Number of Star Ratings (IMDB) | `imdb_ratings` | 1099840
Weighted Average Rating (IMDB) | `imdb_stars` | 9.0
Length of Film (in minutes) | `length` | 202

## Announcements

1. [Feedback on the Minute Paper after Class 05](https://github.com/THOMASELOVE/431-2020/tree/master/minutepapers) is now available.
2. What is Dr. Love's main source when he wants to remember how to do something in R? 
    - The [R Graphics Cookbook](https://r-graphics.org/) from Winston Chang. [R Graphics Cookbook](https://r-graphics.org/) is a practical guide that provides **more than 150 recipes** to help you generate high-quality graphs quickly, without having to comb through all the details of R’s graphing systems. Each recipe tackles a specific problem with a solution you can apply to your own project, and includes a discussion of how and why the recipe works.
    - I recommend all of it, especially the chapters on [R Basics](https://r-graphics.org/chapter-r-basics), [Getting Your Data in Shape](https://r-graphics.org/chapter-dataprep), and [Summarized Data Distributions](https://r-graphics.org/chapter-distribution).
3. As part of the Lab 01 Survey, several folks described potential data sets they might want to use for projects in 431 and 432. I built [some comments on these project data ideas](http://bit.ly/431-2020-lab01-project-data-ideas). Please take a look.
4. [Kelly Bodwin](https://twitter.com/kellybodwin/status/1303083136046170112) started an interesting stream on Twitter crowdsourcing articles/papers/books/chapters that people in the field thought a first-year statistics student should absolutely read, or that they wished they'd seen at the start of their statistics / data science career. 
    - My list is part of the [Course Syllabus](https://thomaselove.github.io/431-2020-syllabus/) but several people [responded to Kelly](https://twitter.com/kellybodwin/status/1303083136046170112) with interesting suggestions.
    - One common suggestion: Nate Silver's *The Signal and the Noise* which we've read in 431 in the past and will read in 432 this year.
5.  It's by no means mandatory, but you might want to visit RStudio Community at https://community.rstudio.com/ which is a generally useful place, especially after the course ends and you want to have a community to discuss issues with that's friendly.
6. Depending on where you are in the Leek reading, you may have developed a curiosity about Bland-Altman plots, especially because there's nothing in our Course Notes about them, at least not yet.
    - Here's a [nice introduction to one way of accomplishing these plots in R](https://cran.r-project.org/web/packages/BlandAltmanLeh/vignettes/Intro.html).

## What Should I Be Working On?

1. [Lab 02](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab02/lab02.md) is due to Canvas on Monday.

## One Last Thing

The American Statistical Association and The New York Times have an ongoing collaboration entitled "[What's Going On In This Graph?](https://www.nytimes.com/column/whats-going-on-in-this-graph)" which is a great way to force yourself to think through some interesting visualization challenges and get a bit inspired. Here's one I particularly liked [from 2017-10-10](https://www.nytimes.com/2017/10/09/learning/whats-going-on-in-this-graph-oct-10-2017.html):

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class06/images/nyt_2017-10-10.png)

### Questions we might ask here...

1. What do the axis labels tell us about what is being shown?
2. How would you describe the relationship between the variables under study?
3. What does the diagonal line indicate about the pattern?
4. What characterizes the foods (granola, coconut oil, granola bats and frozen yogurt, for example) which appear in the lower right portion of the graph?
5. Do these results surprise you or confirm your prior beliefs about the phenomenon under study?
6. Is there anything else worth noting about the graph?

