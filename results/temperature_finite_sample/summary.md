# Finite-group sampling results

The experiment uses 12 sampling cells, 1,000 replications per cell, and five methods. Nuisance functions and equal target masses are known. The growing-temperature schedule uses the oracle moment scale. Methods share the same residual counts within each sampling cell.

Regret is lost population treatment value at capacity 1/3. Squared score error is the target-mass-weighted squared difference from centered CATE. Parentheses contain seed-level Monte Carlo standard errors; correct allocation is a fraction.

| Sampling | Base n | Method | Kappa | Mean regret (MCSE) | Mean squared score error (MCSE) | Correct allocation (MCSE) |
|---|---:|---|---:|---:|---:|---:|
| balanced | 64 | kappa_1 | 1 | 0.0096833333 (0.000260172) | 0.031975417 (0.000660307) | 0.419 (0.0156103) |
| balanced | 64 | kappa_2 | 2 | 0.0073166667 (0.000261686) | 0.019303572 (0.000657069) | 0.561 (0.0157011) |
| balanced | 64 | kappa_16 | 16 | 0.012033333 (0.00120715) | 0.087506858 (0.00343843) | 0.518 (0.015809) |
| balanced | 64 | theorem_schedule | 36.746702 | 0.044716667 (0.00335265) | 0.37972915 (0.0160586) | 0.457 (0.0157607) |
| balanced | 64 | empirical_dr | linear DR | 0.0641 (0.00399902) | 0.6904326 (0.0295163) | 0.414 (0.0155835) |
| balanced | 256 | kappa_1 | 1 | 0.010183333 (0.000257076) | 0.025026176 (0.000302193) | 0.389 (0.0154246) |
| balanced | 256 | kappa_2 | 2 | 0.0057 (0.000250145) | 0.0052076808 (0.000171792) | 0.658 (0.0150087) |
| balanced | 256 | kappa_16 | 16 | 0.00665 (0.00025822) | 0.022764892 (0.0007904) | 0.601 (0.0154932) |
| balanced | 256 | theorem_schedule | 73.493405 | 0.019583333 (0.00200755) | 0.18095717 (0.00691742) | 0.525 (0.0157995) |
| balanced | 256 | empirical_dr | linear DR | 0.019933333 (0.00203446) | 0.18143651 (0.00694163) | 0.524 (0.0158011) |
| balanced | 1024 | kappa_1 | 1 | 0.012733333 (0.000223908) | 0.023975331 (0.000153371) | 0.236 (0.0134345) |
| balanced | 1024 | kappa_2 | 2 | 0.0038166667 (0.00022157) | 0.0015942419 (5.04901e-05) | 0.771 (0.0132942) |
| balanced | 1024 | kappa_16 | 16 | 0.0058166667 (0.000251344) | 0.0058844833 (0.000193006) | 0.651 (0.0150807) |
| balanced | 1024 | theorem_schedule | 146.98681 | 0.0081333333 (0.000431575) | 0.044580694 (0.00153452) | 0.532 (0.0157869) |
| balanced | 1024 | empirical_dr | linear DR | 0.0081333333 (0.000431575) | 0.04458146 (0.00153455) | 0.532 (0.0157869) |
| balanced | 4096 | kappa_1 | 1 | 0.015033333 (0.000156777) | 0.023474391 (7.73339e-05) | 0.098 (0.00940662) |
| balanced | 4096 | kappa_2 | 2 | 0.0011833333 (0.000135426) | 0.00064703564 (1.70331e-05) | 0.929 (0.00812558) |
| balanced | 4096 | kappa_16 | 16 | 0.0033833333 (0.000212101) | 0.0014771865 (4.7804e-05) | 0.797 (0.0127261) |
| balanced | 4096 | theorem_schedule | 293.97362 | 0.0062833333 (0.000255553) | 0.010555734 (0.000343395) | 0.623 (0.0153332) |
| balanced | 4096 | empirical_dr | linear DR | 0.0062833333 (0.000255553) | 0.010555777 (0.000343396) | 0.623 (0.0153332) |
| balanced | 16384 | kappa_1 | 1 | 0.0165 (5.24667e-05) | 0.023287044 (3.80359e-05) | 0.01 (0.003148) |
| balanced | 16384 | kappa_2 | 2 | 1.6666667e-05 (1.66667e-05) | 0.00037695267 (6.5392e-06) | 0.999 (0.001) |
| balanced | 16384 | kappa_16 | 16 | 0.00053333333 (9.28066e-05) | 0.00040686329 (1.28095e-05) | 0.968 (0.00556839) |
| balanced | 16384 | theorem_schedule | 587.94724 | 0.0045 (0.000234104) | 0.0026541979 (8.71383e-05) | 0.73 (0.0140463) |
| balanced | 16384 | empirical_dr | linear DR | 0.0045 (0.000234104) | 0.0026542004 (8.71384e-05) | 0.73 (0.0140463) |
| balanced | 65536 | kappa_1 | 1 | 0.016666667 (0) | 0.023250925 (1.84593e-05) | 0 (0) |
| balanced | 65536 | kappa_2 | 2 | 0 (0) | 0.00031466995 (2.90901e-06) | 1 (0) |
| balanced | 65536 | kappa_16 | 16 | 0 (0) | 0.00013930864 (4.42095e-06) | 1 (0) |
| balanced | 65536 | theorem_schedule | 1175.8945 | 0.0017 (0.000159589) | 0.00071594945 (2.65118e-05) | 0.898 (0.00957537) |
| balanced | 65536 | empirical_dr | linear DR | 0.0017 (0.000159589) | 0.00071594971 (2.65119e-05) | 0.898 (0.00957537) |
| unbalanced | 64 | kappa_1 | 1 | 0.0096166667 (0.00026051) | 0.031077905 (0.000606133) | 0.423 (0.0156306) |
| unbalanced | 64 | kappa_2 | 2 | 0.0073333333 (0.00026175) | 0.016453255 (0.000648996) | 0.56 (0.015705) |
| unbalanced | 64 | kappa_16 | 16 | 0.0076166667 (0.000262678) | 0.043805956 (0.00150006) | 0.543 (0.0157607) |
| unbalanced | 64 | theorem_schedule | 36.746702 | 0.01235 (0.00125361) | 0.15761722 (0.00604329) | 0.519 (0.0158079) |
| unbalanced | 64 | empirical_dr | linear DR | 0.02275 (0.00220979) | 0.27844019 (0.0109841) | 0.495 (0.0158185) |
| unbalanced | 256 | kappa_1 | 1 | 0.010366667 (0.000255686) | 0.024823186 (0.00025449) | 0.378 (0.0153412) |
| unbalanced | 256 | kappa_2 | 2 | 0.0055166667 (0.000248138) | 0.0038155466 (0.000139702) | 0.669 (0.0148883) |
| unbalanced | 256 | kappa_16 | 16 | 0.0063 (0.000255686) | 0.0097827714 (0.000321069) | 0.622 (0.0153412) |
| unbalanced | 256 | theorem_schedule | 73.493405 | 0.0082 (0.000431601) | 0.063992917 (0.00237107) | 0.528 (0.0157945) |
| unbalanced | 256 | empirical_dr | linear DR | 0.0082166667 (0.000431606) | 0.064159342 (0.00237898) | 0.527 (0.0157962) |
| unbalanced | 1024 | kappa_1 | 1 | 0.0127 (0.00022456) | 0.023642592 (0.000130723) | 0.238 (0.0134736) |
| unbalanced | 1024 | kappa_2 | 2 | 0.0032833333 (0.000209728) | 0.0012616982 (4.20186e-05) | 0.803 (0.0125837) |
| unbalanced | 1024 | kappa_16 | 16 | 0.0045833333 (0.000235451) | 0.0025817493 (8.18452e-05) | 0.725 (0.0141271) |
| unbalanced | 1024 | theorem_schedule | 146.98681 | 0.0064 (0.000256461) | 0.016116669 (0.000570184) | 0.616 (0.0153877) |
| unbalanced | 1024 | empirical_dr | linear DR | 0.0064 (0.000256461) | 0.016116913 (0.000570192) | 0.616 (0.0153877) |
| unbalanced | 4096 | kappa_1 | 1 | 0.015116667 (0.000153148) | 0.023406144 (6.41994e-05) | 0.093 (0.00918888) |
| unbalanced | 4096 | kappa_2 | 2 | 0.00083333333 (0.000114925) | 0.00054239862 (1.2109e-05) | 0.95 (0.00689547) |
| unbalanced | 4096 | kappa_16 | 16 | 0.0020333333 (0.000172581) | 0.00072587736 (2.30726e-05) | 0.878 (0.0103549) |
| unbalanced | 4096 | theorem_schedule | 293.97362 | 0.0051 (0.000243) | 0.0043364329 (0.000161148) | 0.694 (0.01458) |
| unbalanced | 4096 | empirical_dr | linear DR | 0.0051 (0.000243) | 0.0043364482 (0.000161149) | 0.694 (0.01458) |
| unbalanced | 16384 | kappa_1 | 1 | 0.0166 (3.32832e-05) | 0.023277176 (3.17978e-05) | 0.004 (0.00199699) |
| unbalanced | 16384 | kappa_2 | 2 | 1.6666667e-05 (1.66667e-05) | 0.0003575748 (4.86222e-06) | 0.999 (0.001) |
| unbalanced | 16384 | kappa_16 | 16 | 0.0001 (4.07225e-05) | 0.00021558049 (6.10373e-06) | 0.994 (0.00244335) |
| unbalanced | 16384 | theorem_schedule | 587.94724 | 0.0030333333 (0.00020346) | 0.0010241787 (3.36814e-05) | 0.818 (0.0122076) |
| unbalanced | 16384 | empirical_dr | linear DR | 0.0030333333 (0.00020346) | 0.0010241797 (3.36815e-05) | 0.818 (0.0122076) |
| unbalanced | 65536 | kappa_1 | 1 | 0.016666667 (0) | 0.023321833 (1.6607e-05) | 0 (0) |
| unbalanced | 65536 | kappa_2 | 2 | 0 (0) | 0.0003216884 (2.30697e-06) | 1 (0) |
| unbalanced | 65536 | kappa_16 | 16 | 0 (0) | 9.7971502e-05 (2.33012e-06) | 1 (0) |
| unbalanced | 65536 | theorem_schedule | 1175.8945 | 0.00081666667 (0.000113829) | 0.00026736477 (9.72122e-06) | 0.951 (0.00682976) |
| unbalanced | 65536 | empirical_dr | linear DR | 0.00081666667 (0.000113829) | 0.00026736482 (9.72122e-06) | 0.951 (0.00682976) |

