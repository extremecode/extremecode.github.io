# Ftest
## Defination
An “F Test” is a catch-all term for any test that uses the F-distribution. In most cases, when people talk about the F-Test, what they are actually talking about is The F-Test to Compare Two Variances. However, the f-statistic is used in a variety of tests including regression analysis, the Chow test and the Scheffe Test (a post-hoc ANOVA test).


## Assumptions
Several assumptions are made for the test. Your population must be approximately normally distributed (i.e. fit the shape of a bell curve) in order to use the test. Plus, the samples must be independent events. In addition, you’ll want to bear in mind a few important points:

The larger variance should always go in the numerator (the top number) to force the test into a right-tailed test. Right-tailed tests are easier to calculate.
For two-tailed tests, divide alpha by 2 before finding the right critical value.
If you are given standard deviations, they must be squared to get the variances.
If your degrees of freedom aren’t listed in the F Table, use the larger critical value. This helps to avoid the possibility of Type I errors.

## F test to compare variance between 
<pre>
Step 1: If you are given standard deviations, go to Step 2. If you are given variances to compare, go to Step 3.

Step 2: Square both standard deviations to get the variances. For example, if σ1 = 9.6 and σ2 = 10.9, then the variances (s1 and s2) would be 9.62 = 92.16 and 10.92 = 118.81.

Step 3: Take the largest variance, and divide it by the smallest variance to get the f-value. For example, if your two variances were s1 = 2.5 and s2 = 9.4, divide 9.4 / 2.5 = 3.76.
Why? Placing the largest variance on top will force the F-test into a right tailed test, which is much easier to calculate than a left-tailed test.

Step 4: Find your degrees of freedom. Degrees of freedom is your sample size minus 1. As you have two samples (variance 1 and variance 2), you’ll have two degrees of freedom: one for the numerator and one for the denominator.

Step 5: Look at the f-value you calculated in Step 3 in the f-table. Note that there are several tables, so you’ll need to locate the right table for your alpha level. Unsure how to read an f-table? Read What is an f-table?.

Step 6: Compare your calculated value (Step 3) with the table f-value in Step 5. If the f-table value is smaller than the calculated value, you can reject the null hypothesis.

</pre>


## two tailed F test
you just want to know if the variances are not equal to each other. In notation:
Ha = σ21 ≠ σ2 2

Sample problem: Conduct a two tailed F Test on the following samples:
Sample 1: Variance = 109.63, sample size = 41.
Sample 2: Variance = 65.99, sample size = 21.

Step 1: Write your hypothesis statements:
Ho: No difference in variances.
Ha: Difference in variances.

Step 2: Calculate your F critical value. Put the highest variance as the numerator and the lowest variance as the denominator:
F Statistic = variance 1/ variance 2 = 109.63 / 65.99 = 1.66

Step 3: Calculate the degrees of freedom:
The degrees of freedom in the table will be the sample size -1, so:
Sample 1 has 40 df (the numerator).
Sample 2 has 20 df (the denominator).

Step 4: Choose an alpha level. No alpha was stated in the question, so use 0.05 (the standard “go to” in statistics). This needs to be halved for the two-tailed test, so use 0.025.

Step 5: Find the critical F Value using the F Table. There are several tables, so make sure you look in the alpha = .025 table. Critical F (40,20) at alpha (0.025) = 2.287.
f-test

Step 6: Compare your calculated value (Step 2) to your table value (Step 5). If your calculated value is higher than the table value, you can reject the null hypothesis:
F calculated value: 1.66
F value from table: 2.287.
1.66 < 2 .287.
So we cannot reject the null hypothesis.
