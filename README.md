# TIM-Barrels_AverageStructureCalculation

This project was developed for Algorithms in Structural Bioinformatics course - MSc in Data Science and Information Technologies, Departement of Informatics and Telecommunications, National & Kapodistrian Uneversity of Athens.

# Project's goal

The main goal of this project was to construct a pipeline that calculates the coordinates of the average structure of a specific protein family - we chose the TIM-Barrel enzymatic family.

# Workflow

<img width="858" alt="Screenshot 2022-08-08 at 4 19 57 PM" src="https://user-images.githubusercontent.com/110672874/183428090-b212eb48-f9f0-43e9-85a1-f860e868fd11.png">

# Jupyter Notebooks

Below you can find a sort description of the Jupyter Notebooks that we developed during the project.
These were applied both on the IC (Isomerase Classification) and NIC (No Isomerase Classification) protein datasets.

- **pdbe_fold_input_file.ipynb**:
The pdbe_fold_input_file.ipynb file takes as input a text file containing the PDB IDs separated by comma and returns a text file
in the appropriate format (PDB ID: chain), to use it as input to PDBeFold and perform multiple structure alignment

- **superposed_structure.ipynb**:
The superposed_structure.ipynb file iterates through a folder containing the PDB files of all proteins used for the analysis.
After each iteration it takes as input the corresponding PDB file and the output file of the PDBeFold that contains the rotation
and translation matrices and calculates the superposed coordinates for each protein. Then it stores the coordinates along with the
protein's PDB ID in a text file. So, as output it produces a text file including the superposed coordinates and the protein IDs 
(superposed_coordinates.txt).

- **average_structure.ipynb**:
The average_structure.ipynb file takes as input the PDBeFold fasta output file that contains the multiple alignment and the text
file produced by the superposed_structure.ipynb and calculates the coordinates of the mean structure. The coordinates are the stores
in a text file as output (average_structure_coordinates.txt).

- **write_pdb_file.ipynb**:
The write_pdb_file.ipynb script takes as input the average_structure_coordinates.txt and creates a PDB - like file containing the 
coordinates of the mean structure to be used as input in ChimeraX for visualization purposes. 

# Output

<img width="485" alt="Screenshot 2022-08-08 at 4 46 34 PM" src="https://user-images.githubusercontent.com/110672874/183433095-c4ac7772-f875-43a7-83cb-ce38ab7b8776.png">

For analytic explanation of each pipeline's step please have a look at README.pdf, which is uploaded at the repository. 
