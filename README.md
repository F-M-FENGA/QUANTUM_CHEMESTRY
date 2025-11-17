```markdown
# Quantum Chemistry 

Summary
-------
This folder contains the code and notebooks associated with a Master's project in quantum chemistry. It gathers geometry optimizations, ORCA input/output handling, variational quantum algorithms for excited states (SSVQE, QEOM), and scripts/notebooks for generating plots and figures used in the report.

Repository structure
--------------------
- Quantum Chemistry.ipynb
  - Main notebook (exploration, analyses, and figures). Likely contains cells to run experiments, show results, and produce plots.
- Geometry_optimisation/
  - Scripts and input/output files for geometry optimization (may include ORCA input files, parsers, and optimized geometries).
- Orca_calculation/
  - ORCA input (.inp) and output (.out) files, plus automation and parsing scripts used to run and analyze ORCA calculations (energies, frequencies, orbitals).
- SSVQE/
  - Implementation and scripts for SSVQE (subspace-search VQE): state preparation, variational circuits, cost functions, training loops, and result saving.
- QEOM/
  - Scripts and tools for QEOM (Quantum Equation-of-Motion): computing excited states from a VQE/SSVQE reference, analyzing excitation matrices, energies, and transitions.
- Curves and Plots/
  - Scripts and notebooks to generate all figures for the report: energy curves, convergence plots, densities, and orbital diagrams.

Prerequisites
-------------
- Platform: Linux / macOS (Windows via WSL is possible).
- Python 3.8+ (matching the environment used in the project).
- Recommended environment manager: conda (miniconda/anaconda) or Python venv.
- Typical Python packages:
  - numpy, scipy, pandas, matplotlib, seaborn, jupyter, jupyterlab
  - qiskit or other quantum SDK used in the project (Pennylane)
  - pyscf (if classical quantum chemistry routines are used)
  - any ORCA parsing utilities used in the repo
- ORCA (if you intend to rerun ORCA calculations):
  - ORCA installed and available on PATH
  - ORCA license as required

Installation (example using conda)
---------------------------------
1) Create and activate a conda environment:
   conda create -n qc-env python=3.9 -y
   conda activate qc-env

2) Install Python dependencies (example):
   pip install numpy scipy pandas matplotlib seaborn jupyterlab qiskit pyscf

3) Optionally install ORCA and ensure the `orca` executable is in PATH.

Usage
-----
- Notebook:
  - Launch Jupyter and open `Quantum Chemistry.ipynb`:
    jupyter lab
  - Execute cells in order or follow the instructions inside the notebook.

- ORCA calculations:
  - Place ORCA input files (.inp) in `Orca_calculation/` and run:
    orca mycalc.inp > mycalc.out
  - Use parsing scripts in `Orca_calculation/` to extract energies and frequencies.

- Geometry optimization:
  - Run optimization scripts in `Geometry_optimisation/`. If ORCA inputs are provided, run them as shown above.

- SSVQE / QEOM:
  - Check the scripts and notebooks in `SSVQE/` and `QEOM/`.
  - Run training scripts to produce result files (e.g., .npz, .json, .csv) and checkpoints.

## Author

F. M. FENGA  
Master 2, Atomic, Molecular, and Biophysics Physics  
University of Yaoundé I  
franklin.fenga@facsciences-uy1.cm ```

---
