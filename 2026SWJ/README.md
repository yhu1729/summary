# 2026SWJ

## ChatGPT (July 2026)

### Summary

This work introduces the projection enhanced triangular finite element method (PET-FEM) for polygonal meshes. Each polygon is subdivided into triangles, while internal triangle degrees of freedom are recovered from a least-squares polynomial projection of the polygonal degrees of freedom. The construction retains familiar FEM interpolation and avoids problem-dependent stabilization parameters. Higher-order elements use a serendipity-like reduction of internal unknowns and remain less sensitive to distortion than classical serendipity FEM. For first-order analysis, the authors also combine PET-FEM with virtual-element stabilization to produce the VPF-12 element and examine under-integrated variants. Polynomial reproduction and Poisson tests attain the expected optimal convergence rates. Linear and nonlinear structural benchmarks--including patch tests, thin-beam bending, Cook's membrane, and punch loading--show robust behavior on regular and Voronoi meshes. Under-integrated PET-FEM reduces shear locking without hourglass modes, while VPF-12 gives accurate nearly incompressible results on coarse meshes and converges in cases where conventional triangular FEM or VEM variants fail.

### Contributions

1. Defined polygonal PET-FEM through triangular submeshes and least-squares recovery.
2. Extended the construction to higher order with serendipity-style internal moments.
3. Improved robustness to polygon distortion compared with classical serendipity elements.
4. Introduced the locking-resistant VPF-12 hybrid for nearly incompressible materials.
5. Established optimal Poisson convergence and robust nonlinear structural performance.
