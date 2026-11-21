# Cross-Platform Benchmark Results

This branch records automated cross-platform `TestE2EMicroBench` latency and host CPU utilization results.

## Latest Summary by Platform and Backend

| Target | Backend | Commit | `host_new` | `getpid` | `open_close` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` |
| :--- | :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `linux/amd64` | `systrap` | `de66c0f7` | 1.85 ms | 4.2 us (105%) | 14.7 us (115%) | 26.3 us (109%) | 9.9 us (112%) | 2.89 ms (191%) | 616.0 us (126%) | 0.4% CPU |
| `linux/arm64` | `systrap` | `de66c0f7` | 111.63 ms | 3.1 us (102%) | 10.8 us (110%) | 17.5 us (110%) | 6.8 us (106%) | 1.95 ms (180%) | 709.4 us (116%) | 0.3% CPU |
| `windows/amd64` | `systrap` | `de66c0f7` | 44.99 ms | 425 ns (106%) | 3.1 us (109%) | 35.4 us (105%) | 32.0 us (118%) | 5.94 ms (114%) | 4.07 ms (81%) | 1.6% CPU |
| `windows/amd64` | `whpx` | `de66c0f7` | 9.96 ms | 11.5 us (107%) | 27.3 us (128%) | 68.8 us (163%) | 64.0 us (177%) | 959.6 us (210%) | 1.08 ms (123%) | 0.0% CPU |
| `windows/arm64` | `systrap` | `de66c0f7` | 114.95 ms | 952 ns (86%) | 5.4 us (111%) | 30.5 us (120%) | 27.6 us (104%) | 16.98 ms (37%) | 17.84 ms (19%) | 1.6% CPU |

## Historical Trend (Last 10 Runs per Target)

### `linux/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-21T16:45:40Z` | `de66c0f7` | 4.2 us (105%) | 26.3 us (109%) | 9.9 us (112%) | 2.89 ms (191%) | 616.0 us (126%) | 0.4% CPU | 0 |
| `2026-11-20T21:36:43Z` | `a55326e7` | 4.1 us (105%) | 28.6 us (119%) | 9.8 us (112%) | 3.89 ms (188%) | 593.1 us (128%) | 0.4% CPU | 0 |
| `2026-11-20T16:44:58Z` | `11473661` | 2.8 us (102%) | 14.8 us (116%) | 5.0 us (106%) | 1.80 ms (187%) | 423.8 us (126%) | 0.2% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 4.5 us (104%) | 26.8 us (113%) | 10.1 us (112%) | 3.45 ms (191%) | 582.4 us (127%) | 0.4% CPU | 0 |

### `linux/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-21T16:45:40Z` | `de66c0f7` | 3.1 us (102%) | 17.5 us (110%) | 6.8 us (106%) | 1.95 ms (180%) | 709.4 us (116%) | 0.3% CPU | 0 |
| `2026-11-20T21:36:43Z` | `a55326e7` | 3.2 us (101%) | 18.5 us (112%) | 7.0 us (107%) | 6.99 ms (105%) | 1.33 ms (97%) | 0.3% CPU | 0 |
| `2026-11-20T16:44:58Z` | `11473661` | 3.2 us (102%) | 17.1 us (109%) | 7.1 us (105%) | 2.13 ms (180%) | 645.4 us (115%) | 0.3% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 3.2 us (102%) | 18.8 us (112%) | 6.6 us (106%) | 2.07 ms (177%) | 759.4 us (114%) | 0.3% CPU | 0 |

### `windows/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-21T16:45:40Z` | `de66c0f7` | 425 ns (106%) | 35.4 us (105%) | 32.0 us (118%) | 5.94 ms (114%) | 4.07 ms (81%) | 1.6% CPU | 0 |
| `2026-11-20T21:36:43Z` | `a55326e7` | 520 ns (95%) | 46.8 us (114%) | 42.7 us (113%) | 8.16 ms (140%) | 5.37 ms (74%) | 1.6% CPU | 0 |
| `2026-11-20T16:44:58Z` | `11473661` | 574 ns (94%) | 85.0 us (110%) | 72.4 us (117%) | 12.06 ms (131%) | 8.24 ms (78%) | 1.5% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 561 ns (95%) | 80.8 us (117%) | 69.5 us (113%) | 10.74 ms (135%) | 7.31 ms (75%) | 0.8% CPU | 0 |

### `windows/amd64` (`whpx`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-21T16:45:40Z` | `de66c0f7` | 11.5 us (107%) | 68.8 us (163%) | 64.0 us (177%) | 959.6 us (210%) | 1.08 ms (123%) | 0.0% CPU | 0 |
| `2026-11-20T21:36:43Z` | `a55326e7` | 11.7 us (102%) | 89.2 us (171%) | 82.2 us (189%) | 1.16 ms (223%) | 1.17 ms (142%) | 0.0% CPU | 0 |
| `2026-11-20T16:44:58Z` | `11473661` | 16.5 us (99%) | 158.3 us (169%) | 145.0 us (184%) | 1.75 ms (237%) | 1.85 ms (132%) | 0.0% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 16.5 us (103%) | 158.4 us (189%) | 150.5 us (186%) | 1.75 ms (213%) | 1.67 ms (130%) | 0.0% CPU | 0 |

### `windows/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-21T16:45:40Z` | `de66c0f7` | 952 ns (86%) | 30.5 us (120%) | 27.6 us (104%) | 16.98 ms (37%) | 17.84 ms (19%) | 1.6% CPU | 0 |
| `2026-11-20T21:36:43Z` | `a55326e7` | 990 ns (82%) | 34.0 us (94%) | 28.5 us (106%) | 18.68 ms (41%) | 14.56 ms (31%) | 1.6% CPU | 0 |
| `2026-11-20T16:44:58Z` | `11473661` | 999 ns (83%) | 34.0 us (105%) | 28.7 us (109%) | 16.22 ms (40%) | 22.90 ms (17%) | 1.6% CPU | 0 |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 973 ns (89%) | 34.2 us (97%) | 31.2 us (105%) | 18.81 ms (36%) | 17.70 ms (25%) | 0.0% CPU | 0 |

