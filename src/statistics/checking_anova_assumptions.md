# How to check ANOVA assumptions

First things first. A one-way ANOVA is a statistical test used to determine
whether or not there is a significant difference between the means of 3 or more
independent groups. Typically, a one-way ANOVA is used when we have three
or more categorical, independent groups, but it can be used for just two groups
(but an independent-samples t-test is more commonly used for two groups).
Notice that when the number of groups is two, it is expected no difference
between the results of t-test and ANOVA.

For the two groups, the Welch test (also known as t-test for not equal variances
case) might be preferable because it keeps us away from many problems
related with heteroscedascity scenarios. When having unequal variances in our
two groups, ANOVA is not the method of choice, while the t-test will still work
(but now with unequal variances).

If the assumptions aren’t met, then the results of our one-way ANOVA could be
unreliable.

***
### Assumptions:

1. **Normality** - each sample was drawn from a normally distributed population.

```
-> Check the assumption visually using histograms or Q-Q plots
or
-> Check the assumption using formal statistical tests like Shapiro-Wilk,
Kolmogorov-Smironov, Jarque-Barre, or D’Agostino-Pearson


As long as each group has a large sample size, a one-way ANOVA is considered fairly robust against violations of the normality assumption.


If the assumption is severely violated, we have two choices:
    - Transform the values of our data so that the distributions are more normally distributed;
    - Perform an equivalent non-parametric test such as Kruskal-Wallis Test that doesn’t require the assumption of normality.
```

2. **Equal variances** - the variances of the populations that the samples come from are equal.

```
-> Check the assumption visually using boxplots (the variance in each group can be seen by the length of each boxplot)
or
-> Check the assumption using a formal statistical tests like Bartlett’s Test


As long as each group has the same sample size, a one-way ANOVA is considered fairly robust against violations of the equal variances assumption.


If the assumption is severely violated, we have two choices:
    - Run a Kruskal-Wallis Test (non-parametric version of the one-way ANOVA)
```

3. **Independence** - the observations in each group are independent of each other and the observations within groups were obtained by a random sample.

```
There are no alternatives when this assumption is violated. 
The best thing to do is to set up the experiment again in a way that uses a randomized design. 
```

***

**Main source:**

- https://www.statology.org/anova-assumptions/
