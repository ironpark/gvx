# Cross-Platform Benchmark Results

This branch records automated cross-platform `TestE2EMicroBench` latency and host CPU utilization results.

## Latest Summary by Platform and Backend

| Target | Backend | Commit | `host_new` | `getpid` | `open_close` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` |
| :--- | :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `linux/amd64` | `systrap` | `ec3d554c` | 2.56 ms | 4.5 us (104%) | 14.8 us (113%) | 26.8 us (113%) | 10.1 us (112%) | 3.45 ms (191%) | 582.4 us (127%) | 0.4% CPU |
| `linux/arm64` | `systrap` | `ec3d554c` | 1.82 ms | 3.2 us (102%) | 10.9 us (109%) | 18.8 us (112%) | 6.6 us (106%) | 2.07 ms (177%) | 759.4 us (114%) | 0.3% CPU |
| `windows/amd64` | `systrap` | `ec3d554c` | 53.41 ms | 561 ns (95%) | 4.9 us (115%) | 80.8 us (117%) | 69.5 us (113%) | 10.74 ms (135%) | 7.31 ms (75%) | 0.8% CPU |
| `windows/amd64` | `whpx` | `ec3d554c` | 12.44 ms | 16.5 us (103%) | 45.4 us (140%) | 158.4 us (189%) | 150.5 us (186%) | 1.75 ms (213%) | 1.67 ms (130%) | 0.0% CPU |
| `windows/arm64` | `systrap` | `ec3d554c` | 96.21 ms | 973 ns (89%) | 5.4 us (109%) | 34.2 us (97%) | 31.2 us (105%) | 18.81 ms (36%) | 17.70 ms (25%) | 0.0% CPU |

## Historical Trend (Last 10 Runs per Target)

### `linux/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 4.5 us (104%) | 26.8 us (113%) | 10.1 us (112%) | 3.45 ms (191%) | 582.4 us (127%) | 0.4% CPU | 0 |

### `linux/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 3.2 us (102%) | 18.8 us (112%) | 6.6 us (106%) | 2.07 ms (177%) | 759.4 us (114%) | 0.3% CPU | 0 |

### `windows/amd64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 561 ns (95%) | 80.8 us (117%) | 69.5 us (113%) | 10.74 ms (135%) | 7.31 ms (75%) | 0.8% CPU | 0 |

### `windows/amd64` (`whpx`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 16.5 us (103%) | 158.4 us (189%) | 150.5 us (186%) | 1.75 ms (213%) | 1.67 ms (130%) | 0.0% CPU | 0 |

### `windows/arm64` (`systrap`)

| Timestamp (UTC) | Commit | `getpid` | `pipe_pingpong` | `futex_pingpong` | `fork_wait` | `fork_exec_true` | `shm_sparse_idle` | Failures |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `2026-11-20T08:05:37Z` | `ec3d554c` | 973 ns (89%) | 34.2 us (97%) | 31.2 us (105%) | 18.81 ms (36%) | 17.70 ms (25%) | 0.0% CPU | 0 |

