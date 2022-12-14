---
title: "Predictive simulations of human movement"
excerpt: "Advanced numerical methods to generate fast predictive simulations of human movement <br/><img src='/images/PredSim_1.png'>"
collection: portfolio
---

Predictive simulations generate novel movements based on a mathematical description (ie, a model) of the neuro-musculoskeletal system without relying on experimental data. Predictive simulations of movement are typically formulated as optimal control problems based on the assumption that the central nervous system optimizes performance during movement. These optimal control problems are hard to solve when using detailed musculoskeletal models with many degrees of freedom and muscles. Such models are nevertheless required to capture the complexity of human movement.

To address these computational challenges, we developed and implemented a set of numerical methods that enable fast predictive simulations of movement. These numerical methods include direct collocation, algorithmic differentiation, and implicit formulation of differential equations. Here is an example of a predictive simulation of walking, based on a complex musculoskeletal model (31 degrees of freedom, 92 muscles, 6 compliant foot-ground contacts per foot), generated using our methods in less than 20 minutes:

<p align="center">
  <img src="/images/PredictiveSimulation.gif">
</p>

This work is covered in a series of papers with associated code:

1. We use [OpenSim](https://simtk.org/projects/opensim) for modeling the musculoskeletal system and developed a custom version of the software, [OpenSimAD](https://github.com/antoinefalisse/opensimAD), to support algorithmic differentiation (AD). AD speeds up the computation of derivatives as compared to finite differences, thereby making the optimal control problems underlying predictive simulations of movement faster to solve. We supported AD in OpenSim through a custom source code transformation tool powered by [CasADi](https://web.casadi.org/).
    - [Paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0217730) 
    - [Code (Python and C++)](https://github.com/antoinefalisse/opensimAD)
    
2. We exploited predictive simulations to explore what performance criterion underlies human walking. We identified a multi-objective performance criterion combining energy and effort considerations that produces physiologically realistic walking gaits. We also exploited predictive simulations to explore the effect of mechanical assumptions on walking, and highlighted the importance of using detailed musculoskeletal models (eg, including models of the toes) to capture the salient features of walking:
    - [Paper - performance criterion](https://royalsocietypublishing.org/doi/10.1098/rsif.2019.0402)
    - [Code (Matlab) - performance criterion](https://github.com/antoinefalisse/3dpredictsim)
    - [Paper - mechanical assumptions](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0256311)
    - [Code (Python) -  mechanical assumptions](https://github.com/antoinefalisse/predictsim_mtp)
