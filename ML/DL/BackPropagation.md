# BackPropagation

<img src="./images/backprop.jpeg" alt="data" class="inline"/>

**The core idea of neural networks is to compute weighted sums of the values in the input layer and create a mapping between the input and output layer by a series of functions (in general, nonlinear functions).**

* Every neural network has an input layer, a series of hidden layers and an output layer. 

### Example
Let us take the task of classifying our images into four categories ‘cat’, ‘dog’, ‘frog’ and ‘horse’. The values in the input layer represent the pixel values of a given image that we want to classify into four categories. The small circles in each layer are called neurons. The values of the output layer represent the score for each category. We classify the image into the category that gets the highest score. For instance, if the ‘frog’ neuron in the output layer receives the highest value in comparison to the other neurons of the layer, we say the image is a ‘frog’. The other intermediary layers are called hidden layers.


### Understand the Architecture of  neuron
<img src="./images/backprop.png" alt="data" class="inline"/>

Every junction between two layers have a set of parameters called weights. These weights are not random numbers, the weight matrix between different layers can be visualized as a template or a feature that we are looking for in the image to classify it. The values of the next layer are calculated by applying a function called activation function to the values of the previous layer and the weights in between the two layers. Commonly used activation functions are sigmoid, tanh, Rectified Linear Unit (also called ReLU), leaky ReLU and Maxout. The difference between the output that we predict using the network and the actual class of the image determines the loss of the network. Greater the number of images that we classify correctly, lesser the loss. There are several ways of computing the loss of a neural network. One naive approach would be to find the mean squared error i.e, the mean of squares of the difference between the predicted and actual values. Other techniques that are often used to compute loss are softmax(cross-entropy) and support vector machine (hinge) loss. So, the aim of a neural network problem is to learn the best set of weights to give us the desired scores in the output layer. In other words, to minimize the loss function of the network.


### What is backpropagation?
Training a neural network typically happens in two phases.
#### Forward Pass:
We compute the outputs of every node in the forward pass and calculate the final loss of the network.
#### Backward Pass:
We start at the end of the network, backpropagate or feed the errors back, recursively apply chain rule to compute gradients all the way to the inputs of the network and then update the weights. This method of backpropagating the errors and computing the gradients is called backpropagation.


### A short recap of derivatives:
Let us consider the following function.
<img src="./images/backprop1.png" alt="data" class="inline"/>

Product of two variables.
<img src="./images/backprop2.png" alt="data" class="inline"/>

Partial derivatives of the function w.r.t the inputs.
It is simple enough to find the partial derivative with respect to either of the inputs. For example, if

Let us take sample values as inputs to the function.
The partial derivative on variable x ( ∂f/ ∂x) and variable y ( ∂f/ ∂y) are 3 and -2 respectively. This gives us an understanding that increasing the variable x by an amount ε would increase the output function by 3ε. Similarly, increasing the variable y by an amount ε would decrease the output function by 2ε. Thus, the derivative of a function on each variable tells us the sensitivity of the function with respect to that variable.



