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



