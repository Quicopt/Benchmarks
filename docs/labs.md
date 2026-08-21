# LABS — Low-Autocorrelation Binary Sequences

Low-Autocorrelation Binary Sequences: find a ±1 sequence of length N minimizing the off-peak autocorrelation energy E = sum_k C_k^2. Quality is read as the merit factor F = N^2 / (2E) (higher is better), and `%_of_best` is the ratio of merit factors — 100 means the reference was matched. For N ≤ 66 the reference is the *proven* optimum (Packebusch & Mertens, [arXiv:1512.02475](https://arxiv.org/abs/1512.02475)) and `source` reads `optimum`; above 66 no optimum is known and the reference is the best heuristic record we are aware of — Knauer's 2004 table, superseded at N=92, 98 and 99 by the GPU memetic-tabu results of Zhang et al. ([arXiv:2504.00987](https://arxiv.org/abs/2504.00987), v2). Those are third-party attributions, not Quicopt output, and the ones above N=66 move as new records are published. Two solver versions are reported below, newest first; on the 97 lengths both cover, v0.2 reaches a lower energy at 81 and ties the other 16.

### Quicopt v0.2

**99/99 instances graded vs best-known** — median 100.0%, range 72.7–100.0% of best-known.

Per row: `runs` independent runs were made and the best is reported. `cpu_time_s` is that batch's total measured CPU time, and `wall_time_s` is the same batch spread over 100 cores — `cpu_time_s`/100 — so that it reads on the same basis as the v0.1 table below. The runs did not actually occupy 100 cores, so treat that column as a projection at perfect parallel efficiency and `cpu_time_s` as the measurement. Both columns cost the whole batch, so divide `cpu_time_s` by `runs` for the per-run average that benchmark submissions usually report. Solution certificates (the best sequence per instance) are in [`../LABS/solutions/`](../LABS/solutions/); recompute and check them with [`../LABS/notebooks/verify_solutions.ipynb`](../LABS/notebooks/verify_solutions.ipynb) — a LABS instance is just its length, so that notebook needs no instance data and runs offline.

| instance | N | energy | merit_factor | best-known | %_of_best | source | runs | wall_time_s | cpu_time_s | hardware | solver |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LABS-2 | 2 | 1 | 2.0 | 1 | 100.0 | optimum | 100 | 0.0001 | 0.009 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-3 | 3 | 1 | 4.5 | 1 | 100.0 | optimum | 100 | 0.0008 | 0.082 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-4 | 4 | 2 | 4.0 | 2 | 100.0 | optimum | 100 | 0.0001 | 0.011 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-5 | 5 | 2 | 6.25 | 2 | 100.0 | optimum | 100 | 0.0001 | 0.012 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-6 | 6 | 7 | 2.57 | 7 | 100.0 | optimum | 100 | 0.0001 | 0.014 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-7 | 7 | 3 | 8.17 | 3 | 100.0 | optimum | 100 | 0.0001 | 0.015 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-8 | 8 | 8 | 4.0 | 8 | 100.0 | optimum | 100 | 0.0001 | 0.013 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-9 | 9 | 12 | 3.38 | 12 | 100.0 | optimum | 100 | 0.0001 | 0.013 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-10 | 10 | 13 | 3.85 | 13 | 100.0 | optimum | 100 | 0.0002 | 0.017 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-11 | 11 | 5 | 12.1 | 5 | 100.0 | optimum | 100 | 0.0002 | 0.017 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-12 | 12 | 10 | 7.2 | 10 | 100.0 | optimum | 100 | 0.0001 | 0.015 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-13 | 13 | 6 | 14.08 | 6 | 100.0 | optimum | 100 | 0.0002 | 0.016 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-14 | 14 | 19 | 5.16 | 19 | 100.0 | optimum | 100 | 0.0002 | 0.017 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-15 | 15 | 15 | 7.5 | 15 | 100.0 | optimum | 100 | 0.0002 | 0.018 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-16 | 16 | 24 | 5.33 | 24 | 100.0 | optimum | 100 | 0.0002 | 0.018 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-17 | 17 | 32 | 4.52 | 32 | 100.0 | optimum | 100 | 0.0002 | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-18 | 18 | 25 | 6.48 | 25 | 100.0 | optimum | 100 | 0.0002 | 0.022 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-19 | 19 | 29 | 6.22 | 29 | 100.0 | optimum | 100 | 0.0002 | 0.022 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-20 | 20 | 26 | 7.69 | 26 | 100.0 | optimum | 100 | 0.0002 | 0.022 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-21 | 21 | 26 | 8.48 | 26 | 100.0 | optimum | 100 | 0.0003 | 0.025 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-22 | 22 | 39 | 6.21 | 39 | 100.0 | optimum | 100 | 0.0003 | 0.026 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-23 | 23 | 47 | 5.63 | 47 | 100.0 | optimum | 100 | 0.0024 | 0.237 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-24 | 24 | 36 | 8.0 | 36 | 100.0 | optimum | 100 | 0.0026 | 0.26 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-25 | 25 | 36 | 8.68 | 36 | 100.0 | optimum | 100 | 0.0264 | 2.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-26 | 26 | 45 | 7.51 | 45 | 100.0 | optimum | 100 | 0.0028 | 0.278 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-27 | 27 | 37 | 9.85 | 37 | 100.0 | optimum | 100 | 0.3082 | 30.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-28 | 28 | 50 | 7.84 | 50 | 100.0 | optimum | 100 | 0.0288 | 2.88 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-29 | 29 | 62 | 6.78 | 62 | 100.0 | optimum | 100 | 0.0303 | 3.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-30 | 30 | 59 | 7.63 | 59 | 100.0 | optimum | 100 | 0.0318 | 3.18 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-31 | 31 | 67 | 7.17 | 67 | 100.0 | optimum | 100 | 0.3206 | 32.06 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-32 | 32 | 64 | 8.0 | 64 | 100.0 | optimum | 100 | 0.0345 | 3.45 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-33 | 33 | 64 | 8.51 | 64 | 100.0 | optimum | 100 | 0.3727 | 37.27 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-34 | 34 | 65 | 8.89 | 65 | 100.0 | optimum | 100 | 0.4089 | 40.89 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-35 | 35 | 73 | 8.39 | 73 | 100.0 | optimum | 100 | 0.0395 | 3.95 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-36 | 36 | 82 | 7.9 | 82 | 100.0 | optimum | 25 | 1.05 | 104.86 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-37 | 37 | 86 | 7.96 | 86 | 100.0 | optimum | 100 | 0.4077 | 40.77 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-38 | 38 | 87 | 8.3 | 87 | 100.0 | optimum | 100 | 0.4457 | 44.57 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-39 | 39 | 99 | 7.68 | 99 | 100.0 | optimum | 10 | 4.22 | 422.24 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-40 | 40 | 108 | 7.41 | 108 | 100.0 | optimum | 25 | 1.14 | 114.39 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-41 | 41 | 108 | 7.78 | 108 | 100.0 | optimum | 5 | 167.16 | 16716.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-42 | 42 | 101 | 8.73 | 101 | 100.0 | optimum | 10 | 4.57 | 456.79 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-43 | 43 | 109 | 8.48 | 109 | 100.0 | optimum | 10 | 4.82 | 481.68 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-44 | 44 | 122 | 7.93 | 122 | 100.0 | optimum | 25 | 23.44 | 2344.34 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-45 | 45 | 118 | 8.58 | 118 | 100.0 | optimum | 25 | 24.01 | 2401.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-46 | 46 | 131 | 8.08 | 131 | 100.0 | optimum | 100 | 0.0484 | 4.84 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-47 | 47 | 135 | 8.18 | 135 | 100.0 | optimum | 25 | 24.46 | 2445.54 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-48 | 48 | 140 | 8.23 | 140 | 100.0 | optimum | 25 | 24.79 | 2479.16 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-49 | 49 | 136 | 8.83 | 136 | 100.0 | optimum | 5 | 186.78 | 18678.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-50 | 50 | 153 | 8.17 | 153 | 100.0 | optimum | 25 | 26.15 | 2615.45 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-51 | 51 | 153 | 8.5 | 153 | 100.0 | optimum | 5 | 194.08 | 19407.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-52 | 52 | 166 | 8.14 | 166 | 100.0 | optimum | 5 | 203.5 | 20349.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-53 | 53 | 170 | 8.26 | 170 | 100.0 | optimum | 5 | 206.0 | 20600.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-54 | 54 | 175 | 8.33 | 175 | 100.0 | optimum | 5 | 216.33 | 21632.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-55 | 55 | 171 | 8.85 | 171 | 100.0 | optimum | 8 | 13.45 | 1345.47 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-56 | 56 | 192 | 8.17 | 192 | 100.0 | optimum | 5 | 208.15 | 20815.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-57 | 57 | 188 | 8.64 | 188 | 100.0 | optimum | 5 | 217.98 | 21797.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-58 | 58 | 197 | 8.54 | 197 | 100.0 | optimum | 5 | 229.93 | 22993.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-59 | 59 | 205 | 8.49 | 205 | 100.0 | optimum | 5 | 242.4 | 24239.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-60 | 60 | 218 | 8.26 | 218 | 100.0 | optimum | 5 | 255.18 | 25518.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-61 | 61 | 226 | 8.23 | 226 | 100.0 | optimum | 5 | 235.71 | 23570.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-62 | 62 | 235 | 8.18 | 235 | 100.0 | optimum | 5 | 242.04 | 24204.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-63 | 63 | 207 | 9.59 | 207 | 100.0 | optimum | 5 | 254.38 | 25438.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-64 | 64 | 208 | 9.85 | 208 | 100.0 | optimum | 5 | 260.99 | 26099.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-65 | 65 | 240 | 8.8 | 240 | 100.0 | optimum | 5 | 264.04 | 26404.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-66 | 66 | 257 | 8.47 | 257 | 100.0 | optimum | 20 | 598.9 | 59890.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-67 | 67 | 273 | 8.22 | 241 | 88.28 | Knauer 2004 | 5 | 265.52 | 26551.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-68 | 68 | 250 | 9.25 | 250 | 100.0 | Knauer 2004 | 5 | 272.53 | 27253.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-69 | 69 | 274 | 8.69 | 274 | 100.0 | Knauer 2004 | 5 | 287.08 | 28708.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-70 | 70 | 295 | 8.31 | 295 | 100.0 | Knauer 2004 | 5 | 310.68 | 31067.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-71 | 71 | 327 | 7.71 | 275 | 84.1 | Knauer 2004 | 5 | 299.45 | 29945.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-72 | 72 | 300 | 8.64 | 300 | 100.0 | Knauer 2004 | 40 | 1114.34 | 111433.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-73 | 73 | 316 | 8.43 | 308 | 97.47 | Knauer 2004 | 40 | 1228.79 | 122879.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-74 | 74 | 349 | 7.85 | 341 | 97.71 | Knauer 2004 | 5 | 321.43 | 32143.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-75 | 75 | 341 | 8.25 | 329 | 96.48 | Knauer 2004 | 5 | 329.2 | 32920.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-76 | 76 | 362 | 7.98 | 334 | 92.27 | Knauer 2004 | 5 | 353.2 | 35319.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-77 | 77 | 394 | 7.52 | 358 | 90.86 | Knauer 2004 | 5 | 354.04 | 35404.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-78 | 78 | 411 | 7.4 | 347 | 84.43 | Knauer 2004 | 5 | 342.41 | 34241.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-79 | 79 | 407 | 7.67 | 339 | 83.29 | Knauer 2004 | 5 | 353.52 | 35352.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-80 | 80 | 384 | 8.33 | 352 | 91.67 | Knauer 2004 | 5 | 373.16 | 37316.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-81 | 81 | 408 | 8.04 | 372 | 91.18 | Knauer 2004 | 5 | 373.8 | 37379.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-82 | 82 | 457 | 7.36 | 377 | 82.49 | Knauer 2004 | 5 | 392.44 | 39243.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-83 | 83 | 437 | 7.88 | 377 | 86.27 | Knauer 2004 | 5 | 374.14 | 37414.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-84 | 84 | 466 | 7.57 | 430 | 92.27 | Knauer 2004 | 5 | 385.43 | 38542.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-85 | 85 | 482 | 7.49 | 414 | 85.89 | Knauer 2004 | 5 | 399.36 | 39935.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-86 | 86 | 471 | 7.85 | 439 | 93.21 | Knauer 2004 | 5 | 389.96 | 38996.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-87 | 87 | 491 | 7.71 | 431 | 87.78 | Knauer 2004 | 5 | 400.88 | 40088.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-88 | 88 | 528 | 7.33 | 448 | 84.85 | Knauer 2004 | 5 | 417.25 | 41724.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-89 | 89 | 516 | 7.68 | 432 | 83.72 | Knauer 2004 | 5 | 435.24 | 43524.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-90 | 90 | 565 | 7.17 | 453 | 80.18 | Knauer 2004 | 5 | 453.14 | 45314.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-91 | 91 | 589 | 7.03 | 477 | 80.98 | Knauer 2004 | 5 | 441.61 | 44161.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-92 | 92 | 578 | 7.32 | 490 | 84.78 | JPMorgan 2025 | 5 | 457.97 | 45797.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-93 | 93 | 618 | 7.0 | 486 | 78.64 | Knauer 2004 | 5 | 474.31 | 47431.2 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-94 | 94 | 635 | 6.96 | 499 | 78.58 | Knauer 2004 | 5 | 476.52 | 47652.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-95 | 95 | 659 | 6.85 | 479 | 72.69 | Knauer 2004 | 5 | 503.12 | 50311.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-96 | 96 | 628 | 7.34 | 520 | 82.8 | Knauer 2004 | 5 | 520.29 | 52028.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-97 | 97 | 636 | 7.4 | 536 | 84.28 | Knauer 2004 | 40 | 2496.02 | 249602.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-98 | 98 | 601 | 7.99 | 529 | 88.02 | JPMorgan 2025 | 5 | 516.69 | 51668.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-99 | 99 | 725 | 6.76 | 553 | 76.28 | JPMorgan 2025 | 5 | 538.93 | 53892.8 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |
| LABS-100 | 100 | 666 | 7.51 | 578 | 86.79 | Knauer 2004 | 25 | 1906.88 | 190688.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.2 |

### Quicopt v0.1

**97/97 instances graded vs best-known** — median 64.4%, range 51.4–100.0% of best-known.

Per row: `energy` is the best over a batch of 100 single-core seeds run in parallel on 100 cores, and `wall_time_s` is that batch's measured wall-clock (≈ the slowest seed).

| instance | N | energy | merit_factor | best-known | %_of_best | source | wall_time_s | hardware | solver |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LABS-4 | 4 | 2 | 4.0 | 2 | 100.0 | optimum | 0.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-5 | 5 | 2 | 6.25 | 2 | 100.0 | optimum | 0.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-6 | 6 | 7 | 2.57 | 7 | 100.0 | optimum | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-7 | 7 | 3 | 8.17 | 3 | 100.0 | optimum | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-8 | 8 | 8 | 4.0 | 8 | 100.0 | optimum | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-9 | 9 | 12 | 3.38 | 12 | 100.0 | optimum | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-10 | 10 | 13 | 3.85 | 13 | 100.0 | optimum | 0.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-11 | 11 | 5 | 12.1 | 5 | 100.0 | optimum | 0.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-12 | 12 | 10 | 7.2 | 10 | 100.0 | optimum | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-13 | 13 | 6 | 14.08 | 6 | 100.0 | optimum | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-14 | 14 | 19 | 5.16 | 19 | 100.0 | optimum | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-15 | 15 | 23 | 4.89 | 15 | 65.22 | optimum | 0.05 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-16 | 16 | 24 | 5.33 | 24 | 100.0 | optimum | 0.05 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-17 | 17 | 32 | 4.52 | 32 | 100.0 | optimum | 0.06 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-18 | 18 | 25 | 6.48 | 25 | 100.0 | optimum | 0.06 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-19 | 19 | 37 | 4.88 | 29 | 78.38 | optimum | 0.07 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-20 | 20 | 34 | 5.88 | 26 | 76.47 | optimum | 0.07 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-21 | 21 | 34 | 6.49 | 26 | 76.47 | optimum | 0.08 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-22 | 22 | 39 | 6.21 | 39 | 100.0 | optimum | 0.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-23 | 23 | 51 | 5.19 | 47 | 92.16 | optimum | 0.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-24 | 24 | 52 | 5.54 | 36 | 69.23 | optimum | 0.11 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-25 | 25 | 56 | 5.58 | 36 | 64.29 | optimum | 0.13 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-26 | 26 | 61 | 5.54 | 45 | 73.77 | optimum | 0.14 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-27 | 27 | 37 | 9.85 | 37 | 100.0 | optimum | 0.16 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-28 | 28 | 74 | 5.3 | 50 | 67.57 | optimum | 0.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-29 | 29 | 78 | 5.39 | 62 | 79.49 | optimum | 0.21 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-30 | 30 | 83 | 5.42 | 59 | 71.08 | optimum | 0.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-31 | 31 | 83 | 5.79 | 67 | 80.72 | optimum | 0.25 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-32 | 32 | 80 | 6.4 | 64 | 80.0 | optimum | 0.27 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-33 | 33 | 104 | 5.24 | 64 | 61.54 | optimum | 0.31 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-34 | 34 | 97 | 5.96 | 65 | 67.01 | optimum | 0.34 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-35 | 35 | 109 | 5.62 | 73 | 66.97 | optimum | 0.45 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-36 | 36 | 114 | 5.68 | 82 | 71.93 | optimum | 0.37 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-37 | 37 | 106 | 6.46 | 86 | 81.13 | optimum | 0.41 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-38 | 38 | 135 | 5.35 | 87 | 64.44 | optimum | 0.53 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-39 | 39 | 139 | 5.47 | 99 | 71.22 | optimum | 0.54 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-40 | 40 | 144 | 5.56 | 108 | 75.0 | optimum | 0.52 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-41 | 41 | 140 | 6.0 | 108 | 77.14 | optimum | 0.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-42 | 42 | 157 | 5.62 | 101 | 64.33 | optimum | 0.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-43 | 43 | 161 | 5.74 | 109 | 67.7 | optimum | 0.72 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-44 | 44 | 186 | 5.2 | 122 | 65.59 | optimum | 0.84 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-45 | 45 | 170 | 5.96 | 118 | 69.41 | optimum | 0.72 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-46 | 46 | 155 | 6.83 | 131 | 84.52 | optimum | 0.78 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-47 | 47 | 219 | 5.04 | 135 | 61.64 | optimum | 0.84 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-48 | 48 | 208 | 5.54 | 140 | 67.31 | optimum | 1.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-49 | 49 | 224 | 5.36 | 136 | 60.71 | optimum | 1.11 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-50 | 50 | 257 | 4.86 | 153 | 59.53 | optimum | 1.49 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-51 | 51 | 221 | 5.88 | 153 | 69.23 | optimum | 1.12 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-52 | 52 | 242 | 5.59 | 166 | 68.6 | optimum | 1.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-53 | 53 | 238 | 5.9 | 170 | 71.43 | optimum | 1.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-54 | 54 | 263 | 5.54 | 175 | 66.54 | optimum | 1.42 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-55 | 55 | 299 | 5.06 | 171 | 57.19 | optimum | 2.13 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-56 | 56 | 304 | 5.16 | 192 | 63.16 | optimum | 1.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-57 | 57 | 316 | 5.14 | 188 | 59.49 | optimum | 1.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-58 | 58 | 301 | 5.59 | 197 | 65.45 | optimum | 1.85 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-59 | 59 | 313 | 5.56 | 205 | 65.5 | optimum | 2.29 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-60 | 60 | 346 | 5.2 | 218 | 63.01 | optimum | 2.24 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-61 | 61 | 358 | 5.2 | 226 | 63.13 | optimum | 2.76 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-62 | 62 | 371 | 5.18 | 235 | 63.34 | optimum | 2.5 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-63 | 63 | 351 | 5.65 | 207 | 58.97 | optimum | 2.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-64 | 64 | 396 | 5.17 | 208 | 52.53 | optimum | 3.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-65 | 65 | 400 | 5.28 | 240 | 60.0 | optimum | 3.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-66 | 66 | 417 | 5.22 | 257 | 61.63 | optimum | 3.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-67 | 67 | 357 | 6.29 | 241 | 67.51 | Knauer 2004 | 4.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-68 | 68 | 442 | 5.23 | 250 | 56.56 | Knauer 2004 | 3.7 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-69 | 69 | 470 | 5.06 | 274 | 58.3 | Knauer 2004 | 3.46 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-70 | 70 | 479 | 5.11 | 295 | 61.59 | Knauer 2004 | 4.89 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-71 | 71 | 519 | 4.86 | 275 | 52.99 | Knauer 2004 | 5.27 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-72 | 72 | 508 | 5.1 | 300 | 59.06 | Knauer 2004 | 5.68 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-73 | 73 | 544 | 4.9 | 308 | 56.62 | Knauer 2004 | 6.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-74 | 74 | 565 | 4.85 | 341 | 60.35 | Knauer 2004 | 6.35 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-75 | 75 | 569 | 4.94 | 329 | 57.82 | Knauer 2004 | 6.43 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-76 | 76 | 586 | 4.93 | 334 | 57.0 | Knauer 2004 | 6.86 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-77 | 77 | 646 | 4.59 | 358 | 55.42 | Knauer 2004 | 6.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-78 | 78 | 667 | 4.56 | 347 | 52.02 | Knauer 2004 | 7.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-79 | 79 | 647 | 4.82 | 339 | 52.4 | Knauer 2004 | 8.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-80 | 80 | 632 | 5.06 | 352 | 55.7 | Knauer 2004 | 9.77 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-81 | 81 | 672 | 4.88 | 372 | 55.36 | Knauer 2004 | 9.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-82 | 82 | 681 | 4.94 | 377 | 55.36 | Knauer 2004 | 9.68 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-83 | 83 | 733 | 4.7 | 377 | 51.43 | Knauer 2004 | 9.65 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-84 | 84 | 730 | 4.83 | 430 | 58.9 | Knauer 2004 | 9.93 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-85 | 85 | 742 | 4.87 | 414 | 55.8 | Knauer 2004 | 12.65 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-86 | 86 | 767 | 4.82 | 439 | 57.24 | Knauer 2004 | 12.22 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-87 | 87 | 763 | 4.96 | 431 | 56.49 | Knauer 2004 | 12.48 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-88 | 88 | 740 | 5.23 | 448 | 60.54 | Knauer 2004 | 13.29 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-89 | 89 | 828 | 4.78 | 432 | 52.17 | Knauer 2004 | 14.96 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-90 | 90 | 845 | 4.79 | 453 | 53.61 | Knauer 2004 | 16.95 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-91 | 91 | 857 | 4.83 | 477 | 55.66 | Knauer 2004 | 17.47 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-92 | 92 | 738 | 5.73 | 490 | 66.4 | JPMorgan 2025 | 17.71 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-93 | 93 | 854 | 5.06 | 486 | 56.91 | Knauer 2004 | 18.76 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-94 | 94 | 915 | 4.83 | 499 | 54.54 | Knauer 2004 | 19.5 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-95 | 95 | 867 | 5.2 | 479 | 55.25 | Knauer 2004 | 18.94 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-96 | 96 | 984 | 4.68 | 520 | 52.85 | Knauer 2004 | 21.86 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-97 | 97 | 1000 | 4.7 | 536 | 53.6 | Knauer 2004 | 21.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-98 | 98 | 897 | 5.35 | 529 | 58.97 | JPMorgan 2025 | 24.49 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-99 | 99 | 985 | 4.98 | 553 | 56.14 | JPMorgan 2025 | 21.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-100 | 100 | 1022 | 4.89 | 578 | 56.56 | Knauer 2004 | 16.88 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |

---

<sub>Generated from [`../data/`](../data/) by [`../render.py`](../render.py). Reference values are third-party attributions, not Quicopt output.</sub>
