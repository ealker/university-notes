# Artificial Neural Networks 

# What are artificial neural networks? 

Artificial neural networks attempt to model the networks of neurons in a biological brain. The difference between traditional artifical intelligence and machine learning techniques like artificial neural networks is that the former is based on symbolic reasoning (learning) and the later is sub-symbolic. A symbolic learner follows a set of rules, which humans can generally understand - researchers can therefore understand how such a system draws conclusions from data because they can follow the path from input to output. The latter, sub-symbolic systems, operate differently. In such systems, humans have no understanding or control of the processes that determine how a test example is classified. 

> For example, in image recognition, they might learn to identify images that contain cats by analyzing example images that have been manually labeled as "cat" or "no cat" and using the results to identify cats in other images. They do this without any prior knowledge of cats, for example, that they have fur, tails, whiskers and cat-like faces. Instead, they automatically generate identifying characteristics from the examples that they process.

> [Symbolic vs Subsymbolic Notes (MIT)](https://courses.media.mit.edu/2016spring/mass63//wp-content/uploads/sites/40/2016/02/Symbolic-vs.-Subsymbolic.pptx_.pdf)

Artificial neural networks can be considered a supervised learning method; it approximates a function that maps a set of inputs to a set out of outputs, based on training data (a set of input-output pairs). 

## How do artificial neural networks work?

An ANN is made up of various "layers" of "neurons". An input layer of `x` neutrons is connected to every other neutron in a second hidden layer, with every neutron in the second layer connected to every other neutron in the third layer and so on. These "hidden layers" then feed into a single neutron in the "output layer". 

> ... a densley interconnected set of simple units, where each unit takes a number of real-valued inputs (possibly the outputs of other units) and produces a single real-valued output (which may become the input to many other units)."

These units modelled on neurons are called nodes. Each input node brings into the network the value of one independent variable.

A neuron in an ANN will fire when some threshold is reached 

## What is the motivation behind artificial neural networks?

The original goal was to model the human brain, however, given the previous explanation of how ANN work, problems quickly become apparent. The human brain contains `10^11` neurons, and each neuron is conntected to `10^4 (10,000)` other neurons - the product of those two numbers is ridiculously large. 

A key motivation behind wanting to model the human brain is that it can process multiple "jobs" simletaneously; it can be thought of as a highly parallel distributed system. 


======== Lecture 2 ==========

Recap: 

Built on neurons - modelled on biological neuron. We can model very simple functiosn via perceptron. There are many types of neurons with different activation functions (linear, logistic, perceptron).

Perceptron - step funtction output is a function of the vector x and the weights (theta). f = x0theta + x1theta1... xDThetaD. Inputs plus the weights of the inputs. When the sum exceeds the threshold then the output will change. 

An activation function transforms the neurons input into output. A step or sign function is non-differential. 

Each input node --> brings value of one independent variable into the network. 

Hidden layers do most of the work. 

Output nodes give results.



## Types of Neurons 

- Perceptrons 
- Linear
- Logistical (Sigmoidal Activation Function)



## Backpropogation 

Backpropogation (backpropogation of errors) is a learning rule (algorithm) for ANNs. 

## Perceptrons 

If the examples are linearly seperable, use the perceptron training rule. If the training examples are not linearly seperable, then the delta rule with gradient descent algorithm is used. 

### Perceptron Training Rule 


### Delta Rule 

This uses gradient descent to 