## High-middle pair variance

Empirical variances use 999 degrees of freedom. Exact variances retain both first-order projections and the degenerate remainder. The independent-pair column shows Var(Y)/(n_H n_M), which omits covariance from reused observations. The DR row uses its algebraically equivalent linear pair kernel; its degenerate component is zero up to floating-point precision.

| Sampling | Base n | Method | Empirical variance | Exact variance | Empirical / exact | Incorrect independent-pair variance | Exact / incorrect |
|---|---:|---|---:|---:|---:|---:|---:|
| balanced | 64 | kappa_1 | 0.035663021 | 0.038791905 | 0.919342 | 0.00061158721 | 63.4282 |
| balanced | 64 | kappa_2 | 0.073125021 | 0.07952505 | 0.919522 | 0.0012520928 | 63.5137 |
| balanced | 64 | kappa_16 | 0.2320802 | 0.23704812 | 0.979043 | 0.0037133937 | 63.836 |
| balanced | 64 | theorem_schedule | 0.92536895 | 0.92099577 | 1.00475 | 0.014400076 | 63.9577 |
| balanced | 64 | empirical_dr | 1.6564761 | 1.6407828 | 1.00956 | 0.025637232 | 64 |
| balanced | 256 | kappa_1 | 0.0096545188 | 0.0096969356 | 0.995626 | 3.8224201e-05 | 253.686 |
| balanced | 256 | kappa_2 | 0.019564857 | 0.01987945 | 0.984175 | 7.8255802e-05 | 254.032 |
| balanced | 256 | kappa_16 | 0.058110188 | 0.059260216 | 0.980594 | 0.00023208711 | 255.336 |
| balanced | 256 | theorem_schedule | 0.40791876 | 0.41019561 | 0.994449 | 0.0016023266 | 256 |
| balanced | 256 | empirical_dr | 0.40791886 | 0.41019571 | 0.994449 | 0.001602327 | 256 |
| balanced | 1024 | kappa_1 | 0.0024064186 | 0.0024241688 | 0.992678 | 2.3890126e-06 | 1014.72 |
| balanced | 1024 | kappa_2 | 0.0049231758 | 0.0049697493 | 0.990629 | 4.8909876e-06 | 1016.1 |
| balanced | 1024 | kappa_16 | 0.015894873 | 0.014814941 | 1.07289 | 1.4505444e-05 | 1021.34 |
| balanced | 1024 | theorem_schedule | 0.10661618 | 0.10254892 | 1.03966 | 0.00010014543 | 1024 |
| balanced | 1024 | empirical_dr | 0.10661619 | 0.10254893 | 1.03966 | 0.00010014544 | 1024 |
| balanced | 4096 | kappa_1 | 0.00065178529 | 0.00060603815 | 1.07549 | 1.4931328e-07 | 4058.84 |
| balanced | 4096 | kappa_2 | 0.0013276302 | 0.0012424302 | 1.06858 | 3.0568673e-07 | 4064.39 |
| balanced | 4096 | kappa_16 | 0.0037846402 | 0.0037037281 | 1.02185 | 9.0659026e-07 | 4085.34 |
| balanced | 4096 | theorem_schedule | 0.02522858 | 0.025637231 | 0.98406 | 6.2590897e-06 | 4096 |
| balanced | 4096 | empirical_dr | 0.02522858 | 0.025637232 | 0.98406 | 6.2590898e-06 | 4096 |
| balanced | 16384 | kappa_1 | 0.00016257575 | 0.00015150928 | 1.07304 | 9.3320803e-09 | 16235.3 |
| balanced | 16384 | kappa_2 | 0.00032495853 | 0.00031060712 | 1.0462 | 1.910542e-08 | 16257.5 |
| balanced | 16384 | kappa_16 | 0.00092447914 | 0.00092593159 | 0.998431 | 5.6661891e-08 | 16341.3 |
| balanced | 16384 | theorem_schedule | 0.006354319 | 0.0064093079 | 0.99142 | 3.9119311e-07 | 16384 |
| balanced | 16384 | empirical_dr | 0.0063543191 | 0.0064093079 | 0.99142 | 3.9119311e-07 | 16384 |
| balanced | 65536 | kappa_1 | 3.7297762e-05 | 3.7877305e-05 | 0.984699 | 5.8325502e-10 | 64941.2 |
| balanced | 65536 | kappa_2 | 7.6502894e-05 | 7.7651752e-05 | 0.985205 | 1.1940888e-09 | 65030.1 |
| balanced | 65536 | kappa_16 | 0.00022736029 | 0.00023148287 | 0.982191 | 3.5413682e-09 | 65365.4 |
| balanced | 65536 | theorem_schedule | 0.0016061507 | 0.001602327 | 1.00239 | 2.4449569e-08 | 65536 |
| balanced | 65536 | empirical_dr | 0.0016061507 | 0.001602327 | 1.00239 | 2.4449569e-08 | 65536 |
| unbalanced | 64 | kappa_1 | 0.036925542 | 0.036501328 | 1.01162 | 0.00030579361 | 119.366 |
| unbalanced | 64 | kappa_2 | 0.071959379 | 0.07038108 | 1.02243 | 0.00062604642 | 112.422 |
| unbalanced | 64 | kappa_16 | 0.15019433 | 0.14915203 | 1.00699 | 0.0018566968 | 80.3319 |
| unbalanced | 64 | theorem_schedule | 0.48891655 | 0.49112598 | 0.995501 | 0.0072000379 | 68.2116 |
| unbalanced | 64 | empirical_dr | 0.84591727 | 0.85164141 | 0.993279 | 0.012818616 | 66.4379 |
| unbalanced | 256 | kappa_1 | 0.0081138374 | 0.0091248117 | 0.889206 | 1.91121e-05 | 477.436 |
| unbalanced | 256 | kappa_2 | 0.015701503 | 0.017594364 | 0.892417 | 3.9127901e-05 | 449.663 |
| unbalanced | 256 | kappa_16 | 0.033087417 | 0.037287102 | 0.887369 | 0.00011604355 | 321.32 |
| unbalanced | 256 | theorem_schedule | 0.19323726 | 0.2129103 | 0.907599 | 0.0008011633 | 265.751 |
| unbalanced | 256 | empirical_dr | 0.1932373 | 0.21291035 | 0.907599 | 0.00080116349 | 265.751 |
| unbalanced | 1024 | kappa_1 | 0.0022588707 | 0.0022811704 | 0.990224 | 1.1945063e-06 | 1909.72 |
| unbalanced | 1024 | kappa_2 | 0.0043445563 | 0.0043985344 | 0.987728 | 2.4454938e-06 | 1798.63 |
| unbalanced | 1024 | kappa_16 | 0.0086930421 | 0.0093217189 | 0.932558 | 7.252722e-06 | 1285.27 |
| unbalanced | 1024 | theorem_schedule | 0.049138141 | 0.053227585 | 0.923171 | 5.0072715e-05 | 1063.01 |
| unbalanced | 1024 | empirical_dr | 0.049138144 | 0.053227588 | 0.923171 | 5.0072718e-05 | 1063.01 |
| unbalanced | 4096 | kappa_1 | 0.00055663899 | 0.00057029057 | 0.976062 | 7.4656642e-08 | 7638.85 |
| unbalanced | 4096 | kappa_2 | 0.0010667177 | 0.0010996301 | 0.97007 | 1.5284336e-07 | 7194.49 |
| unbalanced | 4096 | kappa_16 | 0.0022482185 | 0.0023304262 | 0.964724 | 4.5329513e-07 | 5141.08 |
| unbalanced | 4096 | theorem_schedule | 0.013134006 | 0.013306897 | 0.987007 | 3.1295448e-06 | 4252.02 |
| unbalanced | 4096 | empirical_dr | 0.013134006 | 0.013306897 | 0.987007 | 3.1295449e-06 | 4252.02 |
| unbalanced | 16384 | kappa_1 | 0.00013540972 | 0.00014257252 | 0.94976 | 4.6660402e-09 | 30555.4 |
| unbalanced | 16384 | kappa_2 | 0.00026325046 | 0.00027490729 | 0.957597 | 9.5527102e-09 | 28777.9 |
| unbalanced | 16384 | kappa_16 | 0.00054799389 | 0.00058260632 | 0.94059 | 2.8330945e-08 | 20564.3 |
| unbalanced | 16384 | theorem_schedule | 0.003125373 | 0.0033267243 | 0.939475 | 1.9559655e-07 | 17008.1 |
| unbalanced | 16384 | empirical_dr | 0.0031253731 | 0.0033267243 | 0.939475 | 1.9559656e-07 | 17008.1 |
| unbalanced | 65536 | kappa_1 | 3.8864901e-05 | 3.5643121e-05 | 1.09039 | 2.9162751e-10 | 122221 |
| unbalanced | 65536 | kappa_2 | 7.4699255e-05 | 6.8726809e-05 | 1.0869 | 5.9704439e-10 | 115112 |
| unbalanced | 65536 | kappa_16 | 0.0001494498 | 0.00014565157 | 1.02608 | 1.7706841e-09 | 82257.2 |
| unbalanced | 65536 | theorem_schedule | 0.00083935052 | 0.00083168107 | 1.00922 | 1.2224785e-08 | 68032.4 |
| unbalanced | 65536 | empirical_dr | 0.00083935052 | 0.00083168107 | 1.00922 | 1.2224785e-08 | 68032.4 |

