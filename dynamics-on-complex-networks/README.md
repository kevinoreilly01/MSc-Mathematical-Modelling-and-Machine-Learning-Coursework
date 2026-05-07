# Dynamics on Complex Networks
### Group Project: Fergal Brennan, Kevin O'Reilly

## Overview
This project investigates how network structure 
influences three fundamentally different dynamical 
processes, synchronisation, simple contagion and 
complex contagion, across three canonical network 
models.

A key finding is that no single network structure 
optimises all dynamical processes, revealing a 
fundamental trade-off between global connectivity 
and local clustering depending on the type of 
dynamics being studied.

## Networks Investigated
- **Erdős–Rényi (ER)** — random graph, Poisson degree 
  distribution, homogeneous mixing
- **Watts–Strogatz (WS)** — small-world network, high 
  clustering, short path lengths
- **Barabási–Albert (BA)** — scale-free network, 
  power-law degree distribution, hub-dominated topology

## Dynamical Processes Studied
- **Kuramoto Model** — synchronisation of coupled 
  phase oscillators
- **Threshold Model** — complex contagion requiring 
  multiple exposures (e.g. adopting a new behaviour)
- **SIR Model** — simple contagion epidemic spreading

## My Contribution (Kevin O'Reilly)
- Wrote the **Introduction** — network properties, 
  graph Laplacian, algebraic connectivity
- Implemented the **Kuramoto synchronisation model** 
  across all three networks
- Implemented the **Threshold (complex contagion) 
  model** across all three networks
- Analysed **network characteristics** — degree 
  distributions, clustering coefficients, path lengths, 
  algebraic connectivity
- Produced results for **Kuramoto synchronisation** 
  and **complex contagion threshold cascades**
- Verified the theoretical prediction that critical 
  coupling Kc is inversely proportional to algebraic 
  connectivity λ₂

## Key Findings

### Kuramoto Synchronisation
| Network | Algebraic Connectivity λ₂ | Critical Coupling Kc |
|---|---|---|
| Barabási–Albert | 1.412 | 1.0 |
| Erdős–Rényi | 0.713 | 1.17 |
| Watts–Strogatz | 0.364 | 2.0 |

- BA networks synchronise most easily — hubs act as 
  stable reference points and increase λ₂
- WS networks resist synchronisation — local clusters 
  lock to different phases, poor global connectivity
- Results confirm the theoretical prediction: Kc is 
  inversely proportional to λ₂

### Complex Contagion (Threshold Model)
| Network | Mean Cascade Size |
|---|---|
| Watts–Strogatz | 64% ± 47% |
| Barabási–Albert | 53% ± 47% |
| Erdős–Rényi | 36% ± 45% |

- WS networks produce the largest cascades — local 
  clustering creates reinforcing triangles where 
  multiple neighbours adopt simultaneously
- BA networks underperform — hub neighbours rarely 
  connect to each other, so single-hub adoption 
  rarely crosses the 25% threshold
- Results reveal a direct trade-off: what helps 
  synchronisation (hubs) hinders complex contagion, 
  and vice versa (clustering)

### SIR Epidemic Spreading
- BA networks spread infection fastest — hubs act as 
  superspreaders creating cascading infections
- WS networks spread slowest — community structure 
  contains local outbreaks with limited shortcuts
- ER networks spread evenly — uniform degree 
  distribution produces predictable mean-field behaviour

## Core Conclusion
> Global coordination processes (synchronisation, 
> epidemic spreading) benefit from hub-dominated 
> networks. Processes requiring reinforcement 
> (complex contagion) depend on clustered local 
> structure. No single network optimises both.

## Tools & Technologies
- Python (NumPy, NetworkX, SciPy, Matplotlib)
- Jupyter Notebook
- Kuramoto model integrated using scipy.integrate.odeint
- Graph Laplacian eigenvalue analysis via 
  numpy.linalg.eigenvalsh
- 500 Monte Carlo SIR runs per network
