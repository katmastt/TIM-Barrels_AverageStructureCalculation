#########################################################
##            Implementation of the project            ##
##                                                     ##
#########################################################

Below you can find a sort description of the Jupyter Notebooks that were developed during the project.
These were applied both on the IC (Isomerase Classification) and NIC (No Isomerase Classification) protein datasets.
------------------------------------------------------------------------------------------------------------------------

1. pdbe_fold_input_file.ipynb
The pdbe_fold_input_file.ipynb file takes as input a text file containing the PDB IDs separated by comma and returns a text file
in the appropriate format (PDB ID: chain), to use it as input to PDBeFold and perform multiple structure alignment

2. superposed_structure.ipynb
The superposed_structure.ipynb file iterates through a folder containing the PDB files of all proteins used for the analysis.
After each iteration it takes as input the corresponding PDB file and the output file of the PDBeFold that contains the rotation
and translation matrices and calculates the superposed coordinates for each protein. Then it stores the coordinates along with the
protein's PDB ID in a text file. So, as output it produces a text file including the superposed coordinates and the protein IDs 
(superposed_coordinates.txt).

3. average_structure.ipynb
The average_structure.ipynb file takes as input the PDBeFold fasta output file that contains the multiple alignment and the text
file produced by the superposed_structure.ipynb and calculates the coordinates of the mean structure. The coordinates are the stores
in a text file as output (average_structure_coordinates.txt).

4. write_pdb_file.ipynb
The write_pdb_file.ipynb script takes as input the average_structure_coordinates.txt and creates a PDB - like file containing the 
coordinates of the mean structure to be used as input in ChimeraX for visualization purposes.
--------------------------------------------------------------------------------------------------------------------------


