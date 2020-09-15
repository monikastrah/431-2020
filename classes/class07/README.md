# 431 Class 07: 2020-09-15

[Main Website](https://thomaselove.github.io/431/) | [Course Calendar](https://thomaselove.github.io/431/calendar.html) | [Syllabus](https://thomaselove.github.io/431-2020-syllabus/) | [Course Notes](https://thomaselove.github.io/431-notes/) | [Piazza & TA Office Hours](https://thomaselove.github.io/431/contact.html) | [Canvas](https://canvas.case.edu) | [Data and Code](https://thomaselove.github.io/431/data_index.html)
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :------------:
for everything | for deadlines | expectations | from Dr. Love | ways to get help | zoom information | for downloads

> It pays to keep wide awake in studying any graph. The thing looks so simple, so frank, and so appealing that the careless are easily fooled. (M. J. Moroney)

## Today's Slides

- Class 07 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class07/431_class-07-slides_2020.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class07/431_class-07-slides_2020.Rmd). These slides also include some materials for Class 08.

## Announcements

1. **Lab Policies** (Reminders: visit [Section 12.3 of the Syllabus](https://thomaselove.github.io/431-2020-syllabus/deliverables-assignments.html#labs) for more details.)
    - All Labs should be in by the deadline on the [Course Calendar](https://thomaselove.github.io/431/calendar.html). We don't give extensions on Labs. Instead, we use the following grading policy, also outlined [on the Labs page](https://github.com/THOMASELOVE/431-2020/blob/master/labs/README.md).
        - Labs turned in after the deadline but before noon the next day (when Sketch is posted) can receive up to 90% of available points. 
        - Labs turned in after the Sketch is posted, but within one week of the deadline can receive up to 75% of available points.
        - Your lowest two (of eight) Lab grades this term are dropped before we calculate your Lab grade for the course.
    - The [Lab Regrade Request Form](http://bit.ly/431-2020-lab-regrade-requests) is now available at http://bit.ly/431-2020-lab-regrade-requests. If you want Dr. Love to review your grade on a Lab, [fill out the form](http://bit.ly/431-2020-lab-regrade-requests) before 2020-12-10 at Noon. 
        - Dr. Love will open the form in mid-December after determining course grades. If your requested regrades on Labs could change your course grade, he'll review your regrade request in detail. If not, then he won't. 
        - The form is posted [to the Labs page](https://github.com/THOMASELOVE/431-2020/blob/master/labs/README.md#grading-errors-and-regrade-requests) and to the [Course Calendar](https://thomaselove.github.io/431/calendar.html).

2. The **Lab 02 Answer Sketch** is [now available](https://github.com/THOMASELOVE/431-2020/tree/master/labs/lab02).

3. **Grades on Lab 01** (and our records about the first two minute papers) are now available in the course grading roster at http://bit.ly/431-2020-grades. You'll need to log into Google via CWRU to see your scores and the comments left there by the Teaching Assistants. Your Lab Code identifies you in the roster. You should have received your three-digit Lab Code via email from Dr. Love either Sunday or Monday. (The email's subject is 431 Lab Code.) Lab grades and comments will be posted like this approximately one week after each Lab deadline.

4. **One of the stronger Lab 01 essays** Since we don't write answer sketches for essays, we will occasionally share a strong one from a student in the class. Here is an essay we liked from Part 3 of Lab 01. We liked the clear writing, and the use of the PPDAC structure to refine the problem, which reminded us of Spiegelhalter's examples.

> A problem I am interested in solving is whether virtual visits are a cost-effective way to deliver outpatient neurology care. Like the PICO (population, intervention, comparator, outcome) framework used to search scientific literature, the PPDAC structure helps me organize my inquiry such that ultimately conclusions can be drawn. It forces me to define all the elements of my question, plan the data-gathering process, select relevant and specific measures of cost-efficiency, perform the data collection, analyze the data, and then reach conclusions. For example, it might transform my original question into: Do remote synchronous communications between a patient and healthcare provider for outpatient neurology have the same episode-level costs as in-person visits? I would decide how to define and obtain costs related to the visits, collect that data, and analyze it. Then, I may be able to state whether costs around in-person and virtual visits are the same or not.

5. **Corrections to Course Notes**: Several enterprising students were good enough to let me know about some typographical and other errors in the Course Notes, Chapter 3. A new version was posted on 2020-09-13 that addresses those concerns. If you find a typo, **PLEASE** let me know either through the corrections folder in Piazza, or via direct email.

6. **Piazza: Inserting Files**: We notice that students don't seem to be including their R Markdown files when they ask questions on Piazza. When I create a new question on Piazza, I see a screen that looks like this:

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class07/images/piazza01.png)

and you can either click on the ![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class07/images/piazza02.png) icon or you can select Insert ... File to upload, for example, an R Markdown file.

7. **Piazza: Private Posts / Anonymity**: When posting to Piazza, we want to **discourage you from writing a private post to the instructors**, instead of one that everyone can see, especially since the first thing Dr. Love will do when he sees that is make it public anyway so that others can benefit from the answer. We promise - if you are confused - someone else is, too, and is counting on you to be brave enough to ask. Piazza also allows you to post questions anonymously, though, **frankly, it's hard to understand why you'd do that**, because all it really does is prevent you from getting some class participation credit for asking your question. 
    - We're all here to learn. **THERE ARE NO DUMB QUESTIONS!**
    - Do not be embarassed to ask a question that is "too simple". 
    - Simple questions are the easiest ones for us (and for your fellow students) to answer! So they make people happy because they can contribute.
    - A simple question is just a clear sign (to me, anyway) that my teaching needs to improve in that area. 
    - If you have a question that's too personal for Piazza for some reason, email Dr. Love.

8. **Tables in R**: There's a nice blog from Thomas Mock (2020-09-04) on [10+ Guidelines for Better Tables in R](https://themockup.blog/posts/2020-09-04-10-table-rules-in-r/) with links to many other excellent resources. The `gt` package figures substantially into the examples there, and [RStudio's gt page](https://gt.rstudio.com/) is a great place to get inspired to build a truly publication-ready table of information.

9. **Data for Good**: The American Statistical Association has a nice post (2020-09-01) on "[Getting Started in Data for Good](https://magazine.amstat.org/blog/2020/09/01/getting-started-in-data-for-good/)" by David Corliss, describing the growing Data for Good movement and providing some ideas for how people can contribute.

10. **HIP-Cuyahoga**: The [Health Improvement Partnership-Cuyahoga (HIP-Cuyahoga)](https://hipcuyahoga.org/) is a diverse and committed group of people who care about health. HIP-Cuyahoga is building opportunities for everyone in Cuyahoga County to be healthy because we believe everyone should have a fair chance to reach his or her fullest health potential. Their key priorities are eliminating structural racism, healthy eating and active living, chronic disease management and linking clinical and public health. If these are areas of interest for you, I encourage you to join their mailing list, and participate in the programs and other efforts they are making.
    - One closely related such effort is the **[Community Tobacco Survey 2020](https://www.surveymonkey.com/r/2020communitytobaccosurvey)**. The Community Awareness and Prevention Association has received continued funding from the Ohio Department of Health to decrease the initiation and use of tobacco by youth and adults, decrease people's exposure to secondhand smoke, and help current tobacco users embrace cessation. If you are interested in helping to develop strategies to improve the overall health and wellness of youth and adults, please feel encouraged to take a brief [Community Tobacco Survey](https://www.surveymonkey.com/r/2020communitytobaccosurvey). 

11. I've updated the **COVID-19** repository with [links to some more articles and an upcoming (free) meeting](https://github.com/THOMASELOVE/covid19) if you're interested.

## The Projects

- A draft of [Project A instructions](https://github.com/THOMASELOVE/431-2020/blob/master/projects/projectA/projectA.md) is now available, but an expanded version will be available later tonight. We'll spend a little time today hitting the highlights.

- I've also added some [information regarding what will make an acceptable Project B data set](https://github.com/THOMASELOVE/431-2020/blob/master/projects/projectB/projectB.md) in response to popular demand, but I don't plan to say any more before Project A is finished.

## What Should I Be Working On? ([calendar](https://thomaselove.github.io/431/calendar.html) has all deadlines.)

1. There is a [Minute Paper after Class 07](http://bit.ly/431-2020-minute-07). Please complete it by noon Wednesday 2020-09-16.
2. Tomorrow (wait for the complete version) or Thursday would be an excellent time to read the Project A Instructions and see what is ahead of you. The "proposal" deadline is 2020-10-02 and the project is due 2020-10-20.
3. [Lab 03](https://github.com/THOMASELOVE/431-2020/blob/master/labs/lab03/lab03.md) is the next deliverable. You should be able to complete it by the end of today's class.
4. Readings: By the end of this week, Spiegelhalter through Chapter 4, and Chapter 7, and Leek through section 5, and sections 9-12.

## One Last Thing

A video recording (nearly 15 minute .mp4) of Dr Love demonstrating the real-time use of R Studio to do (part of) Lab 02 is [now available on our Shared Google Drive](http://bit.ly/431-2020-Love-does-Lab02). This may be especially helpful to those of you having trouble saving your .Rmd and .HTML files or working with R Projects.

![](https://github.com/THOMASELOVE/431-2020/blob/master/classes/class07/images/rmarkdown_wizards.png)

Today's cartoons come from https://github.com/allisonhorst/stats-illustrations.
