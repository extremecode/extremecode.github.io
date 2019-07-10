# Wilcoxon

The Wilcoxon signed rank test (also called the Wilcoxon signed rank sum test) is a non-parametric test. When the word “non-parametric” is used in stats, it doesn’t quite mean that you know nothing about the population. It usually means that you know the population data does not have a normal distribution. The Wilcoxon signed rank test should be used if the differences between pairs of data are non-normally distributed.

Two slightly different versions of the test exist:

* The Wilcoxon signed rank test compares your sample median against a hypothetical median.
* The Wilcoxon matched-pairs signed rank test computes the difference between each set of matched pairs, then follows the same procedure as the signed rank test to compare the sample against some median.
* The term “Wilcoxon” is often used for either test. This usually isn’t confusing, as it should be obvious if the data is matched, or not matched.

The null hypothesis for this test is that the medians of two samples are equal. It is generally used:

As a non-parametric alternative to the one-sample t test or paired t test.
For ordered (ranked) categorical variables without a numerical scale.


## Sample question: 
Is there a difference between the median values for the following sets of treatment data for the twelve groups?
wilcoxon signed rank test 1


Step 1: Subtract treatment 2 from treatment 1 to get the differences:
wilcoxon signed rank test 2


Note: If you only have one sample, calculate the differences between each variable and zero (the hypothesized median) instead of the difference between pairs.

Step 2: Place the differences in order (column 2 in the picture below), and then rank them. Ignore the sign when placing in rank order.
wilcoxon signed rank test 3


Step 3: Make a third column and note the sign of the difference (the one you ignored in Step 2!).
wilcoxon signed rank test 4


The next two steps calculate the Wilcoxon signed rank sums:

Step 4: Calculate the sum of the ranks of the negative differences (the ones with the negative sign in the Step 3 chart). You’re adding up the ranks here, not the actual differences:
W– = 1 + 2 + 4 = 7

Step 5: Calculate the sum of the ranks of the positive differences (the ones with the positive sign in the Step 3 chart).
W+ = 3 + 5.5 + 5.5 + 7 + 8 + 9 + 10 + 11 + 12 = 71

Using the Normal Approximation with Wilcoxin Signed Ranks
What can you do with the above information? If the number of observations/pairs n(n+1)/2 is greater than 20, you can use a normal approximation. This set of data meets this requirement (12(12 + 1) / 2 = 78. There are several modifications/considerations for the z-score formula:

Use the smaller of W+ or W– for the test statistic.
Use the following formula for the mean, μ: n(n+1)/4.
Use the following formula for σ: √((n(n+1)(2n+1))/24)
If you have tied ranks, you must reduce σ by t3-t/48 for each of t tied ranks. There are two tied ranks (5.5 + 5.5), so reduce σ by 8-2/48 = 0.125.
This gives a z-score of:
wilcoxin z v2


Looking up this score in the z-table*, we get an area of 0.9880, equal to a two-tailed p-value of 0.012. This is a tiny p-value, a strong indication that the medians are significantly different.

*The z-table here is to the right of the mean, so I had to double the actual result I found (.4940).

Statistics Definitions > Wilcoxon signed rank test-
