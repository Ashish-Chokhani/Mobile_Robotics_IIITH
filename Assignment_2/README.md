# Author: Ashish Chokhani
# Roll No: 2021102016
# MR Assignment 2

---
## Section 1: Levenberg Marquardt
### Levenberg Marquardt Algorithm Implementation
- In the levenberg_marquardt.py module, you'll find a Python implementation of the Levenberg Marquardt algorithm using numpy.
- This implementation aims to solve for the parameters of a Gaussian distribution. The Gaussian distribution is parametrized by μ and σ.

### Problem Statement
- Given a set of observations (x, y) and an initial estimate of the parameters (μ, σ), the algorithm iteratively refines the parameters to best fit the observations.

### Experiments and Visualization
- Experiment with the number of iterations.
- Experiment with the learning rate.
- Experiment with the tolerance.
- Results are visualized using matplotlib, with graphs displaying:

- Cost function value (J) vs the number of iterations.
- Ground Truth data values and the predicted data values.
- Hyperparameter Observations
- Hyperparameters are experimented with and compiled in a table within the documentation. Each set of hyperparameters is clearly mentioned with justification.

## Section 2: ICP
### Procrustes Alignment for ICP
- In the icp_alignment.py module, a function is provided to perform Procrustes alignment on two point clouds with known correspondences.
- Using the toothless.ply point cloud, the task is to align two point clouds (X & P1, X & P2) and recover the transformation between them.
- The alignment error is computed using Root Mean Squared Error (RSME).

## Section 3: Pose Graph Optimization
1. Pose Graph Optimization for 1D SLAM
- Replicate a solved example for 1D SLAM, optimizing for pose using least squares.
- Refer to the notebook parts/Part 1 - 1D SLAM.ipynb for detailed information and solution.

2. Pose Graph Optimization for 2D SLAM
- Optimize a sample noisy trajectory using pose-graph optimization.
- Refer to the notebook parts/Part 2 - 2D SLAM.ipynb for detailed information on LM implementation, plots and explanation, and Jacobian and Residual Calculation.

3. Trajectory Evaluation and g2o (Bonus Question)
- Evaluate the optimized trajectory using Evo and explore the g2o tool to obtain an even better-optimized trajectory.
- Refer to the notebook parts/Part 3 - Trajectory Evaluation and g2o.ipynb for detailed instructions and insights.
