# LABS — Low-Autocorrelation Binary Sequences

Low-Autocorrelation Binary Sequences: find a ±1 sequence of length N minimizing the off-peak autocorrelation energy E = sum_k C_k^2. Quality is read as the merit factor F = N^2 / (2E) (higher is better). At these sizes the proven optimum exists only for N ≤ 66 and the whole field sits well above it, so no reference/gap column is shown here — the head-to-head against Gurobi and ABS2 lives on the website. Two solver versions are reported below, newest first, over the same instances; on the 97 lengths both cover, v0.2 reaches a lower energy at 81 and ties the other 16.

### Quicopt v0.2

Per row: `runs` independent runs were made and the best is reported. `cpu_time_s` is that batch's total CPU time and `wall_time_s` its measured wall-clock on the cores named in `hardware`; the two are equal where the runs were taken one at a time on a single core. Both columns cost the whole batch, so divide by `runs` to compare against a benchmark that reports per-run averages — the runs overlapped in time, so only `cpu_time_s` divides cleanly. Solution certificates (the best sequence per instance) are in [`../LABS/solutions/`](../LABS/solutions/); recompute and check them with [`../LABS/notebooks/verify_solutions.ipynb`](../LABS/notebooks/verify_solutions.ipynb) — a LABS instance is just its length, so that notebook needs no instance data and runs offline.

