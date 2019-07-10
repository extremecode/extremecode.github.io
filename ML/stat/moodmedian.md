# Mood Median
Mood’s Median Test (for two samples)
The Mood’s Median Test, essentially a two sample version of the Sign Test, is used to determine whether the median of two independent samples are equal. To perform this test, you need to execute the following steps:

* Calculate the total median m of the combination of the two samples.
* Create a 2 × 2 contingency table whose first row consists of the number of elements in each sample that are greater than m and whose second row consists of the number of elements in each sample that are less than or equal to m
* Perform a chi-square test of independence
* If p-value < α then the medians of the populations from which the two samples are derived are unequal; otherwise they are equal
