The python script included here is a supplementary tool for computing vertical profiles for velocity and particle concentration from the depth-averaged values. 

This tool computes the flow vertical profiles from the depth-averaged values, which can be the solid volume fraction, the depth-averaged mixture density, the mixture velocity, or the mixture momentum. When the mixture momentum is given, an iterative procedure is employed to compute the depth-averaged density and velocity, and their vertical profiles. In this case, the Python tool initializes a guess for the depth-averaged velocity and starts an iteration loop.

Within the loop, a function is called to compute the mixture density and the depth-averaged value of a flow property using the current guess of the depth-averaged velocity. The depth-averaged velocity is then updated using the computed values, and the process is repeated with the updated velocity to refine the estimate. An Aitken acceleration scheme is applied to improve the convergence of the iteration. The loop continues until the convergence criteria are met or the maximum number of iterations is reached, at which point the final depth-averaged velocity is obtained.

The capability to find the profiles when the depth-averaged mixture density and momentum are given is particularly relevant, because depth-averaged models solve for these variables, and thus the numerical implementation of the Python code can also be ported to these models.

This tool computes the concentration profiles not only for the solid phase as a whole, but also for the individual solid classes with different sizes and densities (and thus different settling velocities).

We assume the depth-averaged total grain size distribution (TGSD) being defined by a normal distribution in the Krumbein logarithmic phi scale, with mean mu and standard deviation sigma, resulting in specific relative mass fractions on a binned phi scale.

The tool then, from the computed concentration vertical profiles of the different classes, allows the user to compare the depth-averaged TGSD, the basal TGSD, and the bins relative mass fractions that are sedimented (lost) into the basal portion of the flow (from the settling velocities and bottom fractions of solid particles).
