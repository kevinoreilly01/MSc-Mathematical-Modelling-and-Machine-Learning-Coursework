# Monte Carlo Simulations to Model Epidemic Spread
### Open Source Infrastructure for Modelling with Data
### Group Project: Chelsea O'Sullivan, Matthew Amoo, Kevin O'Reilly

## Overview
This project models epidemic spreading across three 
different network structures using Monte Carlo 
simulations and SIR/SEIRD compartmental models.

Rather than relying on deterministic differential 
equations, which would be computationally infeasible, 
we simulate discrete-time stochastic infection and
recovery events across realistic network topologies, 
capturing phenomena like superspreading, random epidemic
die-out, and structural network effects that deterministic
models cannot.

## Networks Implemented
- **Erdős–Rényi (ER)** — random graph baseline, 
  homogeneous mixing
- **Watts–Strogatz** — small-world network with high 
  clustering and short path lengths
- **Barabási–Albert (BA)** — scale-free network with 
  preferential attachment and superspreader hubs

## Epidemic Models Used
- **SIR** — Susceptible, Infected, Recovered
- **SEIR** — adds Exposed compartment (incubation 
  period)
- **SEIRD** — adds Death compartment for high-mortality 
  diseases

## My Contribution (Kevin O'Reilly)
- Implemented and analysed the **Barabási–Albert 
  scale-free network**
- Plotted and validated the **power-law degree 
  distribution** on a log-log scale across 20 
  simulations
- Ran **Monte Carlo SIR and SEIRD simulations** on the 
  BA network with 200 realisations and 95% confidence 
  intervals
- Investigated the role of **superspreader hubs** in 
  accelerating epidemic growth
- Analysed the effect of varying **β (transmission 
  rate)** and **γ (recovery rate)** on outbreak 
  trajectories
- Wrote the **Conclusion** chapter synthesising 
  findings across all three network models

## Key Findings
- Network structure is a dominant factor in epidemic 
  behaviour
- BA scale-free networks produce earlier, sharper 
  infectious peaks due to hub superspreading
- Watts-Strogatz networks slow early spread through 
  local clustering but shortcuts still drive significant 
  outbreaks
- ER networks behave like well-mixed populations. 
  Monte Carlo averages closely match deterministic 
  mean-field solutions
- Higher β increases peak prevalence and accelerates 
  outbreak timing; lower γ amplifies and prolongs 
  epidemics
- Monte Carlo averaging across 100-200 runs removes 
  stochastic noise and produces stable epidemic 
  trajectories

## Tools & Technologies
- Python (NumPy, NetworkX, Matplotlib)
- Jupyter Notebook
- Monte Carlo simulation framework built from scratch
- SIR, SEIR, SEIRD compartmental modelling
- Random walk diffusion analysis

## Background
The three network models represent increasing levels 
of real-world complexity:
