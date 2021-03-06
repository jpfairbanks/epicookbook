---
title: 'Exact recursive expressions'
permalink: 'chapters/blackross2015/intro'
previouschapter:
  url: chapters/finalsize
  title: 'Final size of an epidemic'
nextchapter:
  url: chapters/blackross2015/matlab
  title: 'Original Matlab code'
redirect_from:
  - 'chapters/blackross2015/intro'
---

## Exact recursive expressions for final size

Author: Sangeeta Bhatia @sangeetabhatia03

Editor: Simon Frost @sdwfrost

Date: 2018-10-02

In a closed population, there is often interest in the total number of people infected, also known as the final size. Although simulations can be used (either [deterministic](http://epirecip.es/epicookbook/chapters/sir/intro) or [stochastic](http://epirecip.es/epicookbook/chapters/sir-stochastic-discretestate-continuoustime/intro)) can be used, there are more efficient methods for computing the final size.of a simple SIR model but the method can be generalised to other models.

The details are available in [Black and Ross (2015)](https://doi.org/10.1016/j.jtbi.2014.11.029). Instead of keeping tab of the population counts for each compartment ($S$, $I$, $R$), we keep a record of the number of infection and recovery events. At time t, let the number of infection events be $Z_1$ and the number of recovery events be $Z_t$. Then the state of our model is $(Z_1, Z_2)$. From one state to another, we can have at most one  infection event or a single recovery event. Thus from $(Z_1, Z_2)$, the system can transition to $(Z_1 + 1, Z_2)$, $(Z_1, Z_2 + 1)$. To estimate the distribution of the final size, one needs to calculate the probability of 
all paths leading up to the state from which the system cannot transition $(Z, Z)$. The probabilities can be calculated easily by the states are indexed.

### References

- [Black and Ross (2015)](https://doi.org/10.1016/j.jtbi.2014.11.029).
