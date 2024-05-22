Capacities
+++++++++++++

**Reaction bounds**


The reactions in the model can be constrained with upper and lower bounds as done typically in `FBA`, only that here these bounds are specified for each time interval. 


.. note::
    Upper and lower bounds can be used to simulate environmental conditions. For example:
    
    - Ub oxygen uptake = 0; simulates anaerobic conditions.
    - Lb uptake substrate > 1; simulates feeding into the system.

**Enzyme capacities** 


A reaction `'r'` can be additionally constrained by its upper limit following the relation:

.. image:: Methods_img6.jpg

This relation indicates that the fastest rate a reaction can have is limited by the amount of a catalyst (an imbalanced metabolite) and the kcat value of said catalyst. The implementation of said relation is incorporated by using the following matrices:

- A_cap: Matrix containing the inverse `kcat` value for each reaction (number of columns) catalyzed by each meatbolite in B_cap (number of rows).
- B_cap: Matrix indicating which of the imbalanced metabolites (number of columns) serves as a catalyst of a reaction (each row for a reaction).

An example on how to build A_cap and B_cap for a system with 
multiple enzymes is presented in :doc:`MinCell 3</Examples/MinCell 3>`