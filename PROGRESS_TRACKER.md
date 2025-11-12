# 🧮 Discrete Differential Geometry Exercises — Progress Tracker

A working checklist for completing the CMU 15-458/858 Discrete Differential Geometry programming assignments using this C++ framework.

## 📋 Assignment Overview

| Assignment | Directory | Focus | Status | Progress |
|------------|-----------|-------|--------|----------|
| 0 | `projects/simplicial-complex-operators` | Combinatorial surfaces & simplicial operators | ⏳ Pending | 0% |
| 1 | `projects/discrete-exterior-calculus` | Hodge stars & exterior derivatives | ⏳ Pending | 0% |
| 2 | `projects/discrete-curvatures-and-normals` | Curvature and normal estimates | ⏳ Pending | 0% |
| 3A | `projects/geometric-flow` | Laplacian-based flows | ⏳ Pending | 0% |
| 3B | `projects/poisson-problem` | Scalar Poisson solve | ⏳ Pending | 0% |
| 4 | `projects/parameterization` | Conformal parameterization | ⏳ Pending | 0% |
| 5 | `projects/geodesic-distance` | Heat-method geodesics | ⏳ Pending | 0% |
| 6A | `projects/vector-field-decomposition` | Tree-cotree & Hodge bases | ⏳ Pending | 0% |
| 6B | `projects/direction-field-design` | Trivial connections (optional) | ⏳ Pending | 0% |

> **Build tip:** Each project expects an out-of-source build (`mkdir build && cd build && cmake .. && make`) and runs from `bin/main`. Unit tests are co-compiled per assignment (see sections below).

---

## 🧱 Assignment 0: Combinatorial Surfaces

**Goal:** Implement simplicial complex operators for mesh subsets.

**Directory:** `projects/simplicial-complex-operators`

**Tasks**
- [ ] Implement `assignElementIndices` through `boundary` in `src/simplicial-complex-operators.cpp`.
- [ ] Validate GUI actions (star, closure, link, boundary) respond correctly.
- [ ] Run unit tests: `bin/test-sco`.

**Deliverables**
- [ ] Working simplicial operator implementations.
- [ ] Screenshots or notes verifying GUI operators.

---

## 📐 Assignment 1: Exterior Calculus

**Goal:** Assemble discrete Hodge star and exterior derivative operators.

**Directory:** `projects/discrete-exterior-calculus`

**Tasks**
- [ ] Implement `cotan` and `barycentricDualArea` in `core/src/geometry.cpp`.
- [ ] Build Hodge stars and exterior derivatives in `src/discrete-exterior-calculus.cpp`.
- [ ] Run unit tests: `bin/test-dec`.

**Deliverables**
- [ ] Validated DEC operators.
- [ ] Notes on numerical stability or conditioning observations.

---

## 🎯 Assignment 2: Investigating Curvature

**Goal:** Compute discrete curvature and vertex normals with multiple weighting schemes.

**Directory:** `projects/discrete-curvatures-and-normals`

**Tasks**
- [ ] Implement angle/dihedral/normal and curvature routines in `core/src/geometry.cpp`.
- [ ] Compare visualization toggles for various normal estimators.
- [ ] Run unit tests: `bin/test-curv`.

**Deliverables**
- [ ] Curvature/normal implementation notes.
- [ ] Visual comparisons (screenshots or log).

---

## 🌊 Assignment 3A: Geometric Flow

**Goal:** Evolve meshes via mean curvature flow variants.

**Directory:** `projects/geometric-flow`

**Tasks**
- [ ] Implement `laplaceMatrix` and `massMatrix` in `core/src/geometry.cpp`.
- [ ] Complete `buildFlowOperator` and `integrate` in `src/mean-curvature-flow.cpp`.
- [ ] Finish constructor and `buildFlowOperator` in `src/modified-mean-curvature-flow.cpp`.
- [ ] Run unit tests: `bin/test-flow`.

**Deliverables**
- [ ] Flow implementation with notes on stability (timestep settings, damping).
- [ ] Before/after mesh captures for both flow variants.

