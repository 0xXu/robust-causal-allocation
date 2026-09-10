# Population residual geometry

The study compares 18 aligned, 18 transverse, and 6 common-reference configurations.
Each configuration is evaluated with 64- and 128-node Gauss-Legendre quadrature.

## Results

- Maximum computed regret over the 24 protected controls: 3.08148791102e-33.
- Transverse regret: 3.03164864451e-15 to 9.99699405716e-08; positive in all 18 configurations.
- Boundary-normalized regret: 0.999999999766 to 1.

Aligned and transverse models share their marginal residual-scale distribution,
moment envelope, and uniform Wasserstein-p radius. Their different allocation
boundaries isolate the role of residual alignment. Protected regret is analytically
zero; the computed values above retain floating-point residuals.

## Numerical checks

- Maximum nine-state pair-formula error: 4.44e-16.
- Maximum capacity-mass error: 5.55e-17.
- Maximum boundary difference between quadrature orders: 3.64e-11.
- Maximum normalized-regret difference between quadrature orders: 2.14e-14.

The common reference has zero perturbation radius, so its normalized ratios are null.
The limiting constants shown in the figures describe the large-temperature limit.

[Results](results.csv) · [Diagnostics](diagnostics.json)