## Exact population targets

These rows enumerate the residual support and contain no Monte Carlo uncertainty. Repeated temperatures have the same population target in both sampling designs. The JSON outputs also retain all projection components and each population score.

| Sampling | Base n | Method | Population regret | Population squared score error |
|---|---:|---|---:|---:|
| balanced | 64 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 64 | kappa_2 | 0 | 0.00030065644 |
| balanced | 64 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 64 | theorem_schedule | 0 | 5.2904871e-05 |
| balanced | 64 | empirical_dr | 0 | 2.5679066e-32 |
| balanced | 256 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 256 | kappa_2 | 0 | 0.00030065644 |
| balanced | 256 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 256 | theorem_schedule | 0 | 4.2727124e-10 |
| balanced | 256 | empirical_dr | 0 | 2.5679066e-32 |
| balanced | 1024 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 1024 | kappa_2 | 0 | 0.00030065644 |
| balanced | 1024 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 1024 | theorem_schedule | 0 | 3.8545494e-12 |
| balanced | 1024 | empirical_dr | 0 | 2.5679066e-32 |
| balanced | 4096 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 4096 | kappa_2 | 0 | 0.00030065644 |
| balanced | 4096 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 4096 | theorem_schedule | 0 | 2.4091112e-13 |
| balanced | 4096 | empirical_dr | 0 | 2.5679066e-32 |
| balanced | 16384 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 16384 | kappa_2 | 0 | 0.00030065644 |
| balanced | 16384 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 16384 | theorem_schedule | 0 | 1.5056954e-14 |
| balanced | 16384 | empirical_dr | 0 | 2.5679066e-32 |
| balanced | 65536 | kappa_1 | 0.016666667 | 0.023279178 |
| balanced | 65536 | kappa_2 | 0 | 0.00030065644 |
| balanced | 65536 | kappa_16 | 0 | 5.4807587e-05 |
| balanced | 65536 | theorem_schedule | 0 | 9.4106266e-16 |
| balanced | 65536 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 64 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 64 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 64 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 64 | theorem_schedule | 0 | 5.2904871e-05 |
| unbalanced | 64 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 256 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 256 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 256 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 256 | theorem_schedule | 0 | 4.2727124e-10 |
| unbalanced | 256 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 1024 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 1024 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 1024 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 1024 | theorem_schedule | 0 | 3.8545494e-12 |
| unbalanced | 1024 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 4096 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 4096 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 4096 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 4096 | theorem_schedule | 0 | 2.4091112e-13 |
| unbalanced | 4096 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 16384 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 16384 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 16384 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 16384 | theorem_schedule | 0 | 1.5056954e-14 |
| unbalanced | 16384 | empirical_dr | 0 | 2.5679066e-32 |
| unbalanced | 65536 | kappa_1 | 0.016666667 | 0.023279178 |
| unbalanced | 65536 | kappa_2 | 0 | 0.00030065644 |
| unbalanced | 65536 | kappa_16 | 0 | 5.4807587e-05 |
| unbalanced | 65536 | theorem_schedule | 0 | 9.4106266e-16 |
| unbalanced | 65536 | empirical_dr | 0 | 2.5679066e-32 |
