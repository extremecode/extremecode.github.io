# Hypothesis Testing

As we know, Inferential statistics enables you to make “inferences” about the Population mean from the sample data when you have no clue about the Population.

However, sometimes, you have some assumption/estimate about the Population mean to start with, and you want to confirm the validity of these assumptions/estimates using sample data.



 
* Applications of hypothesis testing,
* Null and alternate hypotheses, and
* Two methods to find the validity of a claim:
* Critical value method
* P-value method

ex - 
* Let's say an e-commerce company wants to decide between two variants of a button: "Shop now" and "Buy now". Although it may seem insignificant, practically speaking, it has been observed that improving the UI/UX design can have enormous benefits for the company. In such cases, we perform A/B testing, which is a subset of hypothesis testing.

* Another important area where hypothesis testing is extensively used is checking the validity of machine learning models. As the course progresses, you will learn how to build and validate various machine learning models. This is where hypothesis testing will come handy.

 

* Any product that you buy comes with a warranty. Electronic products generally come with a one-year warranty, whereas car manufacturers give a 3–10-year warranty depending on the components of the car. These claims are majorly driven by hypothesis testing.

 
* Fundamentals of hypothesis testing
* Hypothesis testing using a single sample 
* Hypothesis testing using two samples

<image 1 placeholder>
![image](https://user-images.githubusercontent.com/20191454/157242874-2b58fa7b-dcab-4627-aef4-3a08a283b6a6.png)




In this video, you learned how to frame the two hypothesis statements, which are defined below:

Null hypothesis (H0): This statement is the default assumption/belief (the status quo).
Alternate hypothesis (Ha): This statement challenges the status quo, i.e., it states the opposite of the null hypothesis.

Listed below are some important properties of null and alternate hypotheses:

The null and alternate hypotheses are always mutually exclusive events.
Mutually Exclusive Events
Mutually Exclusive Events
The null and alternate hypotheses must be collectively exhaustive events.

<image 2 placeholder>
![image](https://user-images.githubusercontent.com/20191454/157242894-3ab9b058-4e1b-4190-9798-bbe1dcc8aaf2.png)



This means that at least one of these events must be true at any given time. The two events cover the complete sample space. Since these are perfect opposites of each other, we can also call them complementary events.

 Complementary Events.
 
 <image 3 placeholder>
![image](https://user-images.githubusercontent.com/20191454/157242931-68bc5409-2541-4390-a6e2-868c6ce692c3.png)


Complementary Events.
As you can see, both the events are perfect opposites and cover the whole sample space.

 

Following are some important points to keep in mind about framing null and alternate hypotheses:

The null and alternate hypotheses are perfect opposites of each other. Hence, they should cover the entire range of possibilities.
The null hypothesis always has the following signs: ‘=’ OR ‘≤’ OR ‘≥’.
The alternate hypothesis always has the following signs: ‘≠’ OR ‘>’ OR ‘<’.
So, whenever a new claim is made, the null hypothesis states that the claim is not true, and the alternate hypothesis states that the claim is true. Hence, for the claim to be declared true, evidence will have to be gathered to prove its statistical validity. In other words, the strategy is to frame the alternate hypothesis as the hypothesis that you are trying to prove.




So, we always begin with the assumption that the null hypothesis is true. Then:

If we have sufficient evidence to prove that the null hypothesis is false, we ‘reject’ it. In this case, the alternate hypothesis is proved to be true.
If we do not have sufficient evidence to prove that the null hypothesis is false, we ‘fail to reject’ it. In this case, the assumption that the null hypothesis is true remains.


From the video, you understood that we never prove the null hypothesis; we can only say that we ‘fail to reject’ the null hypothesis based on the evidence that we have gathered.


If the evidence supports the claim, we accept the alternate hypothesis, i.e., we reject the null hypothesis. If the evidence does not support the claim, we fail to reject the null hypothesis.


One of the examples of hypothesis testing could be proving a person guilty of committing a crime.


<image 4 placeholder>
![image](https://user-images.githubusercontent.com/20191454/157242962-fed13bae-a14a-4efb-86ec-9824792e9870.png)



. You can follow these steps to conduct a hypothesis test using the critical value method:

 

Step 1: Frame the appropriate null and alternative hypotheses.

 

In the OnePlus example, the hypotheses are as follows:
H
o
:
μ
=
30
 
m
i
n
u
t
e
s

H
a
:
μ
≠
30
 
m
i
n
u
t
e
s

 

Step 2: Decide the confidence level (or the significance level).

 

The significance level (α) is defined as 1 - confidence level.

 

Therefore, if the confidence level of a test is 0.95 (95%), its significance level will be 0.05 (5%). It represents the area outside the confidence interval (which is referred to as the rejection region). Higher the significance level, higher are the chances of rejecting the null hypothesis. 

 

In the OnePlus example, we have taken the significance level 
α
=
0.05

 

Step 3: Determine the critical z-score(s) (and the rejection region).

 

The critical z-score(s) defines the boundary of the region beyond which if the sample z-score lies, we reject the null hypothesis. This region is referred to as the rejection region. The region of the graph that represents values closer to the hypothesized mean than the critical z-score(s) is called the acceptance region. 

 

In simple words, if the sample z-score lies further away from the hypothesized mean than the critical z-score(s), we reject the null hypothesis.
 
In the OnePlus example, as the confidence level that is chosen is 95% and we are looking at both sides of the hypothesized mean, the critical z-scores are ±1.96. This means that the rejection region is to the left of -1.96 and to the right of +1.96.


Step 4: Compute the sample z-score (or ‘z-statistic’).

 

The sample z-score tells us how many standard deviations away from the mean the sample mean lies in the distribution of sample means. According to the Central Limit Theorem, the mean of the sample means distribution is assumed to be equal to the population mean, which,

in this case, is the hypothesized mean.



![image](https://user-images.githubusercontent.com/20191454/157242633-b77b6070-d3e5-4710-a2bb-65339bf1503f.png)

It is important to note that in the context of z-tests, the term sample z-score is often used interchangeably with z-statistic. The term test statistic is also commonly used to refer to the standardized sample mean.

 

In the OnePlus example, we took a sample of 100 smartphones and measured the time taken to charge each of them to 100%. This data became our sample. We then calculated the mean (30.37) and standard deviation (2.477) of the sample. Using these values, the sample z-score comes out to be 1.4937.
 

Step 5: Reach a decision and interpret the result.

 

Finally, we compare the sample z-score with the critical z-scores of the test.

If the sample z-score lies in the non-rejection (or acceptance) region, we fail to reject the null hypothesis and conclude that the assumption that the null hypothesis is true remains.
If the sample z-score lies in the rejection region, we reject the null hypothesis and conclude that the null hypothesis is false and the alternative hypothesis is true.
In the OnePlus example, as the sample z-score lies in the acceptance region, we fail to reject the null hypothesis. Therefore, we do not have sufficient evidence to conclude that the time taken to charge the phone is not 30 minutes.



One-tailed tests can be either left-tailed or right-tailed, depending on which side of the curve the rejection region lies on. The formulation of the null and alternate hypotheses determines the type of the test and the position of the rejection region(s) in the distribution of sample means.

 

You can tell the type of the test and the position of the rejection region(s) on the basis of the ‘sign’ used in the alternate hypothesis.

 

       '<’ in H⍺    →   Left-tailed test     →     Rejection region on the left side of the distribution

 

       ‘>’ in H⍺    →   Right-tailed test  →     Rejection region on the right side of the distribution

 

       ‘≠’ in H⍺    →   Two-tailed test     →     Rejection region on both sides of the distribution

 

Considering our OnePlus example, with a significance level =0.05, let’s look at the table given below to understand all three approaches.

![image](https://user-images.githubusercontent.com/20191454/157244337-12489949-ebb4-4cef-b59d-57aef2762a96.png)


In this video, you learned that the p-value is the shaded region, i.e., the area that lies farther away from the hypothesized mean than the calculated sample z-score. 

 

So, intuitively, you can also understand the p-value as the probability of the null hypothesis being true. Thus, a higher p-value indicates greater evidence in favor of the null hypothesis. Similarly, a lower p-value indicates greater evidence against the null hypothesis (and in favor of the alternate hypothesis).

 

In this video, you also learned how to use the “p-value calculator” to compute the p-value for both one-tailed and two-tailed tests.

 

The simple rule that you can follow while using the p-value method to test a hypothesis is as follows:

 

If p-value 
≤
 ⍺ → Reject the null hypothesis.
If p-value 
>
 ⍺ → Fail to reject the null hypothesis.

 

Considering the same example of OnePlus, with ⍺ = 0.05, let’s look at the table given below to understand all three approaches.



![image](https://user-images.githubusercontent.com/20191454/157245747-2c252800-101e-4804-b07c-50a89a0c8377.png)

Stat Z score calculator
http://courses.atlas.illinois.edu/spring2016/STAT/STAT200/pnormal.html


summary:
A hypothesis is a claim or an assumption that you make about one or more population parameters.

 

You learned about the types of hypotheses:

Null hypothesis (H0): Makes an assumption about the status quo and always contains the symbols ‘=’, ‘≤’ or ‘≥’
Alternate hypothesis (Ha): Challenges and complements the null hypothesis and always contains the symbols ‘≠’, ‘<’ or ‘>’
Testing Process
You also learned about the process followed for testing a hypothesis, which is described below:

State relevant null and alternate hypotheses.
Decide on the significance level.
Find the relevant critical value that divides the probability distribution into ‘non-rejection’ and ‘rejection’ regions.
Compute the test statistic and compare it with the relevant critical value.
Decide to either fail to reject the null hypothesis or reject it in the favor of the alternate hypothesis.
 

p-Value Method
 

p-Value signifies the probability of the null hypothesis being true. A higher p-value indicates a stronger evidence in favor of the null hypothesis and a lower p-value indicates a stronger evidence against the null hypothesis.

 

As a rule, we know:

If p-value 
≤
α
 - We reject the null hypothesis.

If p-value
>
α
 - We fail to reject the null hypothesis.

 

Types of Tests
Finally, you learnt about the three types of tests that are used in making a decision about the hypothesis. These are described below:

Two-tailed test: The critical region lies on both sides of the distribution. The alternate hypothesis contains the ≠ sign.
Lower-tailed test: The critical region lies on the left side of the distribution. The alternate hypothesis contains the < sign.
Upper-tailed test: The critical region lies on the right side of the distribution. The alternate hypothesis contains the > sign.
You can also go through the summary document provided below:

https://cdn.upgrad.com/uploads/production/00cbc683-e8dc-4ff1-978c-844424e0c14a/Session%2BSummary.pdf



when to use
![image](https://user-images.githubusercontent.com/20191454/157250128-f5c23e40-89f8-4f31-b418-2fcba7c2a5cc.png)


As you saw in the video, when you know the population standard deviation, you approach the problem in the following way:

Formulate the null and alternative hypotheses (
H
0
 and 
H
a
).
Decide the level of significance (
α
).
Compute the test z-statistic and p-value. (In this case, you could find the z-statistic because you knew the value of population standard deviation (
σ
)).
          The z-statistic can be calculated using the following formula:

Z
=
¯
X
−
μ
σ
√
n

 

          Where,

          
¯
X
 is the sample mean,
           
μ
  is the hypothesized population mean,
           
σ
 is the population standard deviation, and
           n is the sample size.

 

Note: Before you find the p-value, it is important to identify whether it is a right-tailed, left-tailed or two-tailed test. In the YouTube example, since your alternative hypothesis 
H
a
 had a “>” sign, it was a case of a right-tailed test. Now that you have established the type of test, you can calculate the p-value.
 

Once you have the p-value, you can now move on to the last step.

 

             4. Compare the p-value with the level of significance (
α
).

 

If:

p-value 
≤
  : We reject the null hypothesis
p-value 
>
  : We fail to reject the null hypothesis
 

So, in this case, we had sufficient evidence to be able to reject the null hypothesis. Therefore, considering our YouTube example, our inference would be: “We have sufficient evidence to prove that it is really unlikely that if we use the new algorithm, the average time spent by users would be less than or equal to 700 seconds.”



![image](https://user-images.githubusercontent.com/20191454/157254283-5d0cf665-6fe6-4d20-b3f2-7bb6cdc9ac30.png)




Second, you understood how we tweaked the YouTube algorithm problem and brought in further uncertainty into our problem by making:

Sample size n = 21 (as compared to n = 40 in the previous scenario)
Population standard deviation unknown (as opposed to the previous scenario)
 

Third, you learned that the overall approach to solving the problem remains the same, except that in the third step, we calculate t-statistic instead of z-statistic. 

 

We calculate the t-statistic using the formula:

t
=
¯
X
−
μ
s
√
n

Where,

X is the sample mean,
μ
is the hypothesized population mean,
s is the standard deviation of the sample, and
n is the sample size.
 

And with the help of t-statistic and degree of freedom (df) = sample size(n) - 1, we calculate the p-value.

 

Finally, you saw in this example that our p-value exceeded the significance level (), and we, thus, failed to reject the null hypothesis. Therefore, our inference in this case would be as follows: “We don’t have sufficient evidence to conclude that the average time spent will be greater than 700 seconds if the new algorithm was deployed.”


t table
https://cdn.upgrad.com/uploads/production/ebc8f72d-da0a-4c81-966b-d332ac1b0fd7/t-table.pdf


![image](https://user-images.githubusercontent.com/20191454/157264975-ac78cbf0-8f71-4913-917c-ebae1b300a41.png)
