# 2026BDFR

## ChatGPT (July 2026)

### Summary

This paper analyzes iterated Golub--Kahan--Tikhonov regularization for large linear inverse problems obtained by discretizing ill-posed Hilbert-space operator equations. Partial Golub--Kahan bidiagonalization projects the problem into a small Krylov subspace, where iterated Tikhonov regularization is applied. The analysis simultaneously tracks data noise, operator discretization, and projection error. Under source conditions and balanced projection and data errors, it obtains $O(\delta^{2i/(2i+1)})$ convergence, improving the $O(\delta^{2/3})$ saturation of ordinary Tikhonov as the iteration count $i$ increases. Dominant work remains Golub--Kahan matrix-vector products and is essentially independent of $i$. Two regularization-parameter strategies are given, including an alternative permitting smaller Krylov spaces. Deblurring and tomography experiments show gains over non-iterated Golub--Kahan--Tikhonov and, for nonsymmetric cases, iterated Arnoldi--Tikhonov.

### Contributions

1. Defined iterated Tikhonov regularization on a partial Golub--Kahan reduction.
2. Jointly analyzed noise, discretization, Krylov-projection, and regularization errors.
3. Proved convergence rates up to $O(\delta^{2i/(2i+1)})$ under the stated assumptions.
4. Developed two parameter-selection rules, including one that can use a smaller Krylov subspace.
5. Demonstrated improved image-restoration and rectangular-tomography results against non-iterated and Arnoldi-based alternatives.
