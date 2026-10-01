# 2024SV

## ChatGPT (July 2026)

### Summary

Runge--Kutta methods commute with affine changes of variables, but applications such as Lie--Poisson reduction use quadratic maps and seek to evolve only the reduced variables. This paper characterizes when a Runge--Kutta discretization of a quadratic-projectable vector field descends to a closed method in those projected variables. Algebraic conditions on the Butcher coefficients eliminate cross-stage quadratic terms. The main theorem proves that the nontrivial methods satisfying these conditions and symplecticity are precisely symplectic diagonally implicit Runge--Kutta (SyDIRK) methods, up to stage permutation. The descended schemes are generally not Runge--Kutta methods themselves. Higher than second order requires at least one negative composition coefficient. The framework recovers matrix Lie--Poisson and isospectral integrators, extends through Jordan operator algebras and momentum maps, and also applies to nonconservative dynamics. For the Navier--Stokes--Zeitlin system, the resulting method dissipates energy and enstrophy monotonically up to $O(h^3)$ when its weights are nonnegative, while preserving enstrophy exactly in the inviscid case.

### Contributions

1. Defined algebraic conditions under which Runge--Kutta stages project through quadratic transformations.
2. Proved that quadratic-projectable symplectic Runge--Kutta methods are exactly SyDIRK methods up to stage ordering.
3. Derived closed integration formulas expressed entirely in the projected variables.
4. Connected the construction to matrix Lie--Poisson, isospectral, Jordan-algebra, and momentum-map reductions.
5. Established dissipation and exact inviscid enstrophy preservation for a Navier--Stokes--Zeitlin application.
