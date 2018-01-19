# Simulate a uniformly ditributed vector of size K from a simplex

## [Stackexchange](https://stats.stackexchange.com/questions/289258/how-to-simulate-a-uniform-distribution-of-a-triangular-area/289363)

## [Paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.159.912&rep=rep1&type=pdf)
- Algorithm1: Sample (K-1) standard uniform RVs {x_k}, ordered them into  {x_{k}}, define v_i=x_{i}-x_{i-1}, get vector V={v_i}

- Algorithm2: sample K exponential RVs {x_k}, get v_k=x_k/ \sum_{x_i}.

## Key Idea
Poisson Process, order statistics
