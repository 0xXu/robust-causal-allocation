# Data dictionary

This dataset contains the complete retained numerical results for the three studies in *Robust Causal Allocation: Residual Geometry, Ranking Calibration and Statistical Limits*. It includes population calculations, replicate-level method results, summaries, and numerical diagnostics. Individual simulated covariate, treatment, and outcome records are not included.

All values use the studies' synthetic outcome scale. `regret` is population welfare loss relative to the optimal allocation at the stated capacity; lower values are better. Regrets are stored without rescaling, including in the branch study, whose manuscript tables display values in units of 10^-4. `mcse` denotes the Monte Carlo standard error of a reported mean. JSON `null` and empty CSV cells denote quantities that are undefined or inapplicable, rather than zero.

## `results/effect_alignment_geometry_population/`

A deterministic study of 42 configurations: 18 aligned, 18 transverse, and 6 common-reference controls. There are no random seeds or Monte Carlo replicates.

| File | Contents |
|---|---|
| `configurations.json` | The 42 parameter settings. |
| `results.csv`, `results.json` | Equivalent final results, one row per configuration, using 128 quadrature nodes. |
| `boundaries.csv`, `boundaries.json` | Equivalent allocation-boundary coordinates: 65 points per configuration. |
| `quadrature_results.csv` | Results at both 64 and 128 quadrature nodes. |
| `quadrature_comparison.csv` | Differences between the two quadrature resolutions. |
| `branch_checks.csv`, `pair_checks.csv`, `score_checks.csv` | Clipping margins, direct pair-formula comparisons, and integrated-score comparisons. |
| `diagnostics.json` | Aggregate numerical errors and result ranges. |

`config_id` joins these files. `control` is `aligned`, `transverse`, or `common`; `delta=p-1`; `K` is comparison temperature. `epsilon` is the clipping level, `M` the conditional p-moment envelope, and `A`, `c`, `u0`, and `h0` the construction constants. `radius_fraction` is eta/eta0, `eta` is the Wasserstein-p radius, `h` is the scale perturbation, and `omega` is the rare-state parameter. `w` and `d` are the score coefficients, with `a=d/w`.

`capacity_threshold` is the fitted score cutoff and `capacity_mass` its treated population fraction, targeting 0.5. `z` is the transverse coordinate, `boundary` the effect cutoff at that coordinate, and `dimensionless_boundary` its value divided by `a` when `a` is nonzero (stored as zero for the common reference). `normalized_regret` is 12 w² regret/d²; `radius_temperature_normalized_regret` is regret/(eta² K^(-2 delta)); `limiting_constant` is the latter ratio's large-temperature limit. The two normalized regret ratios for the common reference are undefined. Check files report absolute errors or branch margins in the corresponding score/label scale.

## `results/temperature_finite_sample/`

Twelve sampling cells combine six `base_n` values (64 through 65,536) with `balanced` and `unbalanced` designs. Each cell has 1,000 seed-indexed replicates and five methods.

- `config.json` records the group model, clipping level, temperature schedules, sample sizes, and seeds.
- `results.jsonl` contains 60,000 records: one method result per sampling cell and seed.
- `exact.jsonl` contains 60 analytical method-cell records, with population scores and variance components.
- `summary.json` contains aggregate counts and a `cells` array with means, Monte Carlo standard errors, and analytical comparisons.

`group_sizes` equals `[base_n, base_n, base_n]` or `[base_n, 2 base_n, 4 base_n]`; target population masses remain equal. Three-element arrays follow high-, middle-, and low-effect group order. `method` identifies the procedure; `kappa` is its temperature and is null for `empirical_dr`. `scaled_scores` are centered allocation scores, `score_errors` subtract the centered true effects, and `squared_score_error` is their target-mass-weighted squared error. `capacity_allocation` gives within-group treatment fractions; `correct_allocation` identifies selection of the optimal group. `high_middle_pair_statistic` is the empirical high–middle pair comparison.

`population` in the analytical files contains the corresponding population quantities and pairwise variance components. `variance` separates the two first-order projection terms and the degenerate term; their sum is `exact_variance`. `incorrect_independent_pair_variance` is the comparison calculation that treats reused pairs as independent. Variances and squared errors have squared score units; variance ratios are dimensionless.

Seeds 12000–12999 identify replicates. Random streams additionally depend on sampling-design index and `base_n`, so the same seed label across different cells does not denote the same dataset. Within each cell and seed, all five methods share the same simulated group counts.

## `results/branch_stability_confirmation_v1/`

The study combines `n` in {512, 2048, 8192}, five `rho` values from 0 to 1, and 200 replicates per cell. Seven methods yield **21,000 method records from 3,000 dataset configurations and 600 independent seed groups**.

- `config.json` records the design, methods, moment order, Pareto shape, and base seed.
- `results.jsonl` has one record per `(n, rho, replicate, method)`.
- `summary.json` has 105 method-cell rows with `mean`, `mcse`, `median`, and `replicates` for regret.
- `paired-differences.json` has 90 contrasts against `Compensated`: `mean_difference` follows the order named in `contrast`; `low` and `high` are paired 95% t-interval endpoints for that mean difference.
- `completion.json` records totals and solver diagnostics.

`n` is the total training sample size; `rho` controls treatment-branch variation while the mixed residual law stays fixed. `replicate` ranges from 0 to 199. `direction` is the two-coordinate allocation vector before normalization; `direction_error` is its normalized vector's squared Euclidean distance from the normalized true direction (0.8, 0.2). `solver` holds optimization diagnostics and is empty for methods without iterative fits. `PairHuber1`/`PairHuber4` use disjoint same-arm differences; `ArmHuber1`/`ArmHuber4` use ordinary armwise fits with intercepts. Their suffixes identify Huber thresholds.

Each independent stream is indexed by base seed 20260910, `n`, and `replicate`. The five `rho` settings share latent draws within that group, and all methods share each realized dataset. Thus the 3,000 configurations are grouped into 600 independent units; comparisons across `rho` or methods retain this pairing.
