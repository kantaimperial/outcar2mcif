# outcar2mcif

Extracts site-resolved magnetic moments from VASP OUTCAR and writes them to a magCIF file for visualization in VESTA.

## Overview

`outcar2mcif` is a simple command-line tool to convert VASP output files into a format suitable for visualizing magnetic structures.

It reads:

- `OUTCAR` (magnetic moments)
- `CONTCAR` (atomic structure)

and generates:

- `magmom_visualization.mcif`

which can be directly opened in VESTA.

---

## Installation

Install the required Python package:

```bash
pip install pymatgen
