# Cross-Platform Benchmark Results

This branch records automated cross-platform `TestE2EMicroBench` latency and host CPU utilization results.

## Latest Summary by Platform and Backend

| Target | Backend | Commit | `host_new` | `getpid` | `open_close` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` |
| :--- | :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `linux/amd64` | `systrap` | `11473661` | 1.01 ms | 2.8 us (102%) | 9.0 us (111%) | 14.8 us (116%) | 5.0 us (106%) | 1.80 ms (187%) | 423.8 us (126%) | 0.2% CPU |
| `linux/arm64` | `systrap` | `11473661` | 1.97 ms | 3.2 us (102%) | 11.0 us (109%) | 17.1 us (109%) | 7.1 us (105%) | 2.13 ms (180%) | 645.4 us (115%) | 0.3% CPU |
| `windows/amd64` | `systrap` | `11473661` | 65.85 ms | 574 ns (94%) | 5.7 us (113%) | 85.0 us (110%) | 72.4 us (117%) | 12.06 ms (131%) | 8.24 ms (78%) | 1.5% CPU |
| `windows/amd64` | `whpx` | `11473661` | 10.34 ms | 16.5 us (99%) | 45.1 us (133%) | 158.3 us (169%) | 145.0 us (184%) | 1.75 ms (237%) | 1.85 ms (132%) | 0.0% CPU |
| `windows/arm64` | `systrap` | `11473661` | 94.29 ms | 999 ns (83%) | 6.2 us (87%) | 34.0 us (105%) | 28.7 us (109%) | 16.22 ms (40%) | 22.90 ms (17%) | 1.6% CPU |

## Historical Trend (Last 10 Runs per Target)

### `linux/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T16:44:58Z` | `11473661` | 2.8 us (102%) | 14.8 us (116%) | 5.0 us (106%) | 1.80 ms (187%) | 423.8 us (126%) | 0.2% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 4.5 us (104%) | 26.8 us (113%) | 10.1 us (112%) | 3.45 ms (191%) | 582.4 us (127%) | 0.4% CPU | 0 |

### `linux/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T16:44:58Z` | `11473661` | 3.2 us (102%) | 17.1 us (109%) | 7.1 us (105%) | 2.13 ms (180%) | 645.4 us (115%) | 0.3% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 3.2 us (102%) | 18.8 us (112%) | 6.6 us (106%) | 2.07 ms (177%) | 759.4 us (114%) | 0.3% CPU | 0 |

### `windows/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T16:44:58Z` | `11473661` | 574 ns (94%) | 85.0 us (110%) | 72.4 us (117%) | 12.06 ms (131%) | 8.24 ms (78%) | 1.5% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 561 ns (95%) | 80.8 us (117%) | 69.5 us (113%) | 10.74 ms (135%) | 7.31 ms (75%) | 0.8% CPU | 0 |

### `windows/amd64` (`whpx`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T16:44:58Z` | `11473661` | 16.5 us (99%) | 158.3 us (169%) | 145.0 us (184%) | 1.75 ms (237%) | 1.85 ms (132%) | 0.0% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 16.5 us (103%) | 158.4 us (189%) | 150.5 us (186%) | 1.75 ms (213%) | 1.67 ms (130%) | 0.0% CPU | 0 |

### `windows/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T16:44:58Z` | `11473661` | 999 ns (83%) | 34.0 us (105%) | 28.7 us (109%) | 16.22 ms (40%) | 22.90 ms (17%) | 1.6% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 973 ns (89%) | 34.2 us (97%) | 31.2 us (105%) | 18.81 ms (36%) | 17.70 ms (25%) | 0.0% CPU | 0 |

