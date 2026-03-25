# outcar2mcif

Extracts site-resolved magnetic moments from VASP `OUTCAR` and writes them to a magCIF file for visualization in VESTA.

## Overview

`outcar2mcif` is a simple command-line tool that converts VASP output files into a format suitable for visualizing magnetic structures.

It reads:

- `OUTCAR` (magnetic moments)
- `CONTCAR` (atomic structure)

and generates:

- `magmom_visualization.mcif`

which can be directly opened in VESTA.

## Installation

Clone the repository and move into the project directory:

```bash
git clone https://github.com/kantaimperial/outcar2mcif.git
cd outcar2mcif
```

Next, install the required Python package:

```bash
pip install pymatgen
```

Then, make the script executable:

```bash
chmod +x outcar2mcif
```

You can run the script directly from the repository directory:

```bash
./outcar2mcif
```

If you would like to use `outcar2mcif` as a command from any directory, move it to a directory in your `PATH`:

```bash
mv outcar2mcif ~/bin/
```

If `~/bin` is not already included in your `PATH`, add it with:

```bash
export PATH="$HOME/bin:$PATH"
```

Then reload your shell configuration:

```bash
source ~/.bashrc
```

After that, you can run:

```bash
outcar2mcif
```

## Usage

Run the script in a directory containing `OUTCAR` and `CONTCAR`:

```bash
outcar2mcif
```

## Output

The script generates:

```text
magmom_visualization.mcif
```

Open this file in VESTA to visualize magnetic moments.

## Features

- Extracts magnetic moments from VASP `OUTCAR`
- Supports collinear spin calculations
- Automatically maps magnetic moments to atomic positions
- Outputs magCIF format compatible with VESTA

## Notes

- Magnetic moments are written along the z-axis for collinear calculations
- Ensure that `OUTCAR` and `CONTCAR` correspond to the same calculation
- The script uses the final ionic step in `OUTCAR`

## Author

Kanta Ogawa
