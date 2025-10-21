# VPT Segmentation Packing

A package for packing and processing VPT (Vizgen Post-processing Tool) segmentation data.

## Background

This package was created because the original Vizgen package is private and cannot be updated by external contributors. This fork provides the necessary functionality for packing segmentation data into the vzg2 format used by Vizgen's visualization tools.

## Features

- **Cell Preprocessing**: Transform and prepare cell polygon data for visualization
- **Cell Packing**: Pack cell data into vzg2 format with multiple LOD (Level of Detail) levels
- **Assembly**: Create vzg2 archives from structured directories
- **Unpacking**: Load and extract data from vzg2 files

## Installation

### From Git Repository

```bash
pip install git+https://github.com/imcf/vpt-segmentation-packing.git@imcf-dev
```

### With Poetry

```bash
poetry add git+https://github.com/imcf/vpt-segmentation-packing.git@imcf-dev
```

### Local Development

```bash
git clone https://github.com/imcf/vpt-segmentation-packing.git
cd vpt-segmentation-packing
poetry install
```

## Usage

```python
from vpt_segmentation_packing import pack_cells, preprocess_cells, assemble_vzg2
from vpt_segmentation_packing import load_polygons, load_lod

# Preprocess cells
poly_list = preprocess_cells(...)

# Pack cells into vzg2 format
pack_cells(poly_list, cells_dir, ...)

# Assemble vzg2 file
assemble_vzg2(input_dir, output_path)

# Load data from vzg2
polygons = load_polygons(...)
lod_data = load_lod(...)
```

## Requirements

- Python ≥ 3.9
- numpy ≥ 1.20.0
- pandas ≥ 1.3.0
- shapely ≥ 1.8.0
- pyarrow ≥ 6.0.0

## License

MIT

## Contributing

Contributions are welcome! Since the original Vizgen package is private, this repository serves as an open alternative for the community.
