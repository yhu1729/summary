# 2026BB2

## Claude (September 2026)

### Summary

The multirate PDE technique simulates radio-frequency (RF) circuits by lifting the circuit differential-algebraic equation (DAE) to a PDE in a slow envelope time $\tau$ and a $2\pi$-periodic fast variable $\hat t$, whose solution along a characteristic curve recovers the DAE solution. Distributed devices such as transmission lines and filters are characterized instead by impulse responses $h$ or transfer functions $H$, which add a convolution integral to the DAE. The authors extend the multirate PDE to such integro-differential algebraic equations through a bivariate convolution, acyclic in $\tau$ and cyclic in $\hat t$, with a multivariate impulse response $\hat h(\tau,\hat t)$. Requiring the DAE and PDE solutions to coincide along the characteristics yields pointwise equalities for $\hat h$. For a constant carrier frequency $\omega_0$, $\hat h(\tau,\hat t)=h(\tau)\,\delta(\hat t-\omega_0\tau)$ satisfies them, so the convolution runs along the characteristics. A Fourier series in $\hat t$ turns it into convolutions of each envelope $\hat x_k$ with the modulated impulse response $h(\tau)e^{-jk\omega_0\tau}$, whose transform $H(\omega+k\omega_0)$ is lowpass and can be discretized coarsely. The $k=1$ term matches the equivalent complex baseband (ECB) method of communication engineering without requiring a Hilbert transform. The letter is purely theoretical, treats only the bivariate case, and reports no numerical experiments.

### Contributions

1. Formulated a multirate integro-PDE for RF circuits whose convolution term is a bivariate convolution with a multivariate impulse response, required to reproduce the ordinary DAE convolution along every characteristic curve.
2. Derived, for a general instantaneous frequency $\omega(\tau)$, pointwise equalities between the multivariate and ordinary impulse responses that link the integro-DAE and integro-PDE solutions along the characteristics.
3. Showed for a fixed carrier frequency that the impulse response $h(\tau)\,\delta(\hat t-\omega_0\tau)$, with a periodic Dirac distribution, satisfies these equalities and reduces the output to a univariate convolution along each characteristic.
4. Derived a harmonic-wise form in which each Fourier envelope is convolved with a frequency-shifted impulse response, and proved it equivalent to the Dirac form.
5. Identified the $k=1$ envelope and the shifted transfer function $H(\omega+\omega_0)$ with the ECB signal and baseband transfer function, making the method compatible with coupled circuit and communication-system simulation.

### Comments

- §II, Eq. (2), and §III, Eq. (5): the multirate PDE is printed as $\frac{\partial}{\partial\tau}q(\hat x(\tau,\hat t))+\frac{d(\omega(\tau)\tau)}{d\tau}q(\hat x(\tau,\hat t))+i(\hat x(\tau,\hat t))=\hat s(\tau,\hat t)$, with no derivative in $\hat t$ in the second term, which conflicts with the stated characteristic curves $(\tau,\hat t)=(t,\omega(t)t+\Theta)$ along which the PDE and DAE solutions coincide; the intended term is $\frac{d(\omega(\tau)\tau)}{d\tau}\frac{\partial}{\partial\hat t}q(\hat x(\tau,\hat t))$.
- §III and Conclusion: Theorem 3.2 is introduced with "A necessary condition on $\hat h$ is derived next" and is called a necessary condition in the Conclusion, but the theorem states that the DAE and PDE solutions coincide "if" equalities (8) and (9) hold, a sufficient condition, and the preceding text announces "sufficient conditions"; which is intended is unresolved.
- §IV, Eq. (13): the integral in $y_\Theta(t)=\hat y(t,\omega_0t+\Theta)=\int_{-\infty}^{\tau}h(t-\tau')\,\hat x(\tau',\omega_0\tau'+\Theta)\,d\tau'$ has upper limit $\tau$, although $\tau=t$ on this characteristic and the corresponding integrals in the proof of Theorem 3.2 end at $t$; the intended limit is $t$.
- Proof of Theorem 5.2: the final line is $h(\tau)\sum_k\delta(\omega_0\tau-\hat t)$, whose summand does not depend on $k$, whereas the theorem states $h(\tau)\,\delta(\omega_0\tau-\hat t)$ with the periodic Dirac distribution; the theorem's statement is the evident intended result.
