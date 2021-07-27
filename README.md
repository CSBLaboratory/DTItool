# DTItool
Drug Target Identifier Toolbox (DTItool) is an application of Rapid-SL and designed for the identification of potential drug targets. 

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
This checkbox helps the user to explore only in the exhcange reactions of the model. If checked, only exchange reactions will be shown in the table of reactions.

### 5: Table of the Reactions And the Related Bounds
The first column shows the reaction abbreviations of the model.\
The second column shows the lower bounds of the reactions.\
The third column shows the upper bounds of the reactions.\
The reaction bound **can be changed directly** from the table.

### 6: Objective to Attack
Choose the type of the analysis:\
**Proliferation (Biomass Production)**: to perform the convenient lethality analysis.\
**Virulence Factor Production**: to perform an analysis to find the sets which prevents the production of the selected virulence factors (the list is shown in part 14). Parts 8, 9, 10, 14, 15 will be activated by selecting this type of analysis.

### 7: Type of Sets
This part defines the types of the reported _sets_. Choose _Reaction Sets_ to find reaction sets or _Gene Sets_ to find gene sets.

### 8: Search box
This search box helps the user to find the virulence factors between the metabolites by typing a part of the metabolite name in this box.

### 9: Table of the Metabolite Names
All names of the metabolites in the model is shown in this table. Each metabolite can be selected by clicking on its name.

### 10: Add Metabolite Button
All names of the metabolites in the model is shown in this table. Each metabolite can be selected by clicking on its name.