| instance | N | energy | merit_factor | runs | wall_time_s | cpu_time_s | hardware | solver |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LABS-2 | 2 | 1 | 2.0 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-3 | 3 | 1 | 4.5 | 100 | 0.08 | 0.08 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-4 | 4 | 2 | 4.0 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-5 | 5 | 2 | 6.25 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-6 | 6 | 7 | 2.57 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-7 | 7 | 3 | 8.17 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-8 | 8 | 8 | 4.0 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-9 | 9 | 12 | 3.38 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-10 | 10 | 13 | 3.85 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-11 | 11 | 5 | 12.1 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-12 | 12 | 10 | 7.2 | 100 | 0.01 | 0.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-13 | 13 | 6 | 14.08 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-14 | 14 | 19 | 5.16 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-15 | 15 | 15 | 7.5 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-16 | 16 | 24 | 5.33 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-17 | 17 | 32 | 4.52 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-18 | 18 | 25 | 6.48 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-19 | 19 | 29 | 6.22 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-20 | 20 | 26 | 7.69 | 100 | 0.02 | 0.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-21 | 21 | 26 | 8.48 | 100 | 0.03 | 0.03 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-22 | 22 | 39 | 6.21 | 100 | 0.03 | 0.03 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-23 | 23 | 47 | 5.63 | 100 | 0.11 | 0.11 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-24 | 24 | 36 | 8.0 | 100 | 0.26 | 0.26 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-25 | 25 | 36 | 8.68 | 100 | 2.64 | 2.64 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-26 | 26 | 45 | 7.51 | 100 | 0.28 | 0.28 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-27 | 27 | 37 | 9.85 | 100 | 30.82 | 30.82 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-28 | 28 | 50 | 7.84 | 100 | 2.88 | 2.88 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-29 | 29 | 62 | 6.78 | 100 | 3.03 | 3.03 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-30 | 30 | 59 | 7.63 | 100 | 3.18 | 3.18 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-31 | 31 | 67 | 7.17 | 100 | 10.02 | 10.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-32 | 32 | 64 | 8.0 | 100 | 3.45 | 3.45 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-33 | 33 | 64 | 8.51 | 100 | 10.04 | 10.04 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-34 | 34 | 65 | 8.89 | 100 | 10.02 | 10.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-35 | 35 | 73 | 8.39 | 100 | 1.01 | 1.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-36 | 36 | 82 | 7.9 | 100 | 100.03 | 100.03 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-37 | 37 | 86 | 7.96 | 100 | 10.02 | 10.02 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-38 | 38 | 87 | 8.3 | 100 | 44.57 | 44.57 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-39 | 39 | 99 | 7.68 | 25 | 250.01 | 250.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-40 | 40 | 108 | 7.41 | 25 | 114.39 | 114.39 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-41 | 41 | 108 | 7.78 | 5 | 395.0 | 23026.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-42 | 42 | 101 | 8.73 | 10 | 456.79 | 456.79 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-43 | 43 | 109 | 8.48 | 10 | 481.68 | 481.68 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-44 | 44 | 122 | 7.93 | 10 | 1000.0 | 1000.0 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-45 | 45 | 118 | 8.58 | 25 | 2401.03 | 2401.03 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-46 | 46 | 131 | 8.08 | 100 | 4.84 | 4.84 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-47 | 47 | 135 | 8.18 | 10 | 1000.0 | 1000.0 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-48 | 48 | 140 | 8.23 | 25 | 2479.16 | 2479.16 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-49 | 49 | 136 | 8.83 | 5 | 449.0 | 26432.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-50 | 50 | 153 | 8.17 | 10 | 1000.01 | 1000.01 | AMD EPYC-Rome, 1 core | Quicopt v0.2 |
| LABS-51 | 51 | 153 | 8.5 | 5 | 462.0 | 27266.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-52 | 52 | 166 | 8.14 | 5 | 464.0 | 27404.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-53 | 53 | 170 | 8.26 | 5 | 541.0 | 27632.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-54 | 54 | 175 | 8.33 | 5 | 572.0 | 29394.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-55 | 55 | 171 | 8.85 | 5 | 553.0 | 28100.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-56 | 56 | 192 | 8.17 | 5 | 570.0 | 28976.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-57 | 57 | 188 | 8.64 | 5 | 580.0 | 29381.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-58 | 58 | 197 | 8.54 | 5 | 598.0 | 30496.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-59 | 59 | 205 | 8.49 | 5 | 603.0 | 31013.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-60 | 60 | 218 | 8.26 | 5 | 686.0 | 35436.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-61 | 61 | 226 | 8.23 | 5 | 607.0 | 31274.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-62 | 62 | 235 | 8.18 | 5 | 627.0 | 32291.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-63 | 63 | 207 | 9.59 | 5 | 637.0 | 32833.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-64 | 64 | 208 | 9.85 | 5 | 649.0 | 33500.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-65 | 65 | 240 | 8.8 | 5 | 665.0 | 34506.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-66 | 66 | 257 | 8.47 | 25 | 1830.0 | 102582.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-67 | 67 | 273 | 8.22 | 5 | 669.0 | 34622.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-68 | 68 | 250 | 9.25 | 5 | 687.0 | 35621.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-69 | 69 | 274 | 8.69 | 5 | 756.0 | 39257.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-70 | 70 | 295 | 8.31 | 5 | 759.0 | 39651.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-71 | 71 | 327 | 7.71 | 5 | 713.0 | 37027.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-72 | 72 | 300 | 8.64 | 45 | 2776.0 | 158094.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-73 | 73 | 316 | 8.43 | 45 | 3018.0 | 170589.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-74 | 74 | 349 | 7.85 | 45 | 3045.0 | 171502.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-75 | 75 | 341 | 8.25 | 45 | 3235.0 | 185039.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-76 | 76 | 362 | 7.98 | 5 | 833.0 | 43753.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-77 | 77 | 394 | 7.52 | 5 | 813.0 | 42668.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-78 | 78 | 411 | 7.4 | 5 | 831.0 | 43693.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-79 | 79 | 407 | 7.67 | 5 | 845.0 | 44478.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-80 | 80 | 384 | 8.33 | 5 | 864.0 | 45572.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-81 | 81 | 408 | 8.04 | 5 | 887.0 | 46800.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-82 | 82 | 457 | 7.36 | 5 | 908.0 | 48020.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-83 | 83 | 437 | 7.88 | 5 | 891.0 | 47048.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-84 | 84 | 466 | 7.57 | 5 | 908.0 | 47973.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-85 | 85 | 482 | 7.49 | 5 | 917.0 | 48404.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-86 | 86 | 471 | 7.85 | 5 | 921.0 | 48766.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-87 | 87 | 491 | 7.71 | 5 | 945.0 | 49969.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-88 | 88 | 528 | 7.33 | 5 | 991.0 | 52353.6 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-89 | 89 | 516 | 7.68 | 5 | 1018.0 | 53571.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-90 | 90 | 565 | 7.17 | 5 | 1051.0 | 56113.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-91 | 91 | 589 | 7.03 | 5 | 1027.0 | 54674.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-92 | 92 | 578 | 7.32 | 5 | 1056.0 | 56435.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-93 | 93 | 618 | 7.0 | 5 | 1070.0 | 57152.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-94 | 94 | 635 | 6.96 | 5 | 1089.0 | 58294.0 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-95 | 95 | 659 | 6.85 | 5 | 1148.0 | 61544.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-96 | 96 | 628 | 7.34 | 5 | 1175.0 | 63184.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-97 | 97 | 636 | 7.4 | 45 | 5611.0 | 325050.2 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-98 | 98 | 601 | 7.99 | 5 | 1174.0 | 62954.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-99 | 99 | 725 | 6.76 | 5 | 1210.0 | 64894.4 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |
| LABS-100 | 100 | 630 | 7.94 | 50 | 6850.0 | 404860.8 | AMD EPYC-Rome, 60 cores | Quicopt v0.2 |

