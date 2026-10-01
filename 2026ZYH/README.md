# 2026ZYH

## ChatGPT (July 2026)

### Summary

Wall-modeled large-eddy simulation reduces the cost of high-Reynolds-number turbulence calculations, but conventional and offline-learned wall models often fail for nonequilibrium flows or when deployed with different grids and discretizations. This paper develops a differentiable WMLES framework in which forward-mode automatic differentiation propagates exact gradients through the LES solver and enables in-situ optimization of a physics-embedded wall model. The model augments a thin-boundary-layer ordinary differential equation with neural-network-controlled forcing terms. Gradient accuracy is verified on lid-driven cavity flow. Models trained in channel and periodic-hill simulations account for the deployed numerical environment and generalize across Reynolds numbers, grid skewness, hill slopes, and unseen bump, hump, and ramp geometries. A channel-trained model extrapolates six orders of magnitude in Reynolds number, while the periodic-hill-trained model predicts separation and reattachment on new geometries; ramp-flow mean-velocity errors remain below 2% at tested stations.

### Contributions

1. Introduced an end-to-end differentiable wall-modeled large-eddy simulation solver using forward-mode automatic differentiation.
2. Embedded a neural forcing term in a thin-boundary-layer wall-model equation.
3. Verified automatic gradients against finite differences using lid-driven cavity flow.
4. Demonstrated Reynolds-number and grid-discretization transfer from in-situ channel-flow training.
5. Transferred a single periodic-hill-trained model to varied hills and unseen bump, hump, and ramp flows.
