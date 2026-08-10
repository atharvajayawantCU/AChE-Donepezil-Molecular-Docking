# Molecular Docking of Donepezil with Human Acetylcholinesterase

A computational molecular docking study investigating the binding of Donepezil to human acetylcholinesterase (AChE) using AutoDock Vina and PyMOL.

## Project Overview

Donepezil is an acetylcholinesterase inhibitor used in the treatment of Alzheimer's disease. This project explores the predicted binding of Donepezil within the active-site gorge of human acetylcholinesterase using a structure-based molecular docking workflow.

The study uses the human AChE structure **4EY4** as the docking receptor and the experimental Donepezil-bound structure **4EY7** as a structural reference.

## Workflow

AChE structure (4EY4)
        ↓
Receptor preparation
        ↓
Donepezil ligand preparation
        ↓
Active-site grid definition
        ↓
AutoDock Vina docking
        ↓
Docking pose analysis
        ↓
PyMOL visualization
        ↓
Comparison with experimental structure (4EY7)

## Tools Used

- **AutoDock Vina** — molecular docking
- **Meeko** — ligand preparation and PDBQT generation
- **PyMOL** — molecular visualization and structural analysis
- **Python / Jupyter Notebook** — workflow organization and reproducibility

## Docking Parameters

| Parameter | Value |
|---|---|
| Receptor | 4EY4 |
| Ligand | Donepezil |
| Grid center X | 11.1 Å |
| Grid center Y | -53.7 Å |
| Grid center Z | 30.5 Å |
| Grid size | 20 × 20 × 20 Å |
| Exhaustiveness | 8 |
| Energy range | 4 kcal/mol |
| Number of poses | 20 |

## Results

AutoDock Vina generated 20 predicted binding poses.

The best-ranked pose (Mode 1) produced a predicted docking score of:

**−10.2 kcal/mol**

The next highest-ranked poses produced scores of:

- Mode 2: −9.9 kcal/mol
- Mode 3: −9.8 kcal/mol
- Mode 4: −9.7 kcal/mol
- Mode 5: −9.7 kcal/mol

The best-ranked Donepezil pose was located within the canonical active-site gorge of acetylcholinesterase.

### Nearby Binding-Site Residues

Residues identified around the predicted Donepezil binding pose included:

- Trp86
- Tyr124
- Glu202
- Trp286
- Ser293
- Val294
- Phe295
- Phe297
- Tyr337
- Phe338
- Tyr341
- His447
- Gly448

Several of these residues form part of the aromatic-rich environment of the AChE active-site gorge.

## Structural Comparison

The experimental Donepezil-bound AChE structure **4EY7** was used as a structural reference.

Alignment of 4EY7 chain A with the 4EY4 receptor produced a protein RMSD of:

**0.187 Å**

This indicates a highly similar overall protein conformation between the structures.

A numerical ligand RMSD between the predicted and experimental Donepezil poses was not calculated in this workflow.

## Repository Contents

AChE-Donepezil-Molecular-Docking/
│
├── README.md
├── AChE_Donepezil_Molecular_Docking.ipynb
│
└── docking/
    └── vina_config.txt

## Reproducibility

The Jupyter notebook contains the computational docking workflow, while `docking/vina_config.txt` contains the parameters used for the reported docking run.

The reported docking score is a **computational prediction from AutoDock Vina** and should not be interpreted as an experimentally measured binding affinity.

## Limitations

Molecular docking provides a computational prediction of ligand binding pose and scoring rather than a direct measurement of experimental binding affinity. The results should therefore be interpreted as structural and computational predictions.

Further validation could include molecular dynamics simulations, rescoring, experimental binding assays, or comparison across additional AChE inhibitors.

## Future Work

Potential extensions of this project include:

- Molecular dynamics simulations of the AChE–Donepezil complex
- Virtual screening of additional acetylcholinesterase inhibitors
- Comparative docking of related ligands
- Binding free-energy estimation
- Analysis of ligand–residue interaction fingerprints

## Author

**Atharva Jayawant**

BSc Biotechnology  
Christ University, Bangalore
