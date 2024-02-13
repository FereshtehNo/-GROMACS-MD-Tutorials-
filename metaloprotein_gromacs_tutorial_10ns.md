🔬💻 GROMACS Simulation: Running 10 ns Molecular Dynamics for Metalloprotein with 4 Copper Ions (No Ligands)

🔧 **Step 1:** Save only Cu ions in a PDB file and generate position restraints.

- Run `gmx editconf -f cu.pdb -o cu.gro`.
- Run `gmx genrestr -f cu.gro -o posre-cu.itp`.

🔧 **Step 2:** Open your protein PDB without any ions and delete hydrogens.

🔧 **Step 3:** Process the protein PDB file to generate a GROMACS coordinate file with the SPC water model.

 - Run `gmx pdb2gmx -f protein.pdb -o protein.gro -water spc`.

🔧 **Step 4:** Add copper ions coordinates to the topology file.

![Cooper Ions Coordinate Topology File](cooperions_coordinate_topology_file.jpg)

*It's an example. Make sure to change the ID based on your work.*
 
🔧  **Step 5:**  Merge the GRO file of copper ions with the GRO file of the protein, and adjust the atom numbers.









