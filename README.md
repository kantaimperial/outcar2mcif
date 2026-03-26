# vasp-magtools

Small command-line tools for handling magnetic information from VASP outputs.

## Included tools

### `outcar2mcif`
Extracts site-resolved magnetic moments from VASP `OUTCAR` and writes them to a magCIF file for visualization in VESTA.

### `mag2incar`
Reads magnetic moments from a VASP `OUTCAR` file and writes them into `INCAR` as a `MAGMOM` tag.
Supports both collinear and noncollinear (`-SOC`) formats.

## Requirements

```bash
pip install pymatgen
```

## Installation

Clone the repository:

```bash
git clone git@github.com:kantaimperial/vasp-magtools.git
cd vasp-magtools
```

Make the scripts executable:

```bash
chmod +x outcar2mcif
chmod +x mag2incar
```

You can run them directly:

```bash
./outcar2mcif
./mag2incar
./mag2incar -SOC
```

Or move them into a directory in your `PATH`:

```bash
cp outcar2mcif ~/bin/
cp mag2incar ~/bin/
chmod +x ~/bin/outcar2mcif
chmod +x ~/bin/mag2incar
```

## Author

Kanta Ogawa
