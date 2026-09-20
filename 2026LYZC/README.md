# 2026LYZC

## ChatGPT (July 2026)

### Summary

This article models imperfect sliding electrical contact in railgun electromagnetic simulations without meshing the thin contact layer directly. The contact zone between armature and rail is replaced by a zero-thickness interface whose strongly discontinuous boundary conditions encode contact resistance, preload pressure, and liquid aluminum effects. An interior-penalty discontinuous Galerkin framework then modifies numerical fluxes so the discontinuous interface conditions are enforced while preserving favorable conditioning even for extreme contact conductivities. Comparisons with a classical contact-layer model show consistent current-density results, while the boundary-condition model uses far fewer elements and less computation; the reported element count is one-seventeenth of the classical model in a representative comparison. The method is then used to study velocities of 0, 100, 500, and 1000 m/s. Increasing speed shifts current concentration differently on rail and armature sides, highlighting asymmetric electromagnetic effects of preload pressure and imperfect contact.

### Contributions

1. Replaced the thin armature-rail contact layer with a zero-thickness strongly discontinuous interface model.
2. Derived interface conditions that encode contact resistance, pressure, and liquid aluminum material effects.
3. Built an IPDG discretization whose numerical fluxes enforce the discontinuous interface conditions.
4. Verified agreement with the classical contact-layer model at much lower mesh and runtime cost.
5. Analyzed velocity-dependent current-density concentration on rail and armature contact surfaces.
