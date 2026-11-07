---
layout: archive
title: "Research"
hide_title: true
permalink: /research/
author_profile: true
---

High-precision Analog Accelerators for High Performance Computing
------

<!-- Analog crossbars compute matrix-vector products directly inside memory, which promises large speed and energy gains for the sparse iterative solvers behind scientific computing. But analog hardware is noisy and low-precision, and small errors can build up until a solver never converges. I work on getting high precision out of low-precision analog hardware, without giving up its speed and energy advantages.

- **High precision from low-precision hardware:** ARIT uses the Residue Number System to split each value across independent low-bit channels, then rebuilds the result with the Chinese Remainder Theorem. Ten 8-bit channels give a 79-bit range, and all 20 sparse test systems converge, up from 12 at 32-bit.
- **Speed and energy:** In modeling of SONOS crossbars at 45 nm, ARIT runs SpMV 16× (CG) and 8.6× (BiCGStab) faster than an NVIDIA A100, with 7.9× and 23.5× better energy (geometric means).
- **Where analog meets digital:** Fully analog modulo reduction doubles any error at every bit slice, and solvers stop converging under device noise. Digitizing each slice stops that build-up and restores convergence.
- **Fitting sparse matrices on crossbars:** Row-column reordering cuts the hardware needed (thermomech_TC drops from 209,263 to 2,317 blocks), and all of the SpMV stays on the crossbars with no GPU fallback. -->

<!-- Accelerating Graph Workloads using software-hardware co-design
------

Real-world graphs are huge and irregular, so the work has to be spread across thousands of cores. In traditional bulk-synchronous programs, those cores repeatedly stop to synchronize, and communication takes over more of the runtime as core counts climb. We redesign algorithms and communication together, using fine-grained asynchronous messaging (the FA-BSP model and HClib-Actor runtime) to overlap computation with communication.

- **Faster influence maximization:** Our algorithm, Mosaic, shrinks an all-reduce as large as the graph to a single integer. It achieves a 13× end-to-end geometric-mean speedup over the state-of-the-art Ripples on NERSC Perlmutter (3.4× on PACE), scales to 131,072 cores, and matches Ripples' accuracy to within 2%.
- **An alternative to MPI for SpMV:** We built the first distributed SpMV implementations in HClib-Actor. On well-balanced matrices, they run up to 28× faster than PETSc at 64 nodes, with the lead narrowing to 1.1× on the largest matrices.
- **The open problem:** On skewed power-law graphs, a few cores become stragglers and PETSc stays faster, which makes load-balanced partitioning and scheduling the next step. -->
