# Milk Spoilage: Stochastic Modeling

This repository contains a single Jupyter notebook, **`milk_spoilage.ipynb`**, which models the spoilage of milk due to *Bacillus cereus* contamination.

The notebook uses a stochastic birth–death process implemented with the Gillespie algorithm. It explores three main scenarios:

- **Base spoilage dynamics** at a constant temperature
- **Effect of UV treatment** on shelf life
- **Impact of time-varying temperature** during transport, storage, and home use

## Requirements

- Python 3.x
- `numpy`
- `matplotlib`

Install the dependencies with:

```bash
pip install numpy matplotlib
```

## Usage

Launch Jupyter Lab or Jupyter Notebook and open `milk_spoilage.ipynb`:

```bash
jupyter lab
# or
jupyter notebook
```

Run each cell in order to reproduce the simulations and plots. You can adjust parameters such as the UV exposure time or temperature profile to explore different spoilage scenarios.

The notebook does not require any external data files; all simulations are self-contained.
