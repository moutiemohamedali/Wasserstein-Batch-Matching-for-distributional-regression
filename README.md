# Abstract

Regression under i.i.d. noise is well understood, but this assumption rarely holds in practice.
Measurement pipelines, numerical PDE solvers, and privacy constraints all induce noise that
is correlated, heavy-tailed, or structured at the batch level. In the worst regimes, even the
correspondence between an input and its observed output is lost, and it is precisely here that
losses like the MSE break down, since they assume a fixed pointwise input-output match. In
this project, we study the Wasserstein Batch Matching (WBM) framework of Dakhmouche et al.
(2025) [1], which relaxes this match into a distributional, batch-level one driven by the Wasserstein
distance, and we extend it in three directions. First, we derive the influence function of the WBM
estimator, and show that in the linear case it is not B-robust: its influence grows linearly in the
contamination point. This suggests that the strength of WBM does not come from bounding
the effect of outliers, but rather from its tolerance to a broken input-output correspondence. We
then illustrate this on low-dimensional examples, where, under batch-level shuffling, the MSE
collapses towards the mean while WBM still recovers the global shape of both a 1D and a 2D
target. Finally, we apply WBM to operator learning on the Navier–Stokes equations. Under
batch-level shuffling, WBM outperforms the L1 baseline at nearly every corruption rate, with a
near two-fold error reduction at ρ = 0.75. Under heavy-tailed Cauchy corruption, however, its
advantage holds only at low corruption and reverses once corruption is severe, which is consistent
with what the non-B-robustness of the estimator predicts. Together, these results help pin down
where it shines: WBM is robust to corruption that preserves the batch output distribution, and
to heavy tailed noise in settings of moderate corruption.

## Report
[📄 PDF](./Master_Project_Robust_Regression-55.pdf)
