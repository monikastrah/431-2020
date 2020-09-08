# 431 Class 05: 2020-09-08

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

> My biggest regret as a 1st year grad student was pretending to say I knew X when I didn't really. Learning to say "No, tell me about X" became a gateway for (1) learning stuff, (2) getting to know a person, and (3) learning how to say no in other areas of my life. - [Josephine Lutko](https://twitter.com/JosephineLukito/status/1303081582492889088)

## Today's Slides

- Class 05 slides will be available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class05/431_class-05-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class05/431_class-05-slides_2020.Rmd).

## Today's Main Examples

- Dr. Love used R Markdown to explore [your responses to the survey (part 4) of Lab 01](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab01/survey-results-2020/README.md), which we'll discuss at some length in class today.
    - We'll also discuss the [Answer Sketch and Grading Rubric for Lab 01](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab01/README.md), which also contains some survey-based analyses of the Attitudes Towards Statistics scales.
- The [CWRU Color Guide](https://case.edu/umc/our-brand/visual-guidelines/color) is something I'll mention today in class.
- We'll be starting a discussion of data from [NHANES](https://www.cdc.gov/nchs/nhanes/index.htm) today, as well. The Course Notes also make use of similar data in several chapters.
- Today's cartoon (from the Slides) is from [PhD Comics](http://phdcomics.com/comics/archive.php?comicid=1531).

## Announcements

1. Instructions for Project A will be available by Saturday morning.
2. So far this semester, Dr. Love (and the TAs) have been chasing you down via email if something isn't submitted on time, or isn't submitted correctly, and reminding you about deadlines outside of class time. Enjoy it while it lasts, because we intend to (essentially) stop doing that after [Lab 02](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab02/lab02.md).
3. Detailed instructions for downloading individual .csv or .Rmd files using various browser and operating system combinations are now found [here on our Data and Code page](https://github.com/THOMASELOVE/431-data/blob/master/README.md#detailed-steps-for-downloading-individual-csv-or-rmd-files-from-github).
4. Chapters 7-10 in the [Course Notes](https://thomaselove.github.io/431-notes/) are now available. All 10 Chapters so far touch on issues of visualization and data management that we are discussing in class through this week.
5. I adjusted the late penalty for Labs in the Syllabus.
    - For each Lab, on-time submission gets you detailed TA comments plus up to 100% of available points.
    - I'll post an Answer Sketch by noon on the day after each Lab is due. Submission before I do that gets you some TA comments plus up to 90% of available points.
    - Submissions after that (but within a week of the deadline) will get minimal (if any) TA comments plus up to 75% of available points on the Lab.
    - Remember that your lowest two Lab grades will be dropped before we calculate your Lab average.
    - People having trouble with technology issues / remote learning / etc. can contact Professor Love via email to discuss, but the Labs will go on without you, according to these rules. You should submit your work as soon as you can.
6. I corrected some typographical errors in [Lab 02](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab02/lab02.md). I would be surprised if this changes any of your responses if you've already worked on the Lab. Lab 02 submission will open today (2020-09-08) on Canvas.
7. [Lab 03](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab03/lab03.md) and [Lab 04](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04/lab04.md) are now available, for those of you eager to get ahead of things.
8. I encourage you to adjust your email settings for the class on [Piazza](https://piazza.com/case/fall2020/pqhs431) if the messages become overwhelming. If you click on the gear at the top right of any Piazza screen, then select Account Settings and scroll down to Class & Email Settings, you can edit your email notifications. 
    - The Daily Digest seems like a good option for new Questions or Notes from my perspective, although I recommend Real Time for updates to Questions or Notes you follow. 
    - Any announcements I designate as necessary reading for the whole class on Piazza will be sent to you via email immediately regardless of your settings.
9. The [modelsummary](https://vincentarelbundock.github.io/modelsummary/index.html) package is now a recommended package to install in the class. I've modified [our R Packages list](https://thomaselove.github.io/431/r_packages.html) appropriately. 
    - The package provides some great tools for creating summary tables (including things like Table 1) for models and tibbles. More to come, but you can see lots of examples at the [github repository for the package](https://vincentarelbundock.github.io/modelsummary/index.html).
    - I'll demonstrate a few of the capacities of this in the survey example today.
    - Some `modelsummary` functions, especially functions used by the `datasummary` tools, fight with functions in the `Hmisc` package, so there can be some problems if you have `Hmisc` or `rms` (which loads `Hmisc`) loaded when you try to use `modelsummary` and vice versa. We'll usually avoid this by looking at either `modelsummary` or `rms` tools in a particular example. 

## What Should I Be Working On?

As always, check the [Course Calendar](https://thomaselove.github.io/431/calendar.html) for links to and deadlines for all deliverables (labs, minute papers, quizzes and projects.)

1. There is a **Minute Paper after Class 05** at http://bit.ly/431-2020-minute-05, due Wednesday (tomorrow) at noon. The link is also available on [the Minute Paper page](https://github.com/THOMASELOVE/431-2020/blob/master/minutepapers/README.md). 
    - Please remember to do this, as it's an important part of your class participation grade, and it provides very important feedback to Dr. Love and the TAs as we make course adjustments.
2. [Lab 02](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab02/lab02.md) is the next deliverable after the Minute Paper, and requires some coding (and knitting) in R Markdown. You will also need to have read Spiegelhalter Chapters 1-3 to complete it.

## One Last Thing

!()[https://github.com/THOMASELOVE/431-2020/blob/master/classes/class05/images/g2.png]

In section 17 of the Course Syllabus, I [asked you to send me a poster from your favorite movie](https://thomaselove.github.io/431-2020-syllabus/movies.html).  69 of you did, and this included three movies that were mentioned by two students each, specifically: About Time (2013), Inception (2010) and La La Land (2016). We'll get back to your data, but for now, I'll list my twenty favorite movies, [according to my account on Flickchart](https://www.flickchart.com/), three of which were also mentioned by students in the class.

1. The Godfather Part II (1974)
2. The Manchurian Candidate (1962)
3. The Sting (1973)
4. Sleuth (1972)
5. The Godfather (1972), which was mentioned by one student in the class
6. Dead Again (1991)
7. Field of Dreams (1989)
8. Die Hard (1988)
9. The Dark Knight (2008), which was mentioned by one student
10. Ocean's Eleven (2001)
11. When Harry Met Sally (1989), which was also mentioned by one student
12. Forrest Gump (1994)
13. Citizen Kane (1941)
14. Bull Durham (1988)
15. The Princess Bride (1987)
16. Murder on the Orient Express (1974)
17. The Prestige (2006)
18. The Untouchables (1987)
19. The Usual Suspects (1995)
20. The Hudsucker Proxy (1994)

