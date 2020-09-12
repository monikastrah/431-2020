# Movies: Breakout Session Materials for Class 07 (2020-09-15)

As we discussed last time, I've created the [movies_2020-09-10.csv](https://github.com/THOMASELOVE/431-2020/blob/master/classes/movies/data/movies_2020-09-10.csv) data set about the 66 films people listed in response to [my request in Section 17 of the syllabus](https://thomaselove.github.io/431-2020-syllabus/movies.html) which includes several characteristics for each film gathered from the [Internet Movie Data Base](https://www.imdb.com/) (IMDB). The first three variables in the data set are:

Description | Variable 
----------: | -------- 
`film_id` | Numeric code indicating alphabetical order of the films
`film` | Film's Title (IMDB served as the authority here)
`mentions` | Students who sent me the poster of this film (63 are 1, the other 3 are 2)

## Results of our first breakout session (Class 06)

Last time, I asked groups to identify exploratory questions about films in this sample that could be addressed using five key variables:

Variable | Description
------- | -------------------------------------------------
**year** | Year of release 
**imdb_categories** | Film Categories (up to 3) 
**imdb_ratings** | Number of Star Ratings (IMDB) 
**imdb_stars** | Weighted Average Rating (IMDB) 
**length** | Length of Film (in minutes) 

I described a good exploratory question as one which:

- explores relationships involving two or more variables from the data set, and
- lets us use data from all (or almost all) of the films, and 
- ends with a question mark.

Each of the ten breakout groups generated two questions. I've [listed the 20 proposed questions here](https://github.com/THOMASELOVE/431-2020/blob/master/classes/movies/breakout1_results.md).

## Task for today's second breakout session (Class 07)

Several common themes emerged  in your proposals. We'll explore two of them today in our breakout sessions.

1. **Do older films have more IMDB ratings?**
    - "Do older movies have more numbers of star ratings at IMDB?"
    - "Does year of movie release correlate with number of ratings?"
    - "Do the older movies have more ratings when compared to the newer movies released?"
    - "Is there a relationship between the year of release and number of ratings?"
    - "Do more recent films have more ratings?"
2. **Do longer films receive higher star ratings?**
    - "Are longer movies rated higher?"
    - "Does the length of a movie relate to its star rating?"
    - "Does length of the movie correlate with the weighted average IMDB rating?"

To help support this work, Dr. Love has completed an analysis of two other questions that were suggested, specifically those listed below.

- **Do films with more IMDB ratings have higher star ratings?**
    - What's the association between the imdb_ratings and imdb_stars?
    - Is there an association between the number of ratings versus number of stars?
- **Which movie categories (also known as *genres*) have the highest star ratings?**
    - "What is the category of film with the highest average IMDB rating?"
    - "Which category of movies typically get the highest rating?"
    - "Does the number of categories that a film is listed under correlate with star ratings?"

## What will we do in upcoming breakout sessions? Expand the data set. 

- We'll develop, administer, and analyze a survey of this class (students + TAs) regarding these films.
    - Along the way, we'll address whether there is a film on this list that everyone in the class (including Dr. Love) has seen. Some early evidence regarding this issue [is available here](https://github.com/THOMASELOVE/431-2020/blob/master/classes/movies/breakout1_results.md#which-is-the-first-movie-youve-all-seen-alphabetically).
- You'll gather in new breakout groups to identify additional variables available on the internet (not necessarily on IMDB) that could be added to the data to expand on what could be studied here in an interesting way. 
    - For each variable, we're hoping you will identify a URL on the internet where those data seem to be available.
    - Your first variable should be **categorical** (with 2-10 mutually exclusive and collectively exhaustive levels, and without a lot of missing data.) 
        - An example (that you shouldn't use since I have it in a separate file already) would be the Motion Picture Association's Rating (G, PG, PG13, R, NC17 or Not Rated) which is also available on IMDB's page for the film. For my favorite film, this is R. I'll note that only four of these six possible categories are actually relevant to our 66 films.
        - The categories in your suggested variable can be either ordinal or nominal.
    - The other variable you suggest should be **quantitative**, so that it takes values across a range of numerical results, and has units of measurement. 
        - An example (that you shouldn't use since I have it already) would be the percentage of raters on IMDB that rated the film at the maximum level (10 stars) which is a percentage ranging from 0% to 100%. This is available by clicking on the number of people who rated the film on the main IMDB page, and for my favorite film, this would be 43.0%.
        - In this work, we'll require a quantitative variable to be any quantity that has at minimum 11 different observed values in our set of films. Eleven is too small a count, really, to declare something "quantitative" in practice, but we'll make the best of it.
