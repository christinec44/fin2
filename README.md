# Final Project
## Part II
### Six Dimensionl Cube Integral

This code computes the electrostatic potential energy between two cubes separated by a distance, yet non-uniform charge density. This is done by computing a six dimensional integral based upon each of the 3 local coordinates of each cube. I computed the integral using a vegas method and a home-made monte carlo method, which was used for comparison. I calculated the dipole approximation for the integation to estimate the potential energy between the cubes. All three of these are plotted against the distance shown in the figure below with a base-2 logarithmic x-axis and base-10 logarithmic y-axis. 

![Cube model](cubes.png "Integral of Cubes")

Timing between the vegas integration and the homemade integration yield run times of ~277 and ~14.5s respectively. The monte carlo method converges like 1/sqrt(N), where N is the total number of monte carlo steps. After calculations I found that I need to increase the computations by a factor of 13.76^2 on my homemade integration to achieve the same accuracy as the vegas method. Increasing the number of computations in return then increases the runtime. It would make my monte carlo run for ~2,745.43s, which is ~0.76 hours.

This code is an edited version of the code provided by Dr. Michael Rozman for Physics 2200 at the University of Connecticut.
