# Stochastic Modeling of Milk Spoilage

This project models the stochastic growth of **Bacillus cereus** in milk and estimates spoilage times under different environmental conditions.

The model is implemented using a **continuous-time birth–death process** and simulated with the **Gillespie stochastic simulation algorithm (SSA)**. The objective is to analyze how microbial growth uncertainty affects shelf-life predictions and how interventions or temperature fluctuations influence spoilage risk.

All simulations are implemented in a single Jupyter notebook: `milk_spoilage.ipynb`.

---

## Model Overview

The bacterial population is modeled as a **continuous-time Markov process** where:

- Birth events represent bacterial reproduction
- Death events represent bacterial decay
- Spoilage occurs when the population reaches a predefined threshold

The simulation estimates the **first-hitting time distribution** for spoilage events using Monte Carlo sampling.

The notebook explores three primary scenarios:

### 1. Baseline Spoilage Dynamics

Simulates bacterial growth at a constant temperature using the Gillespie algorithm and computes:

- Empirical spoilage-time distributions
- Mean and median shelf-life
- Risk-sensitive quantiles (e.g., 5% spoilage probability)

### 2. UV Treatment Intervention

Evaluates the effect of a UV sterilization shock that removes a large fraction of bacteria at a chosen time point.

The simulation identifies the **optimal intervention time** that maximizes shelf-life extension.

### 3. Temperature-Dependent Growth

Extends the model to incorporate **time-varying temperature profiles** representing:

- Transport
- Retail storage
- Home refrigeration

This demonstrates how short periods of elevated temperature can significantly reduce effective shelf life.

---

## Methods Used

Key techniques used in this project:

- Continuous-time Markov chains
- Birth–death stochastic processes
- Gillespie stochastic simulation algorithm
- Monte Carlo simulation
- First-hitting time analysis
- Empirical CDF estimation

---

## Requirements

Python 3.x

Install dependencies:

```bash
pip install numpy matplotlib

## Usage

Launch Jupyter Lab or Jupyter Notebook and open `milk_spoilage.ipynb`:

```bash
jupyter lab
# or
jupyter notebook
```

Run each cell in order to reproduce the simulations and plots. You can adjust parameters such as the UV exposure time or temperature profile to explore different spoilage scenarios.

The notebook does not require any external data files; all simulations are self-contained.
