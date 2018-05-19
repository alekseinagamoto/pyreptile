# [reptile](https://blog.openai.com/reptile/)
illustrative example of openai's [reptile](https://arxiv.org/abs/1803.02999), a meta-learning algorithm. 

reptile works by repeatedly sampling a task, performing stochastic gradient descent on it, and updating the initial parameters towards the final parameters learned on that task. 

## what is meta-learning?
in meta-learning problems, there is a distribution of tasks, and we would like to obtain an agent that performs well (i.e., learns quickly) when presented with a previously unseen task sampled from this distribution.

## example
we initially fit a model (nn with one hidden layer) on ten randomly generated sine curves, each with a different phase, amplitutde, and bias. for each sine curve, 500 data points is randomly selected for training data.

this model then learns a new sine curve with only 25 datapoints. (in other words, the model will learn a new sine curve with 95% less data.)