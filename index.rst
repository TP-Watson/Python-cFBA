.. cFBA Python documentation master file, created by
   sphinx-quickstart on Tue Mar 26 11:56:52 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Conditional Flux Balance Analysis in Python
=======================================

Introduction
+++++++++++

This ``cFBA Python toolbox`` toolbox provides a set of functions to facilitate 
the implementation of conditional Flux Balance Analysis (cFBA) in Python for 
researchers interested in predicting metabolic responses in dynamic-cyclic 
environments. 


What is cFBA?
-------------

cFBA is a mathematical framework [#Rugen2015]_ [#Reimers2017]_ that integrates 
stoichiometric modeling, dynamic Flux Balance Analysis (dFBA), and resource 
allocation to study metabolism in organisms living in cyclic environments. It 
allows researchers to simulate and analyze metabolic reactions under changing 
environmental conditions, such as **day/night** cycles, **feast/famine** 
conditions, **aerobic/anaerobic** exchanges, etc. 



Key Features of cFBA
--------------------

- **Dynamic Simulation:** cFBA allows for the simulation of metabolic reactions over time, capturing the dynamic behavior of biological systems.
- **Resource Allocation:** The method considers optimal resource allocation strategies, shedding light on how organisms prioritize metabolic pathways in response to changing conditions.
- **Cyclic behavior:** The method implements a constraint that maximizes biomass growth while maintaining the biomass composition equal at start and end point, simulating an organism adapted to cyclic environments. 


How to Use This Documentation
-----------------------------

This documentation provides detailed instructions on how to install and use the cFBA 
Python toolbox. Whether you're new to cFBA or an experienced user, you'll find 
everything you need to get started, including installation guides, usage examples, 
and troubleshooting tips.



References
----------------------------------------------------------

.. [#Rugen2015] Rügen, Marco, Bockmayr, Alexander, and Steuer, Ralf (2015), 'Elucidating temporal resource allocation and diurnal dynamics in phototrophic metabolism using conditional FBA', Scientific reports, 5, 15247.
.. [#Reimers2017] Reimers, Alexandra-M, et al. (2017), 'Cellular trade-offs and optimal resource allocation during cyanobacterial diurnal growth', Proceedings of the National Academy of Sciences, 114 (31), E6457-E65.


_____________


.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Method:

   Method/Constraints
   Method/Capacities
   Method/Optimization 



.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Installation:
   
   Installation/Installation

.. toctree::
   :maxdepth: 3
   :hidden:
   :caption: Examples:

   Examples/MinCell 1
   Examples/MinCell 1 with quotas
   Examples/MinCell 2
   Examples/MinCell 3
   Examples/MinCell 4
      


.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Contributions:
   
   Contributions & Guidelines/Contributions
   Contributions & Guidelines/Contributing guidelines

