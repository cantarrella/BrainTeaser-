# Simulate a Random Vector (uniformly) from a simplex

## [Stackexchange](https://stats.stackexchange.com/questions/289258/how-to-simulate-a-uniform-distribution-of-a-triangular-area/289363)

## [Paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.159.912&rep=rep1&type=pdf)
- Algorithm1: Sample (K-1) standard uniform RVs {x_k}, ordered them into  {x_{k}}, define v_i=x_{i}-x_{i-1}, get vector V={v_i}

- Algorithm2: sample K exponential RVs {x_k}, get v_k=x_k/ \sum_{x_i}.

## Key Idea
Poisson Process, order statistics


# [Simulate Markov Chain](http://www.columbia.edu/~ks20/4703-Sigman/4703-07-Notes-MC.pdf)

## Discrete Markov Chain
As long as {P_ij, given i} is known, simulate a uniform RV on [0,1]. Then check where it falls.

## Continuous Time Markov Chain(CTMC)
Definition: \
P(X(s + t) = j|X(s) = i, {X(u) : 0 ≤ u < s}) = P(X(s + t) = j|X(s) = i) = Pij (t).\
\
Pij (t) represents the probability that the chain will be in state j, t time units from now, given it is in state i now.\
Letting X_n denote the state right after the n-th transition, yields the underlying discretetime
Markov chain, called the embedded Markov chain; it moves according to a transition matrix P = (Pij ).\
\
Similar definition, given state i, the time t the state will hold until a change to state j follows expoential distribution of Q_ij. 
Due to the property of exponential distribution, the holding time of i follows expoential distribution of Q_i=sum_j(Q_ij).\
\
Simulate an exp RV of Q_i, and then choose a new state c from a discrete probability distribution with probability masses Q_ic/Q_i.\

Related Papers: [P1](http://www.columbia.edu/~ks20/4703-Sigman/4703-07-Notes-MC.pdf), [P2](https://arxiv.org/pdf/0910.1683.pdf)

