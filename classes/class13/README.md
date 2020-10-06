# 431 Class 13: 2020-10-06

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class13/images/gelfand.png)

## Today's Slides

- Class 13 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class13/431_class-13-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class13/431_class-13-slides_2020.Rmd).

## Who Will We Meet Today?

- **Emma Wallens, T'yasah Walser, Mia Wang, Ping Wang, Davis Weaver** and **Kristi Westphaln** (54-60 from the Introductory Student Videos in our Shared Google Drive)

## Announcements

1. **STILL TO COME**
    - Lab 04 results

2. Project A Proposal Review Status
    - 70 students have completed 55 initial proposals. 25 (19 individuals + 6 pairs, so 31 students) are approved, although many have comments to attend to.
    - The remaining 30 proposals (39 people) have deadlines of either 9 AM this morning (2 projects / 4 people) or 9 AM Thursday (the rest)
        - If you submit a revision before this deadline, we'll try to get to it as soon as possible. Canvas will mark all revisions as LATE but that doesn't affect our grades. If you need an extension on the revision for an emergency, just let Dr. Love know directly via email, please.
        - People who need additional revisions after this pass: deadline for those revisions will be 9 AM Tuesday 2020-10-13.
    - In producing the next iteration of your project, please follow the comments we've provided on Canvas. 
    - If you have questions about those comments or how to improve your work, please ask them in TA office hours, or via the channels we've made available for the Quiz.
    - In writing our comments on Canvas, we focused almost solely on things that needed to be fixed. If you're wondering whether we thought any of your work was good, the answer is Yes, we did, but we didn't (usually) bother to tell you about that in an effort to get the proposals back in your hands as quickly as possible. 
        - On more than a few occasions, in summarizing comments, I (Dr. Love) was more strident than I should have been, and/or more harsh in my criticism, and for that I apologize. I tend to get impatient when I have a long task ahead of me, and I did too much of this work late at night without a break. That was a mistake.
    - A few things came up repeatedly.
        - Each of the five variables you select can fill one and only one role (outcome, quantitative predictor 1, quantitative predictor 2, binary predictor, multi-categorical predictor.) 
        - When ingesting the data, use message = FALSE in your code chunk setup to suppress the column specifications details. In general, viewers of your HTML shouldn't see messages that are generated automatically but contain no useful content in your specific situation. If you are generating warnings (as opposed to messages) in R, you should fix the problem, rather than suppressing the warnings.
        - In creating categories, create categories people can remember. For example, if the median is 49.86, use 50 as your cutoff, so that people can understand this. Don't make things any more complicated for your eventual explanations of your analyses than they have to be.
        - It is your job to produce a document (and later a video as well) for an audience. That audience is interested in seeing your code that does things that matter, but is not interested in seeing your play-by-play with R. Edit your code to focus on the things worth writing about, or the things that are critical for your data development or analyses. This certainly includes all of the things I described in the checklist and the instructions, but doesn't include repeated checks on your data.
        - In HTML, you have all the vertical space in the world. Your horizontal space, though, is quite limited, so R Markdown creates (in HTML) lots of little scrolling windows for code. We want to avoid those as much as possible. So ... hit ENTER after every %>% and every + in a ggplot. When you have a long list of variables, like in the selection of your initial variables, hit ENTER after a comma somewhere in the middle so that you avoid the scourge of the scrolling window in the HTML result.
        - Spell check in RStudio and also look closely at the HTML that you've created at the end to make sure that the formatting works, and that things look nice.
        
3. This [Notes page for Quiz 1](https://github.com/THOMASELOVE/431-2020/blob/master/quizzes/quiz1/notes.md) contains responses to / hints about **some of** the questions students have asked.

4. How do we arrive at reasonable conclusions from data? From the stat150 project and [Kelly Bodwin](https://twitter.com/kellybodwin), here's some materials on [Making Arguments from Data](https://stat150.blog/post/01-evidence/) including many great links that may be of interest.

5. Ted Laderas gave an interesting talk at the R/Medicine 2020 virtual conference on [The MD in .rmd: Teaching Clinicians Data Analytics with R](https://www.youtube.com/watch?v=AexI0lZ7J-o) which you can watch on YouTube, if you're interested.
    - Ted has a newsletter called [Ready for R](https://tinyletter.com/ready4r/archive) where he shares lots of useful stuff.

6. The next [Prevention Research Center for Healthy Neighborhoods seminar](http://www.prchn.org/seminar) on 2020-10-14 will feature Rita Horwitz, President and CEO of Better Health Partnership, where I work as Chief Data Scientist. Rita will be presenting on [The Better Health Pathways Community Hub](https://cwru.zoom.us/webinar/register/WN_GtO_UX54QESF73sEfjEpgA) and follow that link to register if you are interested.

7. [Scientific Reasoning for Practical Data Science](https://www.youtube.com/watch?v=R6mq5Esjzfw) by Andrew Gelman is now available on YouTube, as part of the Philosophy of Data Science series.

8. A reminder that optional materials related to COVID-19 are archived at https://github.com/THOMASELOVE/covid19. If you see anything you think I should post there, let me know.

9. We revised the [Lab 04 instructions](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04/lab04.md) and the [Lab 04 sketch](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab04) to reflect a change regarding the scoring of Question 6 and also to fix a typo or two. The Lab was still graded out of a possible 105 points.

10. [Lab 05](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab05/lab05.md) is now available.

11. We have permanently cancelled the TA office hours formerly held from 10:30 AM to Noon on Thursday mornings.

## What Should I Be Working On?

1. [Quiz 1](https://github.com/THOMASELOVE/431-2020/blob/master/quizzes/quiz1/quiz1.md) due on Wednesday 2020-10-07 at Noon. Late work is not acceptable.
    - **Before you finalize your submission**, see the [Notes page for Quiz 1](https://github.com/THOMASELOVE/431-2020/blob/master/quizzes/quiz1/notes.md) to read notes responding to some of the questions students have asked about the Quiz.
2. [Project A](https://thomaselove.github.io/431-2020-projectA/) is due 2020-10-20 at Noon. More than half of you have a deadline for a revised proposal, still.
3. [Lab 05](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab05/lab05.md) is due 2020-10-26 at 9 PM.
4. Before Class 15 (2020-10-13), you should have read Spiegelhalter's Introduction and Chapters 1-9 (so this is adding in Chapters 5 and 6.)

## One Last Thing

In the slides today, we'll be spending a little time with [this 2015 article](https://fivethirtyeight.com/features/not-even-scientists-can-easily-explain-p-values/) by Christie Aschwanden at FiveThirtyEight.

- One of many articles that's worth a look if you have time (!) is [Science isn't Broken](https://fivethirtyeight.com/features/science-isnt-broken/) also by Christie Aschwanden at FiveThirtyEight, but we'll get to this more in Class 14.

