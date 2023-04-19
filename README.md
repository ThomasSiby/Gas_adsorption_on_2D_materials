#### Siby Thomas, Felix Mayr, Ajith Kulangara Madam and Alessio Gagliardi. Machine learning and DFT investigation of CO, CO2 and CH4 adsorption on pristine and defective two-dimensional magnesene. 

### What is in here:
- notebooks to load the structure files (found in data) and match them to the table including the features from `Mg_data_for_ML.fixed.xlsx` (`convert-vasp.ipynb`). In the 'Mg_data_for_ML.fixed.xlsx file', \

	(a) the DFT computed properties are:
	E_ads: DFT computed adsoprtion energy
	TE: DFT computed total energy
	E_per_atom: dft computed total energy per atom
	a_alat: lattice constant of the 2D-Mg supercell along the a direction
	b_lat: lattice constnat of the 2D-Mg supercell along the b direction
	AN: Atomic number of elements 

	(b) the features (statistical) for ML analysis are:
	MN: Mass number of elemnets
	GN: group number of elements
	PN: Periodic number of the elements
	Elec_neg: Electronegativity of the elements
	At_radii: Atomic radius of the elements
	vdWR: van der Waal;s radius of the elements
	cov_rad: Covalent radius of the elements
	ion_rad: Ionic radius of the elements
	density: density of the elements

- notebooks to reproduce the cross-validated models shown in the paper Phys. Chem. Chem. Phys., 2023 (https://doi.org/10.1039/D3CP00613A). Both with the statistical fingerprints described in the paper (`simple_ml.ipynb`), as well as SOAP (`soapy_ml.ipynb`). Fitting and plotting functionality is provided by the module `sklearn_utils.py`.

- some experiments with models from the Open-Catalyst-Project to check whether those models could be used as an off-the-shelf surrogate for our problem or at least provide meaningful 
  correlation to the data collected in the experiment. `relax_ocp.ipynb`

### What do yo need to run
This code was run in a standard-datascience-environment (numpy, pandas, sklearn, matplotlib) and should not have special dependencies. 
If we use those, we install them to your current env in the first cell of each notebook.
