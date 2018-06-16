# Basic
## Table of Contents 
* [IQR](#IQR)
* [Continous vs Discrete](#cvd)
* [Range](#range)
* [Finding fake Statistics](#fake)
* [](#)
* [](#)
* [](#)
### IQR <a name="IQR"></a>
*	Q3-Q1 for even set – no middle value
*	Step 1: Put the numbers in order.
1, 2, 5, 6, 7, 9, 12, 15, 18, 19, 27.
*	Step 2: Find the median.
1, 2, 5, 6, 7, 9, 12, 15, 18, 19, 27.
*	Step 3: Place parentheses around the numbers above and below the median. 
Not necessary statistically, but it makes Q1 and Q3 easier to spot.
(1, 2, 5, 6, 7), 9, (12, 15, 18, 19, 27).
*	Step 4: Find Q1 and Q3
Think of Q1 as a median in the lower half of the data and think of Q3 as a median for the upper half of data.
(1, 2, 5, 6, 7),  9, ( 12, 15, 18, 19, 27). Q1 = 5 and Q3 = 18.
*	Step 5: Subtract Q1 from Q3 to find the interquartile range.
18 – 5 = 13.
```markdown
> a<-c(1,2,5,6,7,9,12,15,18,19,27)
> IQR(a)
[1] 13
```

### Continous vs Discrete <a name="cvd"></a>
_Discrete variables are countable in a finite amount of time. For example, you can count the change in your pocket. You can count the money in your bank account. You could also count the amount of money in everyone’s bank account. It might take you a long time to count that last item, but the point is — it’s still countable._
_Continuous Variables would (literally) take forever to count. In fact, you would get to “forever” and never finish counting them. For example, take age. You can’t count “age”. Why not? Because it would literally take forever. For example, you could be:
25 years, 10 months, 2 days, 5 hours, 4 seconds, 4 milliseconds, 8 nanoseconds, 99 picosends…and so on. You couldturn age into a discrete variable and then you could count it. For example:_
*	A person’s age in years.
*	A baby’s age in months.
```markdown
```
### Range  <a name="range"></a>

<pre>
Step 1: Sort the numbers in order, from smallest to largest:
7, 10, 21, 33, 43, 45, 45, 65, 67, 87, 98, 99
Step 2: Subtract the smallest number in the set from the largest number in the set:
99 – 7 = 92
The range is 92
That’s it!
Sample question 2: What is the range of these integers?
14, -12, 7, 0, -5, -8, 17, -11, 19
Step 1: Sort the numbers in order, from smallest to largest:
-12, -11, -8, -5, 0, 7, 14, 17, 19
Step 2: Subtract the smallest number in the set from the largest number in the set:
19 – -12 = 19 + 12 = 31
The range is 31.
That’s it!
Sample question 3: What is the range of the following times?
2.7 hrs, 8.3 hrs, 3.5 hrs, 5.1 hrs, 4.9 hrs
Step 1: Sort the numbers in order, from smallest to largest:
2.7, 3.5, 4.9, 5.1, 8.3
Step 2: Subtract the smallest number in the set from the largest number in the set:
8.3 hr – 2.7 hr = 5.6 hr
The range is 5.6 hr
</pre>
```markdown
r<-c(7, 10, 21, 33, 43, 45, 45, 65, 67, 87, 98, 99)
max(r)-min(r)
```
### Finding fake statistics <a name="fake"></a>
Step 1: Take a close look at who paid for the survey. If you read a statistic stating 90% of people lost 20 pounds in a month on a certain “miracle” diet, look at who paid. If it was the company who owns that “miracle” product, then it’s likely you have what’s called a self-selection study. In a self-selection study, someone stands to gain financially from the results of a trial or survey. You may have seen those soda ads where “90% of people prefer the taste of product X.” But if the manufacturer of product X paid for that survey, you probably can’t trust the results.

Step 2: Take a look to see if the statistics came from a voluntary survey. A voluntary response sample is a samplewhere the participants can choose to be included in the sample or not. For example, if your professor sent you an email with an invitation to comment on what you think of a new textbook, then that would be a voluntary response sample. If it was a mandatory part of your course, then that would not be a voluntary response sample. These types of samples are not suitable for statistics because they carry a heavy bias toward people who have strong opinions (often negative ones). In other words, students are more likely to respond to the above survey if they hate the textbook. The students who like it will probably be less likely to respond.

Step 3: Look for the faulty conclusion that one variable causes another in the survey. For example, you might read a statistic that states unemployment causes an increase in corn production because corn products (like high fructose corn syrup) are cheap and therefore people are more likely to buy cheap foods when unemployed. But there may be many other factors causing an increase in production including an increase in government subsidies for corn. Just because one factor is seemingly connected to another (correlation), that doesn’t necessarily imply causation (that one caused the other). More info: see Correlation vs. Causation.
 
Studies with positive results are more likely to make it into journals, like these listed on PubMed.


Step 4: Beware of publication bias. Journals are likely to report positive results (for example, a drug trial that had a positive outcome) rather than a drug trial that failed. Just because a journal publishes a positive result doesn’t mean that there aren’t other trials out there that reported a negative result.

Step 5: Make sure the sample size isn’t too limited in scope. It’s unlikely you can make generalizations about student achievement in the U.S. by studying a single inner city school in Brooklyn. And it’s unlikely you can make generalizations about American polling behavior by standing outside a polling booth in Ponte Vedra Beach, Florida. Just as inner city schools don’t behave like every other school, an affluent neighborhood can’t be used to generalize about the voting population. Also, make sure the sample size is large enough. If your voting precinct contains 1 million voters, it’s unlikely you’ll get any good results from surveying 20 people.

Step 6: Watch out for misleading percentages. Unemployment may have “slowed by 50%,” but if the unemployment rate was previously 100,000
new unemployment claims per month, that still means 50,000 people are joining the unemployed ranks every month.

Step 7: Beware of precise numbers. If a national survey reports that 3,150,023 households in the U.S. are dog owners, you might be inclined to believe that exact figure. However, it’s highly unlikely (and almost impossible) that anyone would have seriously surveyed all of the households in the U.S. It’s much more likely they surveyed a sample and that 3,150,023 is an estimate and should have been reported as 3 million to avoid being misleading.

There are many other examples of fake statistics. Newspapers sometimes print erroneous figures, drug companies print fake test results, governments present fake statistics in their favor. The golden rule is: question every statistic that you read

```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```
###  <a name=""></a>
```markdown
```

