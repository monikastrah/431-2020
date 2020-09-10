# Movies: Breakout Session Materials for Class 06 (2020-09-10)

I've created a small data set called [movies_2020-09-10.csv](https://github.com/THOMASELOVE/431-2020/blob/master/classes/movies/data/movies_2020-09-10.csv) about the 66 movies people listed in response to [my request in Section 17 of the syllabus](https://thomaselove.github.io/431-2020-syllabus/movies.html) and several characteristics for each movie gathered from the [Internet Movie Data Base](https://www.imdb.com/) (IMDB). We're going to use this example several times this semester.

As an example, for my favorite film, this is the screen I would have used to gather the data...

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

## Task for today's first breakout session (Class 06)

You'll be reporting the results of your work using the google form found at http://bit.ly/431-2020-movies-1. One person in your group should fill out the form.

In brief, you'll ...

1. Identify **two** exploratory questions about films in this sample that could be addressed using the five key variables (`year`, `imdb_categories`, `imdb_ratings`, `imdb_stars` and `length`) that are contained in [the current version of the movies data](https://github.com/THOMASELOVE/431-2020/blob/master/classes/movies/data/movies_2020-09-10.csv).
    - A good question (a) explores relationships involving two or more variables from the data set (b) lets us use data from all (or almost all) of the films and (c) ends with a question mark.
    - As an example that fits at least (a) and (c), we might ask "Do dramas last longer than comedy films?" which could be answered using the `length` and `imdb_categories` variables, although (b) is a problem since some films are not listed as either Drama or Comedy.

2. Look at the list of films on the list. What is the first film on the list (alphabetically) that all of the members of your breakout group have seen? If there isn't a film on the list that you've all seen, write in "We couldn't find one."


## What will we do in upcoming breakout sessions

- In one session, you'll work in a group to answer some of the exploratory questions posed today using R and RStudio.
- In another, you'll gather in new breakout groups to identify two additional variables available on the internet (and not necessarily on IMDB) that could be added to the data to expand on what could be studied here in an interesting way. 
    - For each variable, we're hoping you will identify a URL on the internet where those data seem to be available.
    - Your first variable should be **categorical** (with 2-10 mutually exclusive and collectively exhaustive levels, and without a lot of missing data.) 
        - An example (that you shouldn't use since I have it in a separate file already) would be the Motion Picture Association's Rating (G, PG, PG13, R, NC17 or Not Rated) which is also available on IMDB's page for the film. For my favorite film, this is R.
        - The categories in your suggested variable can be either ordinal or nominal.
    - The other variable you suggest should be **quantitative**, so that it takes values across a range of numerical results, and has units of measurement. 
        - An example (that you shouldn't use since I have it already) would be the percentage of raters on IMDB that rated the film at the maximum level (10 stars) which is a percentage ranging from 0% to 100%. This is available by clicking on the number of people who rated the film on the main IMDB page, and for my favorite film, this would be 43.0%.
        - In this work, we'll require a quantitative variable to be any quantity that has at minimum 11 different observed values in our set of films. Eleven is too small a count, really, to declare something "quantitative" in practice, but we'll make the best of it.
- And more...
