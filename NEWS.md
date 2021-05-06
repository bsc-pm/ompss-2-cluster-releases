# OmpSs-2 Release Notes
All notable changes to the OmpSs-2@Clusters programming model, the
Nanos6 runtime system, the Mercurium source-to-source compiler will be
documented in this file.


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


