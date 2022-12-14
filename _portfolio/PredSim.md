---
title: "Predictive simulations of human movement"
excerpt: "Advanced numerical methods to generate fast predictive simulations of human movement <br/><img src='/images/Gait_snapshots_sideView_white.png'>"
collection: portfolio
---

Predictive simulations generate novel movements based on a mathematical description (ie, a model) of the neuro-musculoskeletal system without relying on experimental data. Predictive simulations of movement are typically formulated as optimal control problems based on the assumption that the central nervous system optimizes performance during movement. These optimal control problems are hard to solve when using detailed musculoskeletal models with many degrees of freedom and muscles. Such models are nevertheless required to capture the complexity of human movements.

To address these computational challenges, we developed and implemented a set of numerical methods that enable fast predictive simulations of movement on standard laptop computers. These numerical methods include direct collocation, algorithmic differentiation, and implicit formulations of differential equations. 

This work is covered in a series of papers with associated code:

1. We used [OpenSim](https://simtk.org/projects/opensim) for modeling the musculoskeletal system and developed a custom version, [opensimAD](https://github.com/antoinefalisse/opensimAD), that supports algorithmic differentiation (AD). AD is a much faster alternative to finite differences to compute derivatives, which is done when solving optimal control problems.
    - [paper[(https://antoinefalisse.github.io/publication/2019_AD_PlosOne) 
    - [code (Python and C++)](https://github.com/antoinefalisse/opensimAD)
    
2. We exploited predictive simulations to explore what performance criterion underlies human walking. We identified a multi-objective performance criterion combining energy and effort considerations that produces physiologically realistic walking gaits. We also exploited predictive simulations to explore the effect of mechanical assumptions on walking, and highlighted the importance of using detailed musculoskeletal models (eg, models of the toes) to capture the salient features of walking:
    - [paper - performance criterion](https://royalsocietypublishing.org/doi/10.1098/rsif.2019.0402)
    - [code (Matlab) - performance criterion](https://github.com/antoinefalisse/3dpredictsim)
    - [paper - mechanical assumptions](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0256311)
    - [code (Python) -  mechanical assumptions](https://github.com/antoinefalisse/predictsim_mtp)
