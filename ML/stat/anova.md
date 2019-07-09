# Anova
## types
* The ANOVA Test
* One Way ANOVA
* Two Way ANOVA
* What is MANOVA?
* What is Factorial ANOVA?
* How to run an ANOVA
* ANOVA vs. T Test
* Repeated Measures ANOVA
* Sphericity

## use cases
An ANOVA test is a way to find out if survey or experiment results are significant. In other words, they help you to figure out if you need to reject the null hypothesis or accept the alternate hypothesis. Basically, you’re testing groups to see if there’s a difference between them. Examples of when you might want to test different groups:

* A group of psychiatric patients are trying three different therapies: counseling, medication and biofeedback. You want to see if one therapy is better than the others.
* A manufacturer has two different processes to make light bulbs. They want to know if one process is better than the other.
Students from different colleges take the same exam. You want to see if one college outperforms the other

## What Does “One-Way” or “Two-Way Mean?
One-way or two-way refers to the number of independent variables (IVs) in your Analysis of Variance test. One-way has one independent variable (with 2 levels) and two-way has two independent variables (can have multiple levels). For example, a one-way Analysis of Variance could have one IV (brand of cereal) and a two-way Analysis of Variance has two IVs (brand of cereal, calories).

## What are “Groups” or “Levels”?
Groups or levels are different groups in the same independent variable. In the above example, your levels for “brand of cereal” might be Lucky Charms, Raisin Bran, Cornflakes — a total of three levels. Your levels for “Calories” might be: sweetened, unsweetened — a total of two levels.

Let’s say you are studying if Alcoholics Anonymous and individual counseling combined is the most effective treatment for lowering alcohol consumption. You might split the study participants into three groups or levels: medication only, medication and counseling, and counseling only. Your dependent variable would be the number of alcoholic beverages consumed per day.

### What Does “Replication” Mean?
It’s whether you are replicating your test(s) with multiple groups. With a two way ANOVA with replication , you have two groups and individuals within that group are doing more than one thing (i.e. two groups of students from two colleges taking two tests). If you only have one group taking two tests, you would use without replication.

## Types of Tests.
There are two main types: one-way and two-way. Two-way tests can be with or without replication.

* One-way ANOVA between groups: used when you want to test two groups to see if there’s a difference between them.
* Two way ANOVA without replication: used when you have one group and you’re double-testing that same group. For example, you’re testing one set of individuals before and after they take a medication to see if it works or not.
* Two way ANOVA with replication: Two groups, and the members of those groups are doing more than one thing. For example, two groups of patients from different hospitals trying two different therapies.

### One Way ANOVA
A one way ANOVA is used to compare two means from two independent (unrelated) groups using the F-distribution. The null hypothesis for the test is that the two means are equal. Therefore, a significant result means that the two means are unequal.

#### When to use a one way ANOVA
##### Situation 1: 
You have a group of individuals randomly split into smaller groups and completing different tasks. For example, you might be studying the effects of tea on weight loss and form three groups: green tea, black tea, and no tea.
##### Situation 2: 
Similar to situation 1, but in this case the individuals are split into groups based on an attribute they possess. For example, you might be studying leg strength of people according to weight. You could split participants into weight categories (obese, overweight and normal) and measure their leg strength on a weight machine.

#### Limitations of the One Way ANOVA
A one way ANOVA will tell you that at least two groups were different from each other. But it won’t tell you what groups were different. If your test returns a significant f-statistic, you may need to run an ad hoc test (like the Least Significant Difference test) to tell you exactly which groups had a difference in means.

### Two Way ANOVA
A Two Way ANOVA is an extension of the One Way ANOVA. With a One Way, you have one independent variable affecting a dependent variable. With a Two Way ANOVA, there are two independents. Use a two way ANOVA when you have one measurement variable (i.e. a quantitative variable) and two nominal variables. In other words, if your experiment has a quantitative outcome and you have two categorical explanatory variables, a two way ANOVA is appropriate.

#### example
you might want to find out if there is an interaction between income and gender for anxiety level at job interviews. The anxiety level is the outcome, or the variable that can be measured. Gender and Income are the two categorical variables. These categorical variables are also the independent variables, which are called factors in a Two Way ANOVA.

The factors can be split into levels. In the above example, income level could be split into three levels: low, middle and high income. Gender could be split into three levels: male, female, and transgender. Treatment groups are all possible combinations of the factors. In this example there would be 3 x 3 = 9 treatment groups.

### Main Effect and Interaction Effect
The results from a Two Way ANOVA will calculate a main effect and an interaction effect. The main effect is similar to a One Way ANOVA: each factor’s effect is considered separately. With the interaction effect, all factors are considered at the same time. Interaction effects between factors are easier to test if there is more than one observation in each cell. For the above example, multiple stress scores could be entered into cells. If you do enter multiple observations into cells, the number in each cell must be equal.

<pre>
Two null hypotheses are tested if you are placing one observation in each cell. For this example, those hypotheses would be:
H01: All the income groups have equal mean stress.
H02: All the gender groups have equal mean stress.


 
For multiple observations in cells, you would also be testing a third hypothesis:
H03: The factors are independent or the interaction effect does not exist.

An F-statistic is computed for each hypothesis you are testing.

Assumptions for Two Way ANOVA
The population must be close to a normal distribution.
Samples must be independent.
Population variances must be equal.
Groups must have equal sample sizes.
</pre>
