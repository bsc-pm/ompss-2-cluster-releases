# OmpSs-2 Release Notes
All notable changes to the OmpSs-2@Clusters programming model, the
Nanos6 runtime system, the Mercurium source-to-source compiler will be
documented in this file.

## Version 2022.12, Wed Dec 21, 2022

### General
- Several important performance improvements and bug fixes.
- Integrating the [**DLB**](https://github.com/bsc-pm/dlb/) library for Dynamic Load Balancing with the Nanos6@Cluster runtime [[1]](#1).
- Introducing the ``auto`` and ``none`` clauses permitting productive development of programs with nested tasks [[2]](#2).

### Instrumentation
- Improved STATS instrumentation report enhancing readability.

<a id="1">[1]</a>
Jimmy Aguilar Mena, Omar Shaaban, Victor Lopez, Marta Garcia, Paul Carpenter, Eduard Ayguade, and Jesus Labarta. Transparent load balancing of MPI programs using OmpSs-2@Cluster and DLB. ICPP2022.

<a id="2">[2]</a>
Omar Shaaban, Jimmy Aguilar Mena, Vicenç Beltran, Paul Carpenter, Eduard Ayguade and Jesus Labarta Mancho. Automatic aggregation of subtask accesses for nested OpenMP-style tasks. SBAC-PAD 2022.



## Version 2022.02, Mon Feb 28, 2022
The OmpSs-2@Clusters 2022.02 contains several improvements and fixes.

### General
- Remove over-subscription of leader-thread and fix load imbalance with `task for`.
- `task for` now respects the priority clause.
- Improve communication performance by grouping messages by destination.
- Reduce redundant communications and data transfers.
- Fix multiple leaks of memory in the messages and dependencies.

### Instrumentation
- Fix instrumentation toml variable list parse
- Add instrumentation events for task for

## Version 2021.05, Thu May 06, 2021
The OmpSs-2@Clusters 2021.05 release is the first release diverged from the OmpSs-2 for smp systems..

### General
- new `node` annotation clause to control nodes to offload or other hints.
- Several important performance improvements.
- Fix `wait` clause to control early release.
- Polling services on LeaderThread
- New scheduling infrastructure for clusters.
- Nodes namespaces.
- Fixed compatibility with some older machines and compilers.
- Fixed message size limit issue when dependencies were > 2GB.
- Grouped granular data fetches messages per node.

### Instrumentation
- Optional instrumentation for the dependency system stages.
- New function `nanos6_instrument_event` to create instrumentation
  events from the user code when using instrumentation.