### Quicopt v0.1

Per row: `energy` is the best over a batch of 100 single-core seeds run in parallel on 100 cores, and `wall_time_s` is that batch's wall-clock (≈ the slowest seed).

| instance | N | energy | merit_factor | wall_time_s | hardware | solver |
| --- | --- | --- | --- | --- | --- | --- |
| LABS-4 | 4 | 2 | 4.0 | 0.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-5 | 5 | 2 | 6.25 | 0.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-6 | 6 | 7 | 2.57 | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-7 | 7 | 3 | 8.17 | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-8 | 8 | 8 | 4.0 | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-9 | 9 | 12 | 3.38 | 0.02 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-10 | 10 | 13 | 3.85 | 0.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-11 | 11 | 5 | 12.1 | 0.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-12 | 12 | 10 | 7.2 | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-13 | 13 | 6 | 14.08 | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-14 | 14 | 19 | 5.16 | 0.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-15 | 15 | 23 | 4.89 | 0.05 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-16 | 16 | 24 | 5.33 | 0.05 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-17 | 17 | 32 | 4.52 | 0.06 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-18 | 18 | 25 | 6.48 | 0.06 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-19 | 19 | 37 | 4.88 | 0.07 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-20 | 20 | 34 | 5.88 | 0.07 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-21 | 21 | 34 | 6.49 | 0.08 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-22 | 22 | 39 | 6.21 | 0.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-23 | 23 | 51 | 5.19 | 0.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-24 | 24 | 52 | 5.54 | 0.11 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-25 | 25 | 56 | 5.58 | 0.13 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-26 | 26 | 61 | 5.54 | 0.14 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-27 | 27 | 37 | 9.85 | 0.16 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-28 | 28 | 74 | 5.3 | 0.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-29 | 29 | 78 | 5.39 | 0.21 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-30 | 30 | 83 | 5.42 | 0.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-31 | 31 | 83 | 5.79 | 0.25 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-32 | 32 | 80 | 6.4 | 0.27 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-33 | 33 | 104 | 5.24 | 0.31 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-34 | 34 | 97 | 5.96 | 0.34 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-35 | 35 | 109 | 5.62 | 0.45 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-36 | 36 | 114 | 5.68 | 0.37 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-37 | 37 | 106 | 6.46 | 0.41 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-38 | 38 | 135 | 5.35 | 0.53 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-39 | 39 | 139 | 5.47 | 0.54 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-40 | 40 | 144 | 5.56 | 0.52 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-41 | 41 | 140 | 6.0 | 0.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-42 | 42 | 157 | 5.62 | 0.6 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-43 | 43 | 161 | 5.74 | 0.72 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-44 | 44 | 186 | 5.2 | 0.84 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-45 | 45 | 170 | 5.96 | 0.72 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-46 | 46 | 155 | 6.83 | 0.78 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-47 | 47 | 219 | 5.04 | 0.84 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-48 | 48 | 208 | 5.54 | 1.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-49 | 49 | 224 | 5.36 | 1.11 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-50 | 50 | 257 | 4.86 | 1.49 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-51 | 51 | 221 | 5.88 | 1.12 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-52 | 52 | 242 | 5.59 | 1.19 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-53 | 53 | 238 | 5.9 | 1.4 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-54 | 54 | 263 | 5.54 | 1.42 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-55 | 55 | 299 | 5.06 | 2.13 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-56 | 56 | 304 | 5.16 | 1.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-57 | 57 | 316 | 5.14 | 1.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-58 | 58 | 301 | 5.59 | 1.85 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-59 | 59 | 313 | 5.56 | 2.29 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-60 | 60 | 346 | 5.2 | 2.24 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-61 | 61 | 358 | 5.2 | 2.76 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-62 | 62 | 371 | 5.18 | 2.5 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-63 | 63 | 351 | 5.65 | 2.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-64 | 64 | 396 | 5.17 | 3.0 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-65 | 65 | 400 | 5.28 | 3.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-66 | 66 | 417 | 5.22 | 3.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-67 | 67 | 357 | 6.29 | 4.01 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-68 | 68 | 442 | 5.23 | 3.7 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-69 | 69 | 470 | 5.06 | 3.46 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-70 | 70 | 479 | 5.11 | 4.89 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-71 | 71 | 519 | 4.86 | 5.27 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-72 | 72 | 508 | 5.1 | 5.68 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-73 | 73 | 544 | 4.9 | 6.75 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-74 | 74 | 565 | 4.85 | 6.35 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-75 | 75 | 569 | 4.94 | 6.43 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-76 | 76 | 586 | 4.93 | 6.86 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-77 | 77 | 646 | 4.59 | 6.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-78 | 78 | 667 | 4.56 | 7.04 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-79 | 79 | 647 | 4.82 | 8.03 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-80 | 80 | 632 | 5.06 | 9.77 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-81 | 81 | 672 | 4.88 | 9.1 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-82 | 82 | 681 | 4.94 | 9.68 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-83 | 83 | 733 | 4.7 | 9.65 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-84 | 84 | 730 | 4.83 | 9.93 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-85 | 85 | 742 | 4.87 | 12.65 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-86 | 86 | 767 | 4.82 | 12.22 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-87 | 87 | 763 | 4.96 | 12.48 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-88 | 88 | 740 | 5.23 | 13.29 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-89 | 89 | 828 | 4.78 | 14.96 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-90 | 90 | 845 | 4.79 | 16.95 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-91 | 91 | 857 | 4.83 | 17.47 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-92 | 92 | 738 | 5.73 | 17.71 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-93 | 93 | 854 | 5.06 | 18.76 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-94 | 94 | 915 | 4.83 | 19.5 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-95 | 95 | 867 | 5.2 | 18.94 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-96 | 96 | 984 | 4.68 | 21.86 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-97 | 97 | 1000 | 4.7 | 21.82 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-98 | 98 | 897 | 5.35 | 24.49 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-99 | 99 | 985 | 4.98 | 21.64 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |
| LABS-100 | 100 | 1022 | 4.89 | 16.88 | AMD EPYC-Rome, 100 cores | Quicopt v0.1 |

---

<sub>Generated from [`../data/`](../data/) by [`../render.py`](../render.py). Reference values are third-party attributions, not Quicopt output.</sub>
