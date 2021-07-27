# DTItool
Drug Target Identifier Toolbox (DTItool) is an application of Rapid-SL and designed for the identification of potential drug targets. 

## Requirements
The following tools are needed to use RapidSL for finding synthetic lethal sets:
1. [COBRA Toolbox](https://opencobra.github.io/cobratoolbox/stable/)
2. CPLEX v12.9.0 or higher.\
tested on MATLAB 2019a.

## DTItool overview:
![alt text](https://github.com/CSBLaboratory/DTItool/blob/main/DTItool_Info.jpg)

### 1: File
This menu contains four submenus:\
**Import Model**: to import new model.\
**Export Model**: to export the current model to a .mat file. All chenges will be saved.\
**Import Bounds**: to import reaction bounds from an Excel file with a specific format; use Export Bounds submenu to obtain this Excel file.\
**Export Bounds**: to export and save the reaction bounds to an Excel file.

### 2: Options
This menu contains four submenus: \
**Exclude Exchange Reactions**: to exclude all exchange reactions from the analysis (default: checked).\
**Exclude Diffusion Reactions**: to exclude all diffusion reactions from the analysis (default: checked).\
**Exclude Spontaneous Reactions**: to exclude all exchange reactions from the analysis (default: checked).\
**Metabolite-Centric Approach**: to include only the reactions related to the _choke point_ metabolites (default: unchecked).
  
### 3: Help
This menu contains one submenu:\
**GitHub Link**: lined to this _README.md_ file.

### 4: Show Only Exchange Reactions
This checkbox helps the user to explore only the exchange reactions of the model. If checked, only exchange reactions will be shown in the table of reactions.

### 5: Table of the Reactions And the Related Bounds
The first column shows the reaction abbreviations of the model.\
The second column shows the lower bounds of the reactions.\
The third column shows the upper bounds of the reactions.\
The reaction bound **can be changed directly** from the table.

### 6: Objective to Attack
Choose the type of analysis:\
**Proliferation (Biomass Production)**: to perform the convenient lethality analysis.\
**Virulence Factor Production**: to perform an analysis to find the sets that prevent the production of the selected virulence factors (the list is shown in part 14). Parts 8, 9, 10, 14, 15 will be activated by selecting this type of analysis.

### 7: Type of Sets
This part defines the types of the reported _sets_. Choose _Reaction Sets_ to find reaction sets or _Gene Sets_ to find gene sets.

### 8: Search box
This search box helps the user to find the virulence factors between the metabolites by typing a part of the metabolite name in this box.

### 9: Table of the Metabolite Names
All names of the metabolites in the model is shown in this table. Each metabolite can be selected by clicking on its name.

### 10: Add Virulence Factors to the List
The selected metabolite in the table can be added to the list of virulence factors by clicking on this button.

### 11: List of Virulence Factors
All selected virulence factors will be shown in this table.

### 12: Remove Virulence Factors from the List
The selected metabolite in the related table can be removed from the list of virulence factors by clicking on this button.

### 13: Number of Workers
The number of workers can be changed by editing this item and clicking on the _Reset Number of Workers_ button (part 14). The default number of workers is 4.

### 14: Reset Number of Workers
This push button will be activated when the value in the _part 13_, is not the same as the current number of workers. Click on this push button to change the number of workers.

### 15: Maximum Cardinality
The maximum desired cardinality can be changed here.

### 16: Cutoff Ratio
The cutoff ratio for the analysis. This value is multiplied by the wild-type flux of the objective function to define the critical value of lethality or production of the virulence factor.

### 17: Start Analysis
To run the analysis click on this push button. After clicking on this button, the user should select a name and a path for the excel file of the results. For _Virulence Factor Production_, if more than one virulence factor is selected, the results for each factor is reported in a separated sheet in the excel file, and combined results (minimal sets) for preventing the production of all selected virulence factors is stored in the last sheet of the excel file.


## Example for Performing the Lethality Analysis:
**1) Use the default model (iAF1260) or select another model using the _File/ Import Model_ menu.**\
**2) Change the reaction bounds (if needed) or load the reaction bounds using the _File/ Import Bounds_ menu.**\
**3) Select the maximum desired cardinality from the _Maximum Cardinality_ spinner.**\
**4) Click on the _Start Analysis_ push button to start the analysis.**\
**Results:** The results is reported in an excel file. For _Virulence Factor Production_, if more than one virulence factor is selected, the results for each factor is reported in a separated sheet in the excel file, and combined results (minimal sets) for preventing the production of all selected virulence factors is stored in the last sheet of the excel file.
