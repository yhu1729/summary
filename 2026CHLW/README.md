# 2026CHLW

## ChatGPT (July 2026)

### Summary

COS(DG) is a compact, nonintrusive oscillation-control wrapper for high-order DG discretizations of hyperbolic conservation laws. Once per time step, it convexly blends each DG polynomial with its cell average using entropy-induced distances that are locally scale- and evolution-invariant. The method needs only immediate neighbors, no derivatives or characteristic decomposition, and works identically for modal and nodal formulations on general meshes. Analysis proves optimal convergence for smooth solutions, $L^2$ nonexpansiveness, and inheritance of entropy stability from an entropy-stable base scheme; a finite convex covering argument supports problem-independent oscillation suppression. A symmetry-preserving entropy sensor localizes the operation, and convex scaling integrates naturally with the Zhang-Shu bound-preserving limiter. Extensive one- and two-dimensional advection, Burgers, and Euler benchmarks, including comparisons with nine TVB-, WENO-, MP-, OFDG-, and OEDG-type approaches, show robust shock capture, fine-structure resolution, scale-independent parameter behavior, and low overhead.

### Contributions

1. Introduced a characteristic-free, entropy-guided convex oscillation-suppression framework for arbitrary-order DG methods.
2. Proved optimal accuracy, $L^2$ nonexpansiveness, and inherited entropy stability.
3. Established local scale and evolution invariance with problem-independent suppression guarantees.
4. Added a symmetry-preserving entropy criterion and unified Zhang-Shu bound preservation.
5. Demonstrated high resolution and robustness against nine established controls on scalar and Euler shock problems.
