# ML/DL Projects

Implementations of core machine learning and optimization algorithms, built from scratch in Python and applied to mechanical engineering problems (spring-mass systems, beam deflection, heat conduction). 
## Projects

| # | Project | Concepts | Notebook |
|---|---------|----------|----------|
| 1 | **Gradient Descent Optimizer** | Steepest descent, learning rate effects, ill-conditioning (`a` scaling in `x² + ay²`), contour plots | [`01-gradient-descent/`](./01-gradient-descent) |
| 2 | **Polynomial Regression** | Custom basis-function regression, bias-variance tradeoff, noise sensitivity, L2 regularization | [`02-polynomial-regression/`](./02-polynomial-regression) |
| 3 | **PCA vs. Mode Shapes** | Dimensionality reduction on multi-DOF spring systems, PCA vs. eigenmode comparison, noise robustness | [`03-pca-mode-shapes/`](./03-pca-mode-shapes) |
| 4 | **Neural Networks** | Regression (sin(x) approximation), hyperparameter sweeps (depth, width, learning rate, activation), classification for an electrostatically actuated MEMS switch | [`04-neural-networks/`](./04-neural-networks) |

## What's in each project

**1. Gradient Descent** — A from-scratch steepest descent optimizer (separated into function evaluation, gradient computation, and the update loop), tested on `f(x) = (x-2)²` and a two-variable quadratic. Includes a study of how the condition number of the Hessian (via the parameter `a` in `x² + ay²`) affects convergence, and how learning rate choice interacts with it.

**2. Polynomial Regression** — A generic regression module (basis functions swappable) applied to a noisy spring-mass displacement signal. Explores underfitting vs. overfitting across polynomial degree, how noise level shifts the optimal degree, how error scales with dataset size, and how L2 regularization recovers performance in the overfitting regime.

**3. PCA vs. Mode Shapes** — For an n-DOF spring system, compares two dimensionality-reduction approaches: projecting onto the lowest eigenmodes of the stiffness matrix vs. running PCA on the resulting displacement data. Investigates when the two agree, when they diverge, and how measurement noise affects PCA's reconstruction error.

**4. Neural Networks** — Two parts: (a) a regression NN fit to `sin(x)` (and a second function), used to study the effect of network width, depth, learning rate schedules, activation functions, noise level, and L2 regularization on train/test error; (b) a classification NN that predicts whether a given voltage/force pair produces a viable electrostatic switch design, based on beam deflection mechanics.

## Notes

Reports discussing and interpreting the results for each assignment are included alongside the notebooks where applicable.
