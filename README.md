# Robust Causal Allocation: Synthetic Experimental Results

Numerical results for **Robust Causal Allocation: Residual Geometry, Ranking Calibration and Statistical Limits**.

All three studies use synthetic data. This dataset contains their retained numerical outputs, experiment parameters, random seed definitions, and statistical summaries.

## Data

| Directory | Study | Contents |
| --- | --- | --- |
| `results/effect_alignment_geometry_population/` | Population residual geometry | 42 deterministic configurations, allocation boundaries, regret and quadrature diagnostics |
| `results/temperature_finite_sample/` | Finite-group sampling | 12 configurations, 1,000 replications each, five methods; 60,000 method-level records and 60 exact targets |
| `results/branch_stability_confirmation_v1/` | Branch stability | 15 configurations, 200 replications each, seven methods; 21,000 method-level records from 600 independent seed groups |

CSV files contain headers. JSONL files contain one JSON record per line. Each study includes a Markdown summary, with parameters and additional results in JSON files. See [DATA_DICTIONARY.md](DATA_DICTIONARY.md) for field definitions and the seed structure.

The stochastic studies retain method-level outputs and summaries. Individual simulated observations are not included. Reported Monte Carlo standard errors measure variation across replications within each configuration.

## Citation

*Robust Causal Allocation: Synthetic Experimental Results*. GitHub. https://github.com/0xXu/robust-causal-allocation
