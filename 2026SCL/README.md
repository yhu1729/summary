# 2026SCL

## ChatGPT (July 2026)

### Summary

This paper develops a mass-lumping technique that enables fully explicit time integration for the shifted-basis extended finite element method (SBXFEM) in three-dimensional dynamic fracture simulations. SBXFEM avoids blending elements, but its enriched degrees of freedom create coupled mass matrices and conditioning issues that complicate explicit dynamics. The authors introduce a mass-scaling factor for the enriched mass-matrix contribution, derive an approximate critical time step, and analyze the resulting kinetic-energy error. At the single cracked-element level the scaling factor matters, but its influence becomes negligible when cracked elements are a small fraction of a larger structure. The method is implemented as an Abaqus Explicit VUEL and tested on 1D and 3D benchmarks, including Mode I and Mode II ductile crack propagation under large deformation. Comparisons with implicit and native Abaqus references show credible fracture behavior with lower computation time, while future work targets self-heating, micro-inertia, cohesive-phase refinements, and contact.

### Contributions

1. Proposed enriched-mass scaling for explicit SBXFEM dynamics in cracked 3D elements.
2. Derived kinetic-energy error and critical-time-step behavior for the lumped enriched mass matrix.
3. Implemented the approach as an Abaqus Explicit user element.
4. Validated the method on increasingly complex dynamic fracture benchmarks.
5. Showed that enriched-mass errors diminish for large structures with few crack-containing elements.
