# 3DOF rocket-Simulation
This is my final project for the "Multivariable linear system control" module. This repo contains a 3DOF (two planar coordinates, one rotational coordinate)
simulation of a thrust vectoring vehicle. This repo contains the Simulink dynamics model, a Matlab file with mass properties and my
final report.

## The Simulation
The translational dynamics were modelled by Newton's Second Law, and the attitude dynamics were modelled by T=Ia.
The control scheme is full state feedback designed via pole placement and linearizing the dynamics around
a hover. The true state measurements were corrupted with Gaussian noise and then passed to an Extended Kalman Filter. In addition,
a saturation block was added to cap the thrust and the thrust vector angle.

The vehicle attempts to follow a reference trajectory that contains an ascent, translation, and then landing.
