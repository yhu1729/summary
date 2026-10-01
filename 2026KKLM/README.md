# 2026KKLM

## Claude (September 2026)

### Summary

The authors solve the fixed-boundary Grad–Shafranov (GS) equation for tokamak equilibria with physics-informed Kolmogorov–Arnold networks (KANs), which place learnable univariate functions on network edges, here FastKANs built from Gaussian radial basis functions. The loss combines the GS residual at about 500 interior collocation points with a Dirichlet penalty at about 390 boundary points of an ITER-like lower single-null shape, and training uses AdamW followed by the self-scaled Broyden (SSBroyden) quasi-Newton method. The profile amplitudes $(P_1,H_1)$ are updated in alternation with the network to meet target toroidal beta and plasma current, and the magnetic axis is tracked by damped Newton iterations. For linear Solov'ev profiles, KANs and parameter-matched multilayer perceptrons (MLPs) reach comparable losses, the MLPs faster, and a KAN reproduces an analytic single-null solution with relative error below $10^{-3}$ in the core. For nonlinear L-mode profiles, only KANs with guided training converge: homotopy continuation from Solov'ev profiles in all cases, and transfer learning from a pretrained Solov'ev network when the amplitudes are fixed. For an H-mode pressure-pedestal profile, different training strategies converge to distinct equilibria, indicating multiple solution branches. The authors note that MLPs with tuned hyperparameters might outperform KANs.

### Contributions

1. Combined FastKANs, SSBroyden refinement, and guided training into a mesh-free GS solver that identifies $(P_1,H_1)$ from beta and current constraints, with an alternative constraint on the on-axis safety factor from an analytic formula.
2. Introduced a homotopy curriculum that blends the Solov'ev and target profile derivatives $dP/d\psi$ and $dH/d\psi$, which converged in every nonlinear case considered and needs no stored pretrained network.
3. Built a collocation point generator for data-prescribed boundaries using Fourier-fitted boundary parametrizations, k-d-tree removal of clusters, potential-based void filling, and X-point refinement.
4. Constructed pedestal equilibria with edge current peaks and negative edge magnetic shear, finding that homotopy and transfer learning with parameter discovery reach similar beta and current but different $H_1$ and on-axis safety factor, and that unguided training with frozen amplitudes converges to a flatter-pressure branch.
5. Gave parameter-count formulas for FastKANs and MLPs to match model sizes and an ablation showing that unguided training and MLPs fail for the nonlinear L-mode profiles, whereas MLPs with frozen pedestal amplitudes converge toward the unguided branch.

### Comments

- Section 3.2, Eq. (17): the outer sum of the Kolmogorov–Arnold representation of $f(x_1,\ldots,x_d)$ runs to $2n+1$, but $n$ is not defined there; the representation for $d$ variables evidently intends $2d+1$.
- Section 5.1.2, Table 3 and Fig. 7: Table 3 gives the Solov'ev FastKAN runtime as "01m 50s", while the Fig. 7 legend for the same comparison reads "FastKAN (L:2, N:16) runtime: 01m 36s" (the MLP runtimes agree in both); which value is correct is unresolved.
- Section 5.1.3, Fig. 9: Section 5.1.1 states that the hyperparameters "used in this and subsequent experiments are summarized in Table 1", where the initial AdamW learning rate is $5\times10^{-4}$, but the Fig. 9 title reads "MLP lrs: [5e-03, 5e-01] | FastKAN lrs: [5e-03, 5e-01]"; unresolved.
- Section 5.2, text after Eq. (41): the integration constants are said to follow from "the boundary requirements at the plasma edge, $P(\psi=\psi_a)=0$ and $F(\psi=\psi_a)=\sqrt{2H(\psi=\psi_a)}=1$", but Eq. (7) defines $\psi_a$ as the flux on the magnetic axis, where Eq. (38) gives $P=P_0\neq0$; Eqs. (40)–(41) follow from these conditions at the boundary $\psi=\psi_b$ ($\psi_n=1$), the evident intended reading.
- Section 5.3, Table 5 (Case B): the text says the frozen $P_1$ and $H_1$ "are set to the values identified by the homotopy method", $(0.354, 0.109)$, as listed in every other Case B row, but the MLP$_2$ row lists $(0.355, 0.110)$.
