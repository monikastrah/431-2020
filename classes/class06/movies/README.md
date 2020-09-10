# Breakout Session Materials for Class 06 (2020-09-10)

I've created a small data set (`movies_2020.csv`) containing the list of movies people listed in response to [my request in Section 17 of the syllabus](https://thomaselove.github.io/431-2020-syllabus/movies.html) and several characteristics of those films gathered from the [Internet Movie Data Base](https://www.imdb.com/) (IMDB). 

As an example, for my favorite film this is the screen I would have used to gather the data...

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

## Questions for the first breakout session

1. Identify a researchable question that could be addressed using these data.
2. Brainstorm to identify two additional variables available on the internet (and not necessarily on IMDB) that could be added to this data set to expand on what could be studied here in an interesting way. 
    - For each variable, we're hoping you will identify a URL on the internet where those data seem to be available.
    - Your first variable should be **categorical** (with 2-10 mutually exclusive and collectively exhaustive levels, and without a lot of missing data.) 
        - An example (that you shouldn't use as your team's example) would be the Motion Picture Arts Association's Rating (G, PG, PG13, R, NC17 or Not Rated) which is also available on the front page of IMDB for the film. In the case of my favorite film, this would be R.
        - The categories in your suggested variable can be either ordinal or nominal.
    - The other variable you suggest should be **quantitative**, so that it takes values across a range of numerical results, and has units of measurement. 
        - An example (that you shouldn't use as your team's example) would be the percentage of raters on IMDB that rated the film at the maximum level (10 stars) which would then be a percentage measure ranging anywhere from 0% to 100%. This is available by clicking on the number of people who rated the film on the main IMDB page, and for my favorite film, this would be 43.0%.
        - In this work, we'll require a quantitative variable to be any quantity that has at minimum 11 different observed values in our set of films. Eleven is too small a count, really, for most quantities, but we'll work with it.
