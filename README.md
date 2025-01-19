# Project Population Biology and Modeling

Code for simulations of one predator and two non-competing prey using an extension of the Lotka-Volterra predator-prey to n prey species (or resources) with density-dependent growth:

## Mathematical Model

The system is modeled by the following set of differential equations:

### Prey Dynamics:

For each prey species ($R_k$) (where ($k = 1, 2, \dots, n$)):

$$
\frac{dR_k}{dt} = r_k R_k \left( 1 - \frac{R_k}{K_k} \right) - a_k R_k P
$$

Where:
- ($R_k$) is the population of prey species 
- ($r_k$) is the intrinsic growth rate of prey species 
- ($K_k$) is the carrying capacity of prey species
- ($a_k$) is the predation efficiency of prey species 
- ($P$) is the predator population.

### Predator Dynamics:

For the predator population (P):

$$
\frac{dP}{dt} = B P \left( \sum_{k=1}^{n} a_k b_k R_k - C \right)
$$

Where:
- ($P$) is the predator population,
- ($B$) is a conversion factor from prey ingestion to predator reproduction
- ($a_k$) is the predation efficiency of prey species 
- ($b_k$) is the nutritional value of prey
- ($C$) is an energetic “maintenance cost” of the predator.
