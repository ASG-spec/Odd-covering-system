
## The Theorem
We prove that no covering system exists within the infinite moduli tower $3^{a} \cdot 5 \cdot 7$. This is achieved by:
1. Bounding the infinite 3-adic tail theoretically (maximum reciprocal mass $M = \\frac{24}{945}$).
2. Utilizing a deterministic $\\mathcal{O}(1)$ Sum-of-Maxima strict union bound on the finite core $L_3 = 945$.

The script `core_density_lb.py` executes this exhaustive sweep, certifying that the absolute worst-case residue configuration leaves exactly $179$ residues uncovered. Since $179 \\gg 24$, the coverage is mathematically impossible.

## Reproducing the Verification

The exhaustive sweep over the $8,505$ independent, symmetry-reduced branches takes approximately **0.74 seconds** on a standard modern CPU.

### Requirements
* Python 3.10+
* `numpy >= 1.24`

*(Note: The `scipy` dependency has been removed, as the Strict Union Bound independently and rigorously guarantees the mathematical floor without requiring a fractional-packing Linear Programming relaxation.)*

### Execution
Run the verification script from your terminal: