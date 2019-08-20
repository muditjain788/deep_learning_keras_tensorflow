# NOTES 

Lets see a model:-

![image1](https://pythonprogramming.net/static/images/machine-learning/artificial-neural-network-model.png)
- A basic neural network consists of an input layer, which is just your data, in numerical form
- After your input layer, you will have some number of what are called "hidden" layers. 
- A hidden layer is just in between your input and output layers. One hidden layer means you just have a neural network.
- Two or more hidden layers? Boom, you've got a deep neural network!


Why is this? Well, if you just have a single hidden layer, the model is going to only learn linear relationships.

** If you have many hidden layers, you can begin to learn non-linear relationships between your input and output layers **

A single neuron might look as follows:

![image 2] (https://pythonprogramming.net/static/images/machine-learning/artificial-neuron-model-sigmoid-activiation-function.png)

- So this is really where the magic happens. The idea is a single neuron is just sum of all of the inputs x weights, fed through some sort of activation function. 
- The activation function is meant to simulate a neuron firing or not. 
- Simple example would be a stepper function, where, at some point, the threshold is crossed, and the neuron fires a 1, else a 0
- Let's say that neuron is in the first hidden layer, and it's going to communicate with the next hidden layer.
- So it's going to send it's 0 or a 1 signal, multiplied by the weights, to the next neuron, and this is the process for all neurons and all layers.
- 
