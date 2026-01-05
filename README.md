# MTH5 Tutorial

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MTgeophysics/mth5_tutorial/main)

A collection of Jupyter notebooks demonstrating how to use the **mth5** package to create, manipulate, and analyze MTH5 files from various magnetotelluric (MT) instruments.

## Quick Start with Binder

Click the "launch binder" badge above to run these tutorials in your browser without installing anything! Binder will create a live Jupyter environment with all dependencies pre-installed.

## About MTH5

**MTH5** is a Python package for working with magnetotelluric (MT) time series data in the HDF5 format. It provides a structured, standardized way to store, access, and manage MT data along with comprehensive metadata following IRIS-PASSCAL MT metadata standards.

### What is an MTH5 File?

An **MTH5 file** is an HDF5-based container format specifically designed for magnetotelluric time series data. Key features include:

- **Hierarchical Structure**: Organizes data by Survey → Station → Run → Channel
- **Standardized Metadata**: Follows community-established metadata standards for MT data
- **Efficient Storage**: Leverages HDF5's compression and chunking for large datasets
- **Self-Describing**: All metadata is stored within the file itself
- **Interoperable**: Compatible with other MT analysis tools and workflows
- **Version Controlled**: Supports schema versioning for data format evolution

MTH5 files are ideal for archiving MT time series data, facilitating data sharing, and ensuring long-term data preservation with complete provenance.

## Repository Contents

This repository contains tutorial notebooks demonstrating how to:

### Create MTH5 Files from Different Instruments

- **Phoenix Systems**
  - `make_mth5_from_phoenix_legacy_mtu.ipynb` - Legacy MTU format
  - `make_mth5_from_phoenix_real.ipynb` - Phoenix .td_* format
  
- **Zonge Systems**
  - `make_mth5_from_z3d.ipynb` - Z3D format data
  
- **NIMS Systems**
  - `make_mth5_from_nims.ipynb` - NIMS format data

- **LEMI Systems**
  - `make_mth5_from_lemi.ipynb` - LEMI format data

- **Metronix Systems**
  - `make_mth5_from_metronix.ipynb` - Metronix format data

- **Geomag Systems**
  - `make_mth5_from_geomag.ipynb` - Geomagnetic data

### Work with MTH5 Files

- `make_mth5_driver_v0.1.0.ipynb` - Working with MTH5 v0.1.0 format
- `make_mth5_driver_v0.2.0.ipynb` - Working with MTH5 v0.2.0 format
- `run_ts_example.ipynb` - Working with time series data
- `transfer_function_example.ipynb` - Working with transfer functions
- `remove_instrument_response_example.ipynb` - Instrument response correction

### Advanced Topics

- `mth5_in_parallel.ipynb` - Parallel processing of MTH5 files
- `mth5_in_parallel_one_file_per_station.ipynb` - Multi-file parallel workflows

## Installation

### Using pip

```bash
pip install mth5
```

### Using conda

```bash
conda install -c conda-forge mth5
```

### From source

```bash
git clone https://github.com/kujaku11/mth5.git
cd mth5
pip install -e .
```

## Requirements

- Python 3.8+
- h5py
- numpy
- xarray
- mt-metadata
- pandas

All dependencies are automatically installed with the mth5 package.

## Getting Started

### Option 1: Run in the Cloud (No Installation Required)

Click the Binder badge at the top of this README to launch an interactive environment in your browser. This is the easiest way to try the tutorials without installing anything locally.

### Option 2: Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/kujaku11/mth5_tutorial.git
   cd mth5_tutorial
   ```

2. Install mth5 and Jupyter:
   ```bash
   pip install mth5 jupyter
   ```

3. Launch Jupyter:
   ```bash
   jupyter notebook src/notebooks/
   ```

4. Open any notebook and follow along with the examples.

## Documentation

- **MTH5 Documentation**: https://mth5.readthedocs.io
- **MT Metadata Standards**: https://doi.org/10.5066/P9AXGKEV
- **GitHub Repository**: https://github.com/kujaku11/mth5

## Contributing

Contributions are welcome! If you have examples or tutorials you'd like to share:

1. Fork the repository
2. Create a new branch for your notebook
3. Add your notebook with clear documentation
4. Submit a pull request

## Support

For questions or issues:

- Open an issue on [GitHub](https://github.com/kujaku11/mth5/issues)
- Consult the [documentation](https://mth5.readthedocs.io)

## License

This tutorial repository follows the same license as the mth5 package. See LICENSE file for details.

## Citation

If you use mth5 in your research, please cite:

> Peacock, J.R., Kappler, K., Ronan, T., Heagy, L., Kelbert, A., Frassetto, A., 2022, MTH5: An HDF5 data container for magnetotelluric time series data: U.S. Geological Survey software release, https://doi.org/10.5066/P9FQQARB

