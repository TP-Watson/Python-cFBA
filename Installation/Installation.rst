Installation
+++++++++++++

1. Clone the GitHub repository containing the cFBA Python toolbox:
You can download it from [GitHub Link].
Alternatively you can use the promot::
    git clone https://github.com/your_username/your_repository.git

2. Install the required packages using pip (if you don't have them yet):
::
    pip install python-libsbml
    pip install optlang

3. Once the required packages are installed, you can run the cFBA Python toolbox. The main file containing all the necessary functions is `py_cFBA.py`.


Usage
+++++++++++++

**Requirements**

- Stoichiometric Matrix that represents the biochemical reactions of the metabolic network.
- Imbalanced and Balanced Metabolites to be simulated.
- When Enzyme Capacities will be tested, you need to know the Enzyme-Reaction Mapping with their corresponding kcat values.


**Step-by-Step instructions to get started**

1. Import the `py_cFBA` module into your Python environment:
::
    from py_cFBA import *

2. (Optional) Generate the basic model structure in excel using the ``cFBA_backbone_from_S_matrix`` function. It only requires an S matrix and the function will guide you to input required data.
3. Include additional information to the model structure in excel. Parameters to fill out: w_matrix *weights*, upper and lower bounds, enzyme capacities. 
4. Generate an SBML file with the ``excel_to_sbml`` function.
5. Define (if needed) quotas for the simulation.
6. Test the model works with a µ = 1 (no growth), by using the function ``create_lp_problem``, using an alpha = 1. 
7. Apply the optimization algorithm by using the ``find_alpha`` function. 
8. Retrieve the simulation fluxes and amounts with ``get_fluxes_amounts`` function. 

These general steps are followed in the two examples avaialable in this documentation. 




cFBA functions
++++++++++++++

The following are the general functions within the method and how you can apply them:

- *cFBA_backbone_from_S_matrix(S_matrix)*: Function to help you generate an Excel backbone for a cFBA model based on the provided Stoichiometric matrix. Alternatively, you can generate your own model structure following the template.
-  *excel_to_sbml(excel_file, output_file)*: Takes the excel file in the format from the previous function and generates an SBML file for the cFBA method.
- *generate_LP_cFBA(sbml_file, quotas)*: Generates the basic structure of the cFBA problem.
- *create_lp_problem( alpha, cons , Mk, imbalanced_mets )*: Tests the linear program given a growth of the system (alpha = µ)
- *find_alpha(cons, Mk, imbalanced_mets)*: Optimization algorithm searching for the largest growth of the system (alpha = µ)
- *get_fluxes_amounts(sbml_file, prob)*: Retrieves the fluxes and metabolites concentrations in the optimal simulation