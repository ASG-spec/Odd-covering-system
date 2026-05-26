# Structural Obstruction of Odd Covering Systems in the 3^infinity * 5 * p Tower

This repository contains the computational and analytic verification for the paper "Structural Obstruction of Odd Covering Systems in the 3^infinity * 5 * p Tower."

## The Theorem
We definitively prove that no odd covering system exists within the infinite moduli tower 3^infinity * 5 * p for all primes p >= 7. 

This is achieved by isolating the infinite 3-adic tail from the finite core and establishing a rigorous algebraic crossover point:

1. **The Tail Threshold:** Bounding the infinite tail mathematically to establish a maximum reciprocal mass limit M_p = (p+1)/(45p).
2. **CRT Core Decomposition:** Decomposing the core modulus N_p = 135p via the Chinese Remainder Theorem to isolate the base modulus Z/135Z from the p-dependent divisors.
3. **The Base Floor (Lemma 1):** Utilizing a deterministic Sum-of-Maxima strict union bound on Z/135Z to certify a base uncovered minimum of Z_135 = 43.
4. **The Penalty Bound (Lemma 2):** Algebraically proving the maximum coverage penalty of all p-dependent mixed divisors is bounded by a constant K = 105.
5. **The Analytic Crossover:** Combining these bounds to prove that the density of uncovered residues strictly exceeds the infinite tail threshold for all primes p > 3.775.

Since the analytic crossover threshold (3.775) strictly precedes the lowest valid prime in the sequence (p = 7), the entire infinite family is obstructed analytically. No piecemeal computational gap-filling is required.

## Reproducing the Verification

The script `analytic_proof.py` executes the 1,215-branch baseline sweep to certify Lemma 1 (Z_135 = 43), computes the penalty constant K, and algebraically derives the crossover threshold P. The entire verification runs in under **0.05 seconds** on a standard modern CPU.

### Requirements
* Python 3.10+
* `numpy >= 1.24`

### Execution
Run the verification script from your terminal:
```bash
python analytic_proof.py
