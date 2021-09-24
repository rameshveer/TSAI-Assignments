# Session 1 

## These assignments are done by 4 members,
1. Pratik gole
2. Bharat
3. Sujay
4. Ramesh V

## Questions and Answers

- ##### What is a neural network neuron?
    In neural networks, a neuron is a memory unit which temporarily stores the results of a computation. Inputs and outputs to/from a neuron are called weights. There can be any number of coming in and going out of a given neuron. The contents of a neuron are temporary.

- ##### What is the use of the learning rate?
    Learning rate will determine the magnitude of change on the weights while the network is trying to correct itself to come as close as possible to the desired training output. The change in weights in the initial layers have a cascading effect on the weights and results of the subsequent layers. If the learning rate is too high, it will make large changes to the weights which may result in the network output swinging wildly and probably never arriving at the optimum solution.

- ##### How are weights initialized?
    Weights are initialized randomly. The distribution of weights is usually done in a normalized way, between 0 and 1. If not restricted between 0 and 1, there is a possibility that some weights may be initialized with very high values and appear to be contributing majorly in the specific layers output. So during backpropagation, since the changes to weights take place in really small increments, it will take a longer time to correct the effect of these highly initialized weights and correctly give values to the correct weights. 

- ##### What is "loss" in a neural network?
    The difference between the expected output and actual output is called loss. We use a loss function to describe the loss, based on our use case. For example one common way of defining loss for numeric output is mean square loss. 

- ##### What is the "chain rule" in gradient flow?
    When adjusting the weights of a neural network, we need to consider the effect not only of the incoming inputs but also the effect of changing the weights of layers before that all the way to the beginning. Which means that we need to individually calculate the effect of change of weight with respect to the output for all weights and then combine them together to find the net effect of change of all the weights. This is done by taking partial derivates of error with respect to the individual weights. 

[![N|Solid](https://dz2cdn1.dzone.com/storage/temp/7914136-chain-rule.png)](https://dzone.com/articles/the-very-basic-introduction-to-feed-forward-neural)

[![N|Solid](https://dz2cdn1.dzone.com/storage/temp/7914137-eq10.gif)](https://dzone.com/articles/the-very-basic-introduction-to-feed-forward-neural)

Here we see that to calculate the change in error (e) with respect to weight 1 (w1) we chain the effects of all ways W1 has contributed towards the output by multiplying the partial derivates of the weights at each stage and then adding the results for each output neuron. 

