# Wilcoxon

The Wilcoxon signed rank test (also called the Wilcoxon signed rank sum test) is a non-parametric test. When the word “non-parametric” is used in stats, it doesn’t quite mean that you know nothing about the population. It usually means that you know the population data does not have a normal distribution. The Wilcoxon signed rank test should be used if the differences between pairs of data are non-normally distributed.

Two slightly different versions of the test exist:

* The Wilcoxon signed rank test compares your sample median against a hypothetical median.
* The Wilcoxon matched-pairs signed rank test computes the difference between each set of matched pairs, then follows the same procedure as the signed rank test to compare the sample against some median.
* The term “Wilcoxon” is often used for either test. This usually isn’t confusing, as it should be obvious if the data is matched, or not matched.

The null hypothesis for this test is that the medians of two samples are equal. It is generally used:

As a non-parametric alternative to the one-sample t test or paired t test.
For ordered (ranked) categorical variables without a numerical scale.
