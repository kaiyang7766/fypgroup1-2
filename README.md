# FYP Group 1.2: Nucleophilicity prediction of ketones

This neural network is trained with data of 726 molecules from the Mayr's database.

The infrastructure of the model:  
a) 400 x 400 neurons  
b) Adam optimizer  
c) Learning rate 0.001  
d) 100,000 learning steps  
e) Dropout rate 0.8  
f) L2 regularization 0.001  

## How to run the file
Input file should be in the format of:
(Name) (SMILES) (Adiabatic I.E.) (Parr function, sorted in descending order)  

Name -- Name of the molecule SMILES -- SMILES expression of molecular structure Adiabatic I.E. -- Ionization energy calculated from fully relaxed (n-1) electron structure Parr function -- Spin density of fully relaxed (n-1) electron structure, sorted in descending order. ~30 Parr function values can be provided. write down to the 30th value if the number of atom in molecule is larger than 30.

An example of input file "ketones_input"is included in this Github repo.

This model is not limited to ketones, but suitable for all molecules in general.

## Acknowledgement
The infrastructure and training of model is adapted from the paper: [Predicting the chemical reactivity of organic materials using a machine-learning approach](https://pubs.rsc.org/en/content/articlehtml/2020/sc/d0sc01328e)
