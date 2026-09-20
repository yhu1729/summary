# 2026GHJ

## ChatGPT (July 2026)

### Summary

BEACONS treats neural PDE surrogates as numerical methods that should carry explicit error guarantees. For homogeneous first-order hyperbolic conservation laws, the method of characteristics predicts solution smoothness and shock formation; combined with shallow-network approximation theory, this yields worst-case $L^\infty$ bounds that extend beyond the training interval. To handle discontinuities, the framework decomposes a solution into simpler functions and composes separately trained shallow networks. Its key inequality bounds composition error by $e_f+Le_g$, allowing a smooth outer function with Lipschitz constant $L$ to suppress error from a discontinuous inner approximation. A Racket domain-specific language specifies PDEs and architectures, generates C code for training and inference, and produces executable proof certificates through IEEE-754-aware symbolic rewriting. Deterministic tests train on the first third of simulations and extrapolate through the remainder for one- and two-dimensional advection, inviscid Burgers, and compressible Euler problems. Against equal-sized fully connected networks, BEACONS generally better preserves waves and conserved quantities, has lower $L^2$ and $L^\infty$ errors, and stays within its certified worst-case bounds. The evidence is limited to selected benchmarks; moreover, Euler certificates are conditional because their reference solver is not formally verified, unlike the advection and Burgers solvers.

### Contributions

1. Combined characteristic analysis with neural approximation theory to derive extrapolatory worst-case $L^\infty$ bounds for hyperbolic PDE solutions.
2. Established an algebraic composition rule that propagates layerwise approximation errors and motivates bounded-error deep architectures for discontinuous solutions.
3. Implemented a Racket-based specification, C code-generation, training, and validation pipeline for BEACONS solvers.
4. Generated machine-checkable error certificates using a terminating symbolic rewrite system designed to respect IEEE-754 floating-point algebra.
5. Demonstrated improved extrapolation, conservation, and error behavior over equal-sized fully connected networks on one- and two-dimensional advection, Burgers, and Euler benchmarks.