---

## 🔥 Assignment 3B: Scalar Poisson Problem

**Goal:** Solve Poisson equations with user-defined vertex densities.

**Directory:** `projects/poisson-problem`

**Tasks**
- [ ] Reuse/verify `laplaceMatrix` and `massMatrix` in `core/src/geometry.cpp`.
- [ ] Implement constructor and `solve` in `src/scalar-poisson-problem.cpp`.
- [ ] Validate vertex selection UI and density inputs.

**Deliverables**
- [ ] Working Poisson solver with sample configurations.
- [ ] Observations on boundary handling and solution smoothness.

---

## 🗺️ Assignment 4: Conformal Parameterization

**Goal:** Flatten meshes via spectral conformal parameterization.

**Directory:** `projects/parameterization`

**Tasks**
- [ ] Build `complexLaplaceMatrix` in `core/src/geometry.cpp`.
- [ ] Implement `buildConformalEnergy` and `flatten` in `src/spectral-conformal-parameterization.cpp`.
- [ ] Complete iterative solver utilities in `src/solvers.cpp` (`solveInversePowerMethod`, `residual`).
- [ ] Run unit tests: `bin/test-param`.

**Deliverables**
- [ ] Flattened mesh visuals and distortion analysis.
- [ ] Notes on solver convergence (iterations, tolerance).

---

## 🧭 Assignment 5: Geodesic Distance

**Goal:** Compute geodesic distances using the heat method.

**Directory:** `projects/geodesic-distance`

**Tasks**
- [ ] Implement constructor, `computeVectorField`, `computeDivergence`, and `compute` in `src/heat-method.cpp`.
- [ ] Test vertex selection workflow in the GUI.
- [ ] Run unit tests: `bin/test-heat`.

**Deliverables**
- [ ] Heat method implementation with timing/accuracy notes.
- [ ] Visualizations of distance isolines or color maps.

---

## 🌐 Assignment 6A: Vector Field Decomposition

**Goal:** Build tree-cotree structures and harmonic bases for vector fields.

**Directory:** `projects/vector-field-decomposition`

**Tasks**
- [ ] Implement spanning tree/cotree and generator routines in `src/tree-cotree.cpp`.
- [ ] Complete harmonic basis workflow in `src/harmonic-bases.cpp`.
- [ ] Optionally, implement Hodge decomposition in `src/hodge-decomposition.cpp`.
- [ ] Run unit tests: `bin/test-decomp`.

**Deliverables**
- [ ] Verified harmonic basis construction.
- [ ] Notes comparing decomposition modes (exact, co-exact, harmonic).

---

## 🧭 Assignment 6B: Direction Field Design (Optional)

**Goal:** Construct trivial connections on topological spheres.

**Directory:** `projects/direction-field-design`

**Tasks**
- [ ] Implement constructor and core routines (`buildPeriodMatrix`, `computeCoExactComponent`, `computeHarmonicComponent`, `computeConnections`) in `src/trivial-connections.cpp`.
- [ ] Experiment with singularity placement via GUI controls.
- [ ] Run unit tests: `bin/test-connect`.

**Deliverables**
- [ ] Direction field designs with screenshots for various singularity layouts.
- [ ] Notes on period matrix conditioning vs. mesh quality.

---

## 🚀 Project Portfolio & Next Steps

- [ ] Maintain build notes (compiler flags, dependencies) for each platform tested.
- [ ] Capture benchmarking data (runtime, iterations) for each solver.
- [ ] Summarize theoretical insights per assignment in `docs/` or a personal journal.
- [ ] Consider extending solvers (e.g., alternate boundary conditions, anisotropic weights).

**Overall Progress:** 0/9 tracked assignments completed  
**Current Focus:** Assignment 0 — Combinatorial Surfaces  
**Next Milestone:** Finish simplicial complex operators and validate with `bin/test-sco`

---

*Update this tracker as you complete tasks and discover insights. Happy geometry processing!*

