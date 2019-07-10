# Bartlett
There are actually two tests called Bartlett’s. The first part of this article is for Bartlett’s test for homogeneity of variances. If you’re looking for Bartlett’s test for sphericity (testing that the correlation matrix has an identity matrix), skip to the bottom section

## Bartlett’s test for homogeneity of variances
Bartlett’s test for homogeneity of variances is used to test that variances are equal for all samples. It checks that the assumption of equal variances is true before running certain statistical tests like the One-Way ANOVA. It’s used when you’re fairly certain your data comes from a normal distribution. A similar test, called Levene’s test, is a better choice for non normal distributions.

The null hypothesis for the test is that the variances are equal for all samples. In statistics terms, that’s:
H0: σ12 = σ22 = … = σk2.
The alternate hypothesis (the one you’re testing), is that the variances are not equal for one pair or more:
H0: σ12 ≠ σ22 ≠… ≠ σk2.

The test statistic is rather ugly:
bartlett's test



## Bartlett’s Test for Sphericity

Bartlett’s test for Sphericity compares your correlation matrix (a matrix of [Pearson correlations](https://www.statisticshowto.datasciencecentral.com/probability-and-statistics/correlation-coefficient-formula/)) to the identity matrix. In other words, it checks if there is a redundancy between variables that can be summarized with some factors.
