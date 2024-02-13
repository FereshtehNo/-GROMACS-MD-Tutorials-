                                                🔬💻 GROMACS Simulation: Running 10 ns Molecular Dynamics for Metalloprotein with 4 Copper Ions (No Ligands)

🔍 **Step 1:** Save only Cu ions in a PDB file.
     gmx editconf -f cu.pdb -o cu.gro
     gmx genrestr -f cu.gro -o posre-cu.itp

