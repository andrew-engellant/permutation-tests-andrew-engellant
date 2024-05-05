
# Satisfaction Permutation Tests

In class we discussed analysis of an employee satisfaction survey. Since the survey was a census, 
normal statistical approaches (like a t-test) do not apply. This assignment asks you to 
extend the work with a few more tests. The R-Markdown file has code blocks for you to edit and 
questions for you to answer. 

When you submit your work, make sure to "knit" your RMD to an `.html` file and include that file in the repo you submit. (You can also knit to PDF and Word formats, which are great, but the HTML files are a bit easier for me to evaluate.) 

## Feedback 

On the first "satisfied" test, it's a bit faster and easier to read if you use the new column I created for you. But you get the correct answer.

In the location one, I asked for "satisfaction" (average score) and not "satisfied" (a score of 5, 6, or 7). But the conclusions don't change, so let's call it good. Just be careful in the future. 

Your interpretation of the median result is exactly right. You put a code comment in to me, but just write that in markdown and set it up somehow, like
```
#### Question

Does a permutation sample still need to be run if the test statistic is zero (matches the null hypothesis)? Is there an instance where the normal distribution of the permutation results is not centered around zero (when the null is that there is no difference)?
```

You need to create the permutations to know that the difference is always zero, so I'm not sure how you might avoid running "a permutation sample" (although I'm not precisely clear on what you mean by that term. In your second question, when you say "normal distribution of the permutation", you probably mean "empirical of the density of the permutation statistics" or something similar. Some of them look normal (most in this homework), some don't (the non-binary one, for instance). 

All that aside, your question is interesting. Most of the time when we're making a null hypothesis of no difference in some statistic we do end up with the sampling distribution being centered on zero. There are lots of times _without_ that assumption where we wouldn't have zero centering. For instance, if the statistic we were interested in, for instance, the count of aces in a 13-card gin rummy hand, the value would be centered around 1. For a more sophisticated example, the chi-squared statistic that we calculate in week 3 is bounded below by zero. But I think if we're assuming no difference in some statistic, then that implies that we're calculating the stat for two groups and differencing them. In that situation, I think we'll always have a distribution centered on zero, but I'll see if I can come up with a counter example. 
