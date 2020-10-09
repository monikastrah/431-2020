# Project A Proposal Status

As of `2020-10-08 8:20 PM` | Solo Projects | Pair Projects | Projects | Students
------ | -----: | -------: | ------: | -------:
**Submitted Work** | **40** | **15** | **55** | **70**
Approved by Dr. Love | 37 | 14 | 51 | 65
Under Revision | 2 | 1 | 3 | 4
On Hold | 1 | 0 | 1 | 1

## Notes from Dr. Love

- If your project has not yet been approved, the **grade** that is posted on Canvas is **NOT** your proposal grade. It is the count of how many (out of the 13 elements) on [the Checklist](https://thomaselove.github.io/431-2020-projectA/checklist.html) you have successfully completed. You need to meet all 13 standards to be approved.
    - Your grade on the proposal will be determined when you have an accepted proposal. Those grades are 25 for people who are accepted at the first deadline, and decreases by 10% for each subsequent deadline, so we anticipate that virtually all students will need to revise will wind up with a grade on the proposal of either 20 or 22.5 points out of a possible 25.
    - Note that Canvas has now been adjusted to mark as LATE only those revisions arriving after Noon Friday.
- If you need an extension on the revision for an emergency, contact Dr. Love directly via email, please.
- In producing the next iteration of your project, please follow the comments we've provided on Canvas. 
- If you have questions about those comments or how to improve your work, please ask them in TA office hours, or via the channels we've made available for the Quiz, or (after the Quiz deadline has passed) you can ask them on Piazza normally.

For most of the projects, a TA did the initial pass through the work and wrote some comments, then Dr. Love amplified those comments. In writing our comments on Canvas, we focused almost solely on things that needed to be fixed. If you're wondering whether we liked your work the answer is Yes, we did, but we didn't (usually) bother to tell you about that in an effort to get the proposals back in your hands as quickly as possible. Sorry for the lack of encouragement. There were good things in every proposal.

- On too many occasions, in summarizing comments, I (Dr. Love) was more strident than I should have been, and/or more harsh in my criticism, and for that I apologize. I tend to lose patience with long, repetitive tasks, and I did too much of this work late at night without a break. That was a mistake by me (the TAs were much smarter about this than I was) and again, I apologize. 

## A few things came up repeatedly.

1. Each of the five variables you select can fill one and only one role (outcome, quantitative predictor 1, quantitative predictor 2, binary predictor, multi-categorical predictor.) 
2. When ingesting the data, use message = FALSE in your code chunk setup to suppress the column specifications details. In general, viewers of your HTML shouldn't see messages that are generated automatically but contain no useful content in your specific situation. If you are generating warnings (as opposed to messages) in R, you should fix the problem, rather than suppressing the warnings.
3. In creating categories, create categories people can remember. For example, if the median is 49.86, use 50 as your cutoff, so that people can understand this. Don't make things any more complicated for your eventual explanations of your analyses than they have to be.
4. It is your job to produce a document (and later a video as well) for an audience. That audience is interested in seeing your code that does things that matter, but is not interested in seeing your play-by-play with R. Edit your code to focus on the things worth writing about, or the things that are critical for your data development or analyses. This certainly includes all of the things I described in the checklist and the instructions, but doesn't include repeated checks on your data.
5. In HTML, you have all the vertical space in the world. Your horizontal space, though, is quite limited, so R Markdown creates (in HTML) lots of little scrolling windows for code. We want to avoid those as much as possible. So ... hit ENTER after every %>% and every + in a ggplot. When you have a long list of variables, like in the selection of your initial variables, hit ENTER after a comma somewhere in the middle so that you avoid the scourge of the scrolling window in the HTML result.
6. Spell check in RStudio and also look closely at the HTML that you've created at the end to make sure that the formatting works, and that things look nice. The HTML is the main document that Dr. Love and the TAs will review in studying your work.

