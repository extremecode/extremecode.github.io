# kruskal Wallis

The Kruskal Wallis test is the non parametric alternative to the One Way ANOVA. Non parametric means that the test doesn’t assume your data comes from a particular distribution. The H test is used when the assumptions for ANOVA aren’t met (like the assumption of normality). It is sometimes called the one-way ANOVA on ranks, as the ranks of the data values are used in the test rather than the actual data points.
The test determines whether the medians of two or more groups are different. Like most statistical tests, you calculate a test statistic and compare it to a distribution cut-off point. The test statistic used in this test is called the H statistic. The hypotheses for the test are:

H0: population medians are equal.

H1: population medians are not equal.

The Kruskal Wallis test will tell you if there is a significant difference between groups. However, it won’t tell you which groups are different. For that, you’ll need to run a Post Hoc test.

## Examples
* You want to find out how test anxiety affects actual test scores. The independent variable “test anxiety” has three levels: no anxiety, low-medium anxiety and high anxiety. The dependent variable is the exam score, rated from 0 to 100%.
* You want to find out how socioeconomic status affects attitude towards sales tax increases. Your independent variable is “socioeconomic status” with three levels: working class, middle class and wealthy. The dependent variable is measured on a 5-point Likert scale from strongly agree to strongly disagree.
