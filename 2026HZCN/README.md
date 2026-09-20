# 2026HZCN

## ChatGPT (July 2026)

### Summary

The paper develops a cell-centered curvilinear Lagrangian discontinuous Galerkin method for two-dimensional resistive magnetohydrodynamics. An implicit-explicit time integrator advances hydrodynamic advection explicitly and magnetic diffusion implicitly. Conservative variables use Taylor bases on reference elements, while a locally divergence-free magnetic basis is carried to curved physical cells by a Piola transformation. A multidimensional approximate Riemann solver supplies nodal velocities and forces, and basis-function deformation moves the curvilinear mesh with the material. Tests include Taylor--Green flow, MHD wave families, smooth and discontinuous-resistivity diffusion, coupled advection--diffusion, a rotor, and a magnetized blast. Smooth problems approach third-order accuracy, discontinuous tests capture the expected field and electric-field structure, and curved cells remain robust under severe rotor deformation. Oscillations persist near a slow shock, and a deliberately non-solenoidal diffusion test requires relaxing the divergence-free representation. The method is limited to two dimensions, with three-dimensional bases and hexahedral meshes left for future work; robustness is demonstrated numerically without a complete stability proof.

### Contributions

1. Constructed a curvilinear cell-centered Lagrangian DG scheme for resistive MHD.
2. Split hyperbolic hydrodynamics and magnetic diffusion in an IMEX integrator.
3. Preserved element-local $\nabla\cdot\mathbf{B}=0$ through divergence-free bases and Piola mapping.
4. Combined moving curved meshes, Taylor bases, nodal Riemann solving, and limiting.
5. Demonstrated high-order accuracy and robustness across smooth and shock-dominated tests.
