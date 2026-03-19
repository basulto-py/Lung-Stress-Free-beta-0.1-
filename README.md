
# 🫁 Lung Stress Free (beta 0.1)

**Status:** Exploratory / WIP / Legacy Baseline
**Tech Stack:** `Python, FEniCS / dolfinx, JAX, SciPy, NumPy`

## 📌 Overview

This repository contains early numerical experiments and baseline code focused on solving a complex inverse problem in biomechanics: estimating the **stress-free reference configuration** of hyperelastic lung tissue.

In continuum mechanics, biological tissues are heavily pre-stressed in vivo. Recovering the true zero-stress state is critical for accurate patient-specific modeling and simulation. This "beta" iteration explores traditional numerical approaches using finite element methods (FEM) to translate these complex biomechanical PDEs into computational models, incorporating the effects of poroelasticity and gravitational loading.

## 🔄 The Pivot: Why Differentiable Physics?

This initial implementation serves as the mathematical baseline. Analyzing the computational bottlenecks and complexity of deriving and implementing traditional adjoint methods for this specific inverse problem directly motivated my current research pivot.

The ultimate goal of this project is to transition from classical solvers to **JAX and Differentiable Physics**, allowing for faster, more elegant gradient-based optimization through automatic differentiation.

## 🚀 Roadmap & Next Steps

- [X] **Phase 1 (Beta 0.1):** Baseline mathematical formulation and traditional numerical implementation for estimating the stress-free reference configuration of hyperelastic tissues.
- [ ] **Phase 2 (The Inverse Problem):** Fully formulate and solve the inverse mechanics problem following the robust methodology proposed by Barnafi et al., incorporating advanced regularization and continuous adjoint methods.
- [ ] **Phase 3 (The JAX Pivot):** Refactor the core simulation to integrate **JAX**. Transition the traditional optimization pipeline to **Differentiable Physics** for exact, automatic gradient computation.
- [ ] **Phase 4 (Scaling):** Scale the JAX-based inverse solver to handle full 3D hyperelastic lung tissue meshes derived from medical imaging.

## 📚 References

This project builds upon foundational and state-of-the-art literature in computational biomechanics and inverse elastostatics:

* **The Inverse Problem:** Barnafi, N., et al. (2024). *Inverse displacement algorithms for the recovery of the unloaded configuration of hyperelastic bodies*. (Methodology for iterative recovery of the stress-free state).
* **Poroelastic Framework:** Avilés-Rojas, N., & Hurtado, D. E. (2022). *Whole-lung finite element models for mechanical ventilation and respiratory research applications*. Frontiers in Physiology, 13, 984286.
* **Tissue Homogenization:** Berger, L., et al. (2016). *A poroelastic model coupled to a fluid network with applications in lung modelling*. Int. J. Numer. Meth. Biomed. Engng.
* **Gravitational Loading Physics:** West, J. B., & Matthews, F. L. (1972). *Stresses, strains, and surface pressures in the lung caused by its weight*. Journal of Applied Physiology, 32(3), 332-345.
* **Mechanical Loading Models:** Peyraut, A., & Genet, M. (2024). *A model of mechanical loading of the lungs*. Biomechanics and Modeling in Mechanobiology.
