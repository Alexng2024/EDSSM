Event-Driven State Space Models (EDSSM): Exact Continuous-Time Propagation on Sparse Timelines
Authors: KS NG, PhD
Draft version: June 2026
________________________________________
Abstract
State space models (SSMs) have become a leading architecture for long-sequence modeling, yet nearly all implementations discretize dynamics on a dense temporal grid of length L, incurring O(L) state updates even when inputs are sparse. Zero-order hold (ZOH) discretization further introduces avoidable error when a fixed step size fails to align with signal discontinuities. We introduce Event-Driven State Space Models (EDSSM), a framework that propagates latent state through exact closed-form continuous-time linear dynamics—implemented via the matrix exponential e^AΔt—and applies updates only at informative event times. Quiescent intervals are merged into a single homogeneous flow, reducing propagation cost from O(L) to O(K) when K≪L events carry information, with sparsity ratio ρ=K/L. We prove that uniform-grid ZOH discretization is a special case of EDSSM, characterize when event-aligned integration achieves zero discretization error under piecewise-constant inputs, and bound excess error of misaligned coarse grids. Unlike learned skip mechanisms that copy hidden state during inactive steps, EDSSM evolves state exactly during silence. We extend the core with event-conditioned gating and multi-scale temporal propagators confined to event times, preserving efficiency. EDSSM targets both native event streams and sparse activations on fixed clocks—settings where dense SSMs overpay computation and energy. We outline benchmarks and ablations against S5, Mamba, Event-SSM, and skip-RNN baselines.
Keywords: state space models, event-driven processing, matrix exponential, sparse sequences, continuous-time dynamics, energy-efficient inference



<img width="1094" height="508" alt="image" src="https://github.com/user-attachments/assets/5cacdc8e-5183-466c-a8a1-45da8ae73977" />
