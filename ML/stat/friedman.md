# Friedman Test
Friedman’s test is a non-parametric test for finding differences in treatments across multiple attempts. Nonparametric means the test doesn’t assume your data comes from a particular distribution (like the normal distribution). Basically, it’s used in place of the ANOVA test when you don’t know the distribution of your data.

Friedman’s test is an extension of the sign test, used when there are multiple treatments. In fact, if there are only two treatments the two tests are identical.

## Assumptions
* Data should be ordinal (e.g. the Likert scale) or continuous,
* Data comes from a single group, measured on at least three different occasions,
* The sample was created with a random sampling method,
* Blocks are mutually independent (i.e. all of the pairs are independent — one doesn’t affect the other),
* Observations are ranked within blocks with no ties.
