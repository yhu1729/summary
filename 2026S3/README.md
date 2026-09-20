# 2026S3

## ChatGPT (July 2026)

### Summary

Relativistic particle-in-cell simulations require particle pushers that accurately integrate charged-particle trajectories in electromagnetic fields. This paper compares explicit relativistic pushers---including Boris, Vay, Higuera--Cary, exact-rotation, and proper-time schemes---against an implicit midpoint benchmark across homogeneous, spatially varying, time-dependent, and plane-wave fields. No method dominates every test. Higuera--Cary is consistently competitive among explicit schemes and substantially improves the scenario for which it was designed. Proper-time methods can be exact in constant fields but may lose order in inhomogeneous or time-dependent fields and are sensitive to root-solver tolerances. The implicit midpoint method often preserves invariants to machine precision but costs more and is not uniformly best. The paper identifies volume-preserving Boris-like maps and applies symmetric Yoshida compositions to construct arbitrary even-order variants. Fourth-order versions converge faster and reduce errors when physical timescales are resolved, but they do not rescue under-resolved steps. The study excludes field-grid and interpolation errors and does not benchmark computational cost.

### Contributions

1. Compared a broad set of relativistic explicit particle pushers across six representative electromagnetic-field tests.
2. Identified Higuera--Cary as a consistently competitive general-purpose explicit alternative to Boris.
3. Showed that proper-time schemes can lose second-order accuracy and depend strongly on nonlinear-solver tolerances.
4. Derived arbitrary even-order, volume-preserving extensions of Boris-like pushers using symmetric Yoshida compositions.
5. Demonstrated fourth-order convergence while showing that higher order cannot compensate for unresolved physical timescales.
