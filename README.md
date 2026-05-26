# Structural Obstruction of Odd Covering Systems in the 3^a * 5 * 7 Tower

This repository contains the computational verification for the paper "Structural Obstruction of Odd Covering Systems in the 3^a * 5 * 7 Tower."

## The Theorem
We prove that no covering system exists within the infinite moduli tower 3^infinity * 5 * 7. This is achieved by:
1. Bounding the infinite 3-adic tail theoretically (maximum reciprocal mass M = 24/945).
2. Utilizing a deterministic Sum-of-Maxima strict union bound on the finite core L_3 = 945.

*Note: This result is certified specifically for the 3^a * 5 * 7 tower (N = 945). Generalization to all p >= 7 remains an open problem; see Section 5.1 of the paper.*

The script `core_density_lb.py` executes this exhaustive sweep, certifying that the absolute worst-case residue configuration leaves at least 179 residues uncovered. Since 179 >> 24, the coverage is mathematically impossible.

## Reproducing the Verification

The exhaustive sweep over the 8,505 independent, symmetry-reduced branches takes approximately **0.74 seconds** on a standard modern CPU.

### Requirements
* Python 3.10+
* `numpy >= 1.24`

### Execution
Run the verification script from your terminal:
```bash
python core_density_lb.py
