# 2026HZYZ

## ChatGPT (July 2026)

### Summary

The paper proposes IFNSO, a single-pass polynomial approximation to the orthogonal polar factor intended to replace repeated Newton--Schulz steps in Muon-style optimization. After transposing a tall matrix and scaling it using $\lVert AA^\top\rVert_F^{1/2}$, the method constructs powers of $I-AA^\top/\lVert AA^\top\rVert_F$ whose exponents grow exponentially. Learnable coefficients combine these terms in a polynomial designed to approach one near unit singular values, with the final coefficient constrained from a selected extremum. Repeated squaring generates high powers using short-dimension matrix products, reducing expensive long-dimension products from $N$ to one. With polynomial depth $L=14$, synthetic $128\times\{128,512,1024\}$ tests report orthogonality error $0.040$ and increasingly favorable operation counts as width grows. A small MNIST/Muon experiment reports $98.87\%$ accuracy and the fastest loss convergence among four baselines. Evidence remains preliminary: testing uses one RTX 4050, random small matrices, and MNIST, while oscillations, slower convergence near one, and high cost for very wide matrices remain.

### Contributions

1. Recast repeated Newton--Schulz compositions as one learnable polynomial for approximate polar-factor orthogonalization.
2. Selected exponentially growing polynomial powers to cover a broad singular-value range with relatively few terms.
3. Introduced a constrained coefficient optimization that fixes the terminal coefficient and stabilizes the remaining coefficients.
4. Used one long-dimension Gram product followed by repeated squaring and aggregation in the shorter dimension.
5. Reported lower error and operation counts on synthetic matrices plus slightly higher MNIST accuracy than the tested baselines.
