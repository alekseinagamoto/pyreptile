# [reptile](https://blog.openai.com/reptile/)
illustrative example of openai's [reptile](https://arxiv.org/abs/1803.02999), a meta-learning algorithm. reptile works by repeatedly sampling a task, performing stochastic gradient descent on it, and updating the initial parameters towards the final parameters learned on that task. 

## what is meta-learning?
in meta-learning problems, there is a distribution of tasks, and we would like to obtain an agent that performs well (i.e., learns quickly) when presented with a previously unseen task sampled from this distribution.

## example
we initially fit a model (nn with one hidden layer) on ten randomly generated sine curves, each parameterized with a unique phase, amplitutde, and bias. for each curve, 500 data points are randomly selected for training. the agent then learns a new sine curve using only 25 datapoints. in other words, it learns a new curve with 95% less data.