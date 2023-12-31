# Author: Ashish Chokhani
# Roll No: 2021102016
# MR Assignment 3

---
## Section 1: Epipolar lines and Epipoles
### Fundamental Matrix Estimation and Epipolar Lines
- In the epipolar_lines.py script, you'll find an implementation to estimate the fundamental matrix (F) that encodes the relative geometry of two images.
- The fundamental matrix is computed without using inbuilt functions.
-  Epipolar lines are drawn on both images for the given point correspondences.

### Procedure
- Compute the fundamental matrix (F) using the provided point correspondences.
- Draw epipolar lines on the second image for each point in the first image.
- Draw epipolar lines on the first image for the corresponding points in the second image.

### Implementation Details
- The convention used for F is [F] = [p'] * [p], where p is the location of the point in the first image, and p' is the location of the point in the second image.
- Fundamental matrix (F) is computed without using inbuilt functions.

## Section 2: Monocular Visual Odometry
### Implementation of Basic Monocular Visual Odometry
- Download required data from data/2, which includes a sequence of images from the KITTI dataset, ground truth pose, and camera parameters.
- Find corresponding features between frames and estimate the essential matrix using RANSAC.
- Decompose the essential matrix to obtain the relative rotation.
- Scale the translation with absolute or relative scale.
- Concatenate the relative transformation.
- Repeat the above steps for the remaining pairs of frames.
- Generate a .txt file containing the estimated poses in the same format as the ground truth.
- Plot the estimated trajectory along with the ground truth trajectory using EVO.

### Copy code
``` 
pip install evo --upgrade --no-binary evo
evo_traj kitti ground-truth.txt your-result.txt -va --plot --plot_mode xz
```

### Outputs
- A .txt file containing the estimated poses.
- A plot of the estimated trajectory along with the ground truth trajectory using EVO.
- Report the obtained trajectory error.

## Section 3: Stereo Dense Reconstruction
### Dense 3D Point Cloud Reconstruction from Stereo Images

- Download required data from data/3, which includes left and right stereo images, ground truth poses, and camera parameters.
- Generate a disparity map for all given stereo pairs using OpenCV (e.g., StereoSGBM).
- Generate colored point clouds from each disparity map, ignoring points with invalid disparity values. Use Open3D for storing point clouds.
- Register (or transform) all generated point clouds into the world frame using the provided ground truth poses.
- Visualize the registered point cloud data in color using Open3D.

### Outputs
- Visualized dense 3D point cloud reconstruction in color.

<br />
Note: Detailed implementation and usage instructions are available within each script and notebook. Ensure that dependencies are installed before running the provided commands.
