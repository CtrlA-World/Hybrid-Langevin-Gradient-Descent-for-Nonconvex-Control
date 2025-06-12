# Hybrid-Langevin-Gradient-Descent-for-Nonconvex-Control
This repository is in reference to the "Hybrid Langevin-Gradient Descent for Nonconvex Control" paper I wrote as a final project for EE546 course in Spring 2025. You can find all the source codes, codes I wrote, and the benchmark for all the material included in the paper. 

**Key Implementation Details**  
- **Hybrid GD-LMC Algorithm**:  
  - Combines GD (deterministic gradient steps) and LMC (stochastic noise injection) into a **single unified method** .  
  - Noise schedule: `σₜ = σ₀e^{-λt}` (Eq. 3 in paper) ensures:  
    - High noise early (`σₜ > 0.5` for `t < 50`) → Exploration (LMC-like).  
    - Low noise later (`σₜ < 0.01` for `t ≥ 200`) → Convergence (GD-like).  
- **Benchmarks**: Compares pure GD, pure LMC, and the hybrid method (Table 1/Fig. 1).  

For questions or issues, contact csaried@uw.edu.

