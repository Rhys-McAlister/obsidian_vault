## Initial molecular geometries

RDKit and Chemcoord were used to generate initial molecular geometries for all molecules in the dataset using their SMILES codes. This algorithm takes the smiles identifier and then performs a crude geometry optimisation using molecular mechanics (i.e A Merck molecular force field) to output an initial geometry.

## Cheap Geometry Optimisation

Taking the initial geometry values we obtained from the SMILES strings, a 'cheap' geometry optimisation is performed using the GFN2-xTB semi-empirical method that yields a more appropriate geometry starting point prior to the following conformal search and quantum chemistry calculations that will follow. The GFN2-xTB method is appropriate for conducting fast calculation of chemical structures.