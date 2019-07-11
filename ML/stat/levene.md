# Levene Test
Levene’s test is used to check that variances are equal for all samples when your data comes from a non normal distribution. You can use Levene’s test to check the assumption of equal variances before running a test like One-Way ANOVA.

If you’re fairly certain your data comes from a normal or nearly normal distribution, use Bartlett’s Test instead.

The null hypothesis for Levene’s is that the variances are equal across all samples. In more formal terms, that’s written as:
H0: σ12 = σ22 = … = σk2.
The alternate hypothesis (the one you’re testing), is that the variances are not equal for at least one pair:
H0: σ12 ≠ σ22 ≠… ≠ σk2.

The test statistic is a little ugly:
levene test

Zi,j can take on three meanings, depending on if you use the mean, median, or trimmed mean of any subgroup. The three choices actually determine the robustness and power of the test.

Robustness, is a measure of how well the test does not falsely report unequal variances (when the variances are actually equal).
Power is a measure of how well the test correctly reports unequal variances.
According to Brown and Forsythe:

Trimmed means work best with heavy-tailed distributions like the Cauchy distribution.
For skewed distributions, or if you aren’t sure about the underlying shape of the distribution, the median may be your best choice.
For symmetric and moderately tailed distributions, use the mean.
