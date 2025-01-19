# Project Population Biology

Code for simulations of one predator and two non-competing prey using an extension of the Lotka-Volterra predator-prey to n prey species (or resources) with density-dependent growth:

\frac{dR_k}{dt} &= r_k R_k \left( 1 - \frac{R_k}{K_k} \right) - a_k R_k P \\
\frac{dP}{dt} &= B P \left( \sum_{k=1}^2 \left( a_k b_k R_k \right) - C \right).
