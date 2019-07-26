# Deep Learning

_Deep Learning has received a lot of hype in recent years due to its impressive performance on many applications, including language translation, medical diagnosis from X-rays, recognizing images to help with self-driving cars, beating the top Go players as well as beating high-ranking DotA players, learning how to play Atari games just from the pixel data… all these to name a few of Deep Learning’s recent accomplishments! In this post, we will (gently) introduce you to the inner workings behind Deep Learning at an intuitive level._

## **What is Machine Learning? And how is Machine Learning any different from “traditional algorithms”?**
### traditional Approach
If you’ve taken a class on algorithms, the standard metaphor for an algorithm is a recipe. An algorithm is a series of steps, that when performed in a specific order, produced your desired output. A “cooking algorithm” for a robot to make bread might go something like this:
Add to a large bowl 3 cups of flour, 1 tablespoon of salt and 3 tablespoons of sugar.
In a separate bowl, dissolve 1 package of yeast in warm water.
Combine the two bowls and knead for 10 minutes.
And so on… (I’m not a bread expert, so I shan’t write a recipe for bread here)
### ML Approach
In Machine Learning, we don’t specify the algorithm the way we did above. Rather, we specify the template (or the “architecture”) on what shape the cooking recipe might take:
Add to a large bowl __ cups of flour, __ tablespoon of salt and __ tablespoons of sugar.
In a separate bowl, dissolve __ package of yeast in warm water.
Combine the two bowls and knead for __ minutes.

### Lets try to understand
The blanks are numbers that are not specified in the beginning but we will have to find out. We then write an algorithm (another series of instructions) to figure out those numbers according to what is “best” (we’ll define this later), relying on the data that we have access to.
At a very high level, the task of Machine Learning is thus two-fold:
Find the best template that is best suited for the task. Deep Learning is simply a subset of the templates we get to choose from that have proven effective across many tasks.
Use the data to figure out what are the best numbers to fill up the template. This is the “Learning” part of “Machine Learning”.

To give a more concrete example, consider the task of predicting house prices based on features such as house size (in sq m), number of stories, distance to nearest school (in m) etc.
```markdown
A standard algorithm might perhaps be something like this: The house price is approximately (100 * house size) + (1000 * number of stories) — (30 * distance to nearest school. A (parametric) Machine Learning approach would look something like this:
Step 1: I’ve specified the template: The house price is __ * house size + __ * number of stories + __ * distance to nearest school.
Step 2: Looking at the data of all the houses I have listed, it seems that the best numbers to fill in the blanks is (90.3, 1006.2, -40.5) respectively.
```

### examples of such input-output pairs are:
* Input: Image (a series of pixels) from a photograph; Output: TRUE/FALSE on whether there is a car in the image or not
* Input: Image (a series of pixels) from a Chest X-Ray; Output: Probability on the likelihood the person has a chest infection
* Input: Sound Recording of a customer-service call; Output: A prediction on how the customer felt about the call with a score from 1–10
* Input: Sequence of words in English; Output: The corresponding translation in French

### Idea
Summary: Machine Learning consists of two steps: specify a template and find the best parameters for that template.



## Deep Learning 
Deep Learning is simply a subset of the architectures (or templates) that employs “neural networks” which we can specify during Step 1. “Neural networks” (more specifically, artificial neural networks) are loosely based on how our human brain works, and the basic unit of a neural network is a neuron.
At the basic level, a neuron does two things:
Receive input from other neurons and combine them together
Perform some kind of transformation to give the neuron’s output
In (1), we often take some linear combination of the inputs. In layman terms, if we had three inputs to the neuron (let’s call them x1, x2, and x3), then we would combine them like this:




<img src="./images/dl_intitution.png" alt="data" class="inline"/>

where the individual blanks are parameters to be optimized for later (i.e. learn from the data what numbers best fill in those blanks). In mathematical terms, the blanks that are attached to the inputs (x1, x2 and x3) are called weights and the blank that is not attached to any input is called the bias.
With the linear combination, we apply some function (called the activation function) to achieve our eventual output. Common examples of these functions are:
Sigmoid Function (A function which ‘squeezes’ all the initial output to be between 0 and 1)
tanh Function (A function which ‘squeezes’ all the initial output to be between -1 and 1)
ReLU Function (If the initial output is negative, then output 0. If not, do nothing to the initial output)
That’s all there is to a neuron!

<img src="./images/dl_intitution.png" alt="data" class="inline"/>
