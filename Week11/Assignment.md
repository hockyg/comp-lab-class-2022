# Week 11

## Using RDKIT and interfacing with psi4

## Testing out psikit

1. Using the `lab_env` environment on greene, create a jupyter notebook called `test-psikit.ipynb`
        - Add and run every step under Usage section on `https://github.com/Mishima-syk/psikit`
	- Note: replace `pk=Psikit()` with `pk=Psikit(debug=True,threads=1)`. This will have psi4 information saved to a file
	- When done, add this jupyter notebook to your git repo
	- Note, I found that the dipolemoment command doesn't work. You can see the dipole moments printed in the psi4 out file
2. Compute partial charges for CAFFEINE compare the different ways of calculating them using a Jupyter notebook
	- Download this jupyter notebook: `https://github.com/Mishima-syk/psikit/blob/master/examples/CHARGE_COMPARISON/charge_comparison.ipynb`
	- Replace the smiles string for the molecule in the notebook with that for caffeine (look it up)
	- Does the sign of the partial charges make sense to you based on chemical intuition?
	- Bonus: Label the structure of the molecule with the RESP charges (see 'include a calculation section in `https://www.rdkit.org/docs/Cookbook.html`)
	- Add this jupyter notebook to your git repo
3. Build a table/dataframe that shows some molecules and contains their quantum energies
	- Create a new jupyter notebook called `energy_table.ipynb`
	- This page has a good description of SMILES strings: `https://chemicbook.com/2021/02/13/smiles-strings-explained-for-beginners-part-1.html`
	- First, create a text file `smiles.csv` where the first line is `smiles` and the subsequent lines each contain 1 smiles string; Put the SMILES strings from the 7 molecules under **bonds** and the first three molecules under **Cyclic Structures/Ring Molecules**
	- Follow this blog post to create a dataframe from your `smiles.csv`, adding the ROMol column and n_atoms column as described in the blog post. 
	- Then, use psikit to compute the optimized energy from each molecule. (this might take some time, so it could be helpful to perform a fake calculation first to make sure things are set up right)
	- Add this energy as a column in your dataframe (look up how to add a column)
        - Have a cell at the end that shows your dataframe with the molecules and energies
	- Add this notebook to your git repo
4. Push everything to github
