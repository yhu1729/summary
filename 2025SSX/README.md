# 2025SSX

## ChatGPT (July 2026)

### Summary

Explicitly forming an $n\times n$ kernel matrix costs quadratic time, limiting kernel methods on large datasets. This paper develops subquadratic approximation algorithms that access Gaussian and related kernel matrices through kernel-density-estimation queries instead of individual entries. Its central primitive approximates multiplication by a nonnegative vector with relative $\ell_2$ error and improved dependence on the target error $\varepsilon$. Applying this primitive yields stronger Frobenius-error guarantees for multiplication by nonnegative matrices and faster relative-error approximation of nonnegative quadratic forms. A new noisy power-iteration analysis shows that matrix--vector products need only $\Theta(\varepsilon)$ accuracy to approximate the top eigenvalue and a witnessing vector, reducing the Gaussian method's dependence from about $\varepsilon^{-7.7}$ to $\varepsilon^{-3.2}$. A separate estimator approximates the sum of all kernel entries using $\Theta(\sqrt{n}/\varepsilon^2)$ sampled points, matching a proved sampling lower bound. Strong Exponential Time Hypothesis reductions establish near-quadratic conditional hardness for related mixed-sign, bilinear, and asymmetric-kernel problems, delineating where the positive-vector and symmetric-kernel assumptions matter. The results are primarily theoretical; experiments only validate the noisy power method's error scaling.

### Contributions

1. Improved nonnegative kernel matrix--vector multiplication by more than a factor of $1/\varepsilon$ over the prior bound.
2. Derived matrix--matrix and nonnegative quadratic-form approximations from the new multiplication primitive with stronger relative-error guarantees.
3. Proved that $\Theta(\varepsilon)$ noisy products suffice for power iteration and obtained a substantially faster top-eigenvalue algorithm.
4. Developed a faster kernel-sum estimator whose $\Theta(\sqrt{n}/\varepsilon^2)$ sample count is asymptotically optimal.
5. Established SETH-based near-quadratic lower bounds for mixed-sign and asymmetric variants, clarifying limits of KDE-based acceleration.
