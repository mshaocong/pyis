This is an extension of a simulation course project I have taken in the past. A general frame for importance sampling is implemented here. This branch will contains the following part: 

1. Sampling a stochastic process (under the objective measure). 

2. Change of measure - usually we want to sample the stochastic process from a different measure (given the Radon-Nikodym density).

3. Siegmund algorithm.

4. I will write a note about its application in simulation; and I plan to test it on a real financial dataset.

# A brief introduction to importance sampling

[Importance sampling](https://en.wikipedia.org/wiki/Importance_sampling) is a well-known variance reduction technique. It has been used in many fields including simulation, finance, and machine learning. The general idea is, for example, when we want to estimate an expectation of a random variable, instead of sampling it under the objective measure, we sample it under a better measure such that the variance of our estimator is much smaller.   

# Sampling a Markov process
In `mc_generator.py`, a usual method used to simulate a Markov processes is implemented. In `Markov process.ipynb` notebook, several examples are introduced, including the following part

* Sample some classical processes such as Brownian motion or Poisson process.

* Sample an Ito diffusion such as [CIR diffusion](https://en.wikipedia.org/wiki/Cox%E2%80%93Ingersoll%E2%80%93Ross_model)

* Sample a couting process given its intensity. Its intensity may depend on the process itself.

# Importance Sampling
Consider several cases of rare event. Use IS to estimate the probability.
