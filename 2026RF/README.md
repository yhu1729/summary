# 2026RF

## ChatGPT (July 2026)

### Summary

This paper gives a mathematical foundation for Boltzmann generators, which use invertible normalizing flows to map an easy reference distribution to a molecular Boltzmann distribution. Physical Coulomb and Lennard--Jones singularities make the target density vanish at atomic collisions, outside standard smooth-transport assumptions. The authors regularize these densities, extend the Moser transport construction to positive low-regularity endpoint densities, and show that its map is invertible and bilipschitz. Sobolev approximation results then provide invertible RealNVP networks whose push-forward measures converge narrowly and, on bounded configuration domains, approach the target arbitrarily closely in Wasserstein-$2$ distance. A two-dimensional double-well experiment reports joint $W_2=0.0993$ and reproduces the observed metastable switching count. An alanine-dipeptide experiment learns the principal $\Phi$--$\Psi$ conformational basins from 60 ns of molecular-dynamics data and reports a $9.21^\circ$ Wasserstein distance. The analysis proves existence and expressivity rather than training convergence; controlling inverse-map conditioning through a bias toward Moser-like transports remains open.

### Contributions

1. Extended Moser transport maps to low-regularity densities relevant to singular molecular interactions.
2. Proved existence of invertible bilipschitz transports between regularized reference and Boltzmann measures.
3. Established Sobolev approximation of these maps by invertible RealNVP networks.
4. Derived arbitrarily accurate Wasserstein-$2$ approximation for molecular Boltzmann distributions on bounded domains.
5. Validated equilibrium and metastable behavior on a double well and alanine dipeptide.
