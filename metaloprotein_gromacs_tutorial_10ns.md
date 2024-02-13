 🔬💻 GROMACS Simulation: Running 10 ns Molecular Dynamics for Metalloprotein with 4 Copper Ions (No Ligands)

🔍 **Step 1:** Save only Cu ions in a PDB file and generate position restraints.

- Run `gmx editconf -f cu.pdb -o cu.gro`.
- Run `gmx genrestr -f cu.gro -o posre-cu.itp`.

🔧 Step 2: Open your protein PDB without any ions and delete hydrogens.

🔧 Step 3: Process the protein PDB file to generate a GROMACS coordinate file with the SPC water model.

 - Run `gmx pdb2gmx -f protein.pdb -o protein.gro -water spc`.

 🔧 Step 4: Add copper ions coordinates to the topology file.

   ; id
3585  CU2+  358  CU2+  CU  1546  2  63.5460  ; qtot 4
; id
3586  CU2+  359  CU2+  CU  1547  2  63.5460  ; qtot 6
; id
3587  CU2+  360  CU2+  CU  1548  2  63.5460  ; qtot 8
; id
3588  CU2+  361  CU2+  CU  1549  2  63.5460  ; qtot 10

   This is an example. Adjust the IDs based on your work.



