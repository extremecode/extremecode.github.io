# Statistics
Statistically, the probability of any one of us being here is so small that you’d think the mere fact of existing would keep us all in a contented dazzlement of surprise

## Table of Contents](#)
* [What is Probability?](#WhatisProbability)
* [Random Variables](#RandomVariables)
* [Calculating Probability](#CalculatingProbability)
* [Binomial Distribution](#BinomialDistribution)
* [Continuous Random variable](#ContinuousRandomvariable)
* [Central Limit Theorem](#CentralLimitTheorem)
* [Area under a Normal Distribution](#AreaunderaNormalDistribution)
* [Z scores](#Zscores)
* [Open Challenges](#OpenChallenges)

## What is Probability? <a name="WhatisProbability"></a>
Simply put, probability is an intuitive concept. We use it on a daily basis without necessarily realising that we are speaking and applying probability to work.

Life is full of uncertainties. We don’t know the outcomes of a particular situation until it happens. Will it rain today? Will I pass the next math test? Will my favorite team win the toss? Will I get a promotion in next 6 months? All these questions are examples of uncertain situations we live in. Let us map them to few common terminology which we will use going forward.

Experiment – are the uncertain situations, which could have multiple outcomes. Whether it rains on a daily basis is an experiment.
Outcome is the result of a single trial. So, if it rains today, the outcome of today’s trial from the experiment is “It rained”
Event is one or more outcome from an experiment. “It rained” is one of the possible event for this experiment.
Probability is a measure of how likely an event is. So, if it is 60% chance that it will rain tomorrow, the probability of Outcome “it rained” for tomorrow is 0.6

### Why do we need probability?
In an uncertain world, it can be of immense help to know and understand chances of various events. You can plan things accordingly. If it’s likely to rain, I would carry my umbrella. If I am likely to have diabetes on the basis of my food habits, I would get myself tested. If my customer is unlikely to pay me a renewal premium without a reminder, I would remind him about it.

So knowing the likelihood might be very beneficial.

## Random Variables <a name="RandomVariables"></a>
To calculate the likelihood of occurence of an event, we need to put a framework to express the outcome in numbers. We can do this by mapping the outcome of an experiment to numbers.

Let’s define X to be the outcome of a coin toss.

X = outcome of a coin toss

Possible Outcomes:

1 if heads
0 if tails
Let’s take another one.

Suppose, I win the game if I get a sum of 8 while rolling two fair dice. I can define my random variable Y to be (the sum of the upward face of two fair dice )

Y can take values = (2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12)

A few things to note about random variables:

Each value of the random variable may or may not be equally likely. There is only 1 combination of dice, with sum 2{(1,1)}, while a sum of 5 can be achieved by {(1,4), (2,3), (3,2), (4,1)}. So, 5 is more likely to occur as compared to 2. On the contrary, the likelihood of a head or a tail in a coin toss is equal and 50-50.
Sometimes, the random variables can only take fixed values, or values only in a certain interval. For example in a dice, the top face will only show values between 1 and 6. It cannot take a 2.25 or a 1.5. Similarly, when a coin is flipped, it can only show heads and tails and nothing else. On the other hand, if I define my random variable to be the amount of sugar in orange. It can take any value like 1.4g, 1.45g, 1.456g, 1.4568g as so on. All these values are possible and all infinite values between them are also possible. So, in this case, the random variable is continuous with a possibility of all real numbers.
Don’t think random variable as a traditional variable (even though both are called variables) like y=x+2, where the value of y is dependent on x. Random variable is defined in terms of the outcome of a process. We quantify the process using the random variable

## Calculating Probability <a name="CalculatingProbability"></a>
Let’s say you went to a fair. There is a stall playing the game of spinning wheel. There are two colors evenly spread on the wheel – red and green. If you land on red, you lose, if you land on green you win.

So what happens when you spin the wheel? You either win or you lose? There is no third outcome in this case. If the wheel is fair, there is a 50% chance of winning and 50% chance of losing.

Next, suppose the organizer decides to increase the prize money and reduce the green area. Now only ¼th area is green and ¾th is red.

How likely are you to win now?

Only 25%! This 25% or .25 is the probability of winning.

Two throws of a dice
The next stall is our favorite dice stall, where we win if we get a sum of 8 in two throws. Let’s see if we have more chances to win here.

Let’s take random variable X to be the sum of two throws. X can take values (2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12). Let’s see the probability of each number.

Let’s see the probability of each number.

There are 6 possibilities in the first throw (we can get any number) and same 6 in the second. So total number if combinations would be 36.

Let’s see how:

2{(1,1)}  => 1/36

3{(1,2),(2,1)} => 2/36

4{(2,2),(3,1),(1,3)} => 3/36

5{(1,4),(4,1),(2,3),(3,2)} => 4/36

6{(3,3),(1,5),(5,1),(2,4),(4,2)} => 5/36

7{(1,6),(6,1),(2,5),(5,2),(3,4),(4,3)} => 6/36

8{(2,6),(6,2),(3,5),(5,3),(4,4)} => 5/36

9{(3,6),(6,3),(5,4),(4,5)} => 4/36

10{(4,6),(6,4),(5,5)} => 3/36

11{(5,6),(6,5)} => 2/36

12{(6,6)} = > 1/36

So, the chance of success here is 5/36 or approximately 1 in 7, while failure is 31/36. So, unless the stall rewards me 7x of the money I bet on winning, it is a bad game to participate in.

We can write this as:

p (Success)= 5/36
p (Failure)= 31/36
You can also see that the total probability is 1. There are only these 2 possibilities.

Let’s see how these probabilities look like. The probability function for a discrete random variable is the probability mass function. It shows the exact probabilities for a particular value of the random variable.

Here is an important thing to note, a sum of 2.5 is not possible on the throw of two dice. So essentially, my random variable is discrete. There are only fixed integer values that it can take and we can see the probabilities of each occurring.
## Binomial Distribution <a name="BinomialDistribution"></a>
## Continuous Random variable <a name="ContinuousRandomvariable"></a>
## Central Limit Theorem <a name="CentralLimitTheorem"></a>
## Area under a Normal Distribution <a name="AreaunderaNormalDistribution"></a>
## Z scores <a name="Zscores"></a>
## Open Challenges <a name="OpenChallenges"></a>
