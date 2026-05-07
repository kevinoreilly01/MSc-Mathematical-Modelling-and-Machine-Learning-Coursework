# Finding Untrained Attractors Using a Reservoir Computer
### Scientific Computing with Numerical Examples
### Group Project: Josh Crotty, Kevin O'Reilly, Zhijian Song

## Overview
This project investigates the phenomenon of **untrained 
attractors (UAs)**. These are unintended long-term behaviours that 
emerge in reservoir computers (RCs) trained on chaotic 
dynamical systems.

When an RC is trained to reproduce a target attractor 
such as the Lorenz system, the closed-loop reservoir 
may settle into additional attractor states never seen 
in training data. This project explores how and why 
these untrained attractors arise, and how reservoir 
hyperparameters influence their appearance.

## Key Topics
- Reservoir Computing (RC) architecture and theory
- Chaotic dynamical systems — Lorenz attractor
- Untrained Attractors (UAs) and confabulation in RCs
- Ridge regression for output layer training
- Spectral radius effects on reservoir dynamics
- Basins of attraction and initial condition sensitivity

## My Contribution (Kevin O'Reilly)
- Investigated how varying **initial conditions** and 
  **spectral radius** influence the discovery of 
  untrained attractors
- Analysed reservoir behaviour across three spectral 
  radius regimes:
  - Near 1 (edge of chaos)
  - Near 0 (stable/dampened)
  - In-between regimes
- Mapped **basins of attraction** to understand which 
  initial conditions lead to trained vs untrained 
  attractor states

## Key Findings
- Spectral radius near 1 produces dynamics at the edge 
  of chaos, most conducive to untrained attractor 
  emergence
- Spectral radius near 0 dampens reservoir dynamics, 
  suppressing untrained attractors
- Initial conditions significantly determine which 
  attractor the closed-loop RC converges to
- Basin of attraction mapping reveals clear boundaries 
  between trained and untrained attractor regions

## Methods & Tools
- Python (NumPy, Matplotlib)
- Jupyter Notebook
- Reservoir Computing framework built from scratch
- 4th-order Runge-Kutta integration for Lorenz system
- Ridge regression for readout layer training

## Background
The Lorenz system used as training data is defined by:

dx/dt = σ(y − x)  
dy/dt = x(ρ − z) − y  
dz/dt = xy − βz

For parameters (σ, ρ, β) = (10, 28, 8/3), the system 
exhibits deterministic chaos, producing the iconic 
butterfly-shaped attractor.
