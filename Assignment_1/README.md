# Author: Ashish Chokhani
# Roll No: 2021102016
# MR Assignment 1

## Section 1: Transformations and Representations
- Euler Angles
<br />
a. Rotation Matrix from Euler Angles
In the transformations.py module, you can find a Python function named euler_to_rotation_matrix(alpha, beta, gamma) that computes a rotation matrix using Euler angles (𝛼, 𝛽, 𝛾) = (π/6, 7π/18, 2π/9) in radians with the X-Y-Z convention. No inbuilt functions are used to ensure transparency and understanding.

b. Solving for Angles with fsolve
Explore the solve_angles.py script where we employ the fsolve function from scipy to solve for Euler angles. The script provides three different initializations, and the results are compared for each initialization.

c. Gimbal Lock Visualization
To visualize Gimbal Lock, run the gimbal_lock_animation.py script. This script demonstrates the Gimbal Lock phenomenon on the point cloud provided in data/toothless.ply. The animation showcases rotations along each axis one by one.

1.2 Quaternions
a. Conversion between Rotation Matrix and Quaternion
Within transformations.py, you will find functions to convert a rotation matrix to a quaternion (rotation_matrix_to_quaternion) and vice versa (quaternion_to_rotation_matrix). These functions are implemented without relying on inbuilt libraries.

b. Matrix Multiplication and Quaternion Transformation
Explore the script matrix_quaternion_comparison.py to witness the comparison between matrix multiplication of two 3x3 rotation matrices and the transformation in the quaternion space. This ensures the consistency of the final transformations.

c. Quaternion Interpolation
To visualize quaternion interpolation, run the script quaternion_interpolation.py. This script interpolates a given model between two rotation matrices using quaternions, providing a clear visualization of the interpolation process.

1.3 Waypoint Generation and Trajectory Visualization
For waypoint generation and smooth trajectory visualization, refer to the waypoint_trajectory.py script. Selecting a starting point within the shape, the script generates waypoints, adds a coordinate frame at the beginning, and ensures motion consistency with no trajectory jumps.

Section 2: 3D Mapping from RGB-D Data
2.1 AI2Thor Scene Setup
To set up AI2Thor and open the assigned scene, refer to the ai2thor_setup.md file. It provides detailed instructions on setting up AI2Thor, navigating the scene, and adjusting camera parameters.

2.2 Recording Script
In the record_movement.py script, you can record the current pose, camera information, and depth images after every movement using WASD or arrow keys. Pose information is stored in the AI2Thor frame format (x, y, z, q0, q1, q2, q3), and additional data can be saved in a separate file if needed.

2.3 Point Cloud Creation
In the create_point_cloud.py script, point clouds are generated for every pair of RGB-D images using Open3D. The depth image is projected onto a 3D point cloud, colors are assigned from RGB images, and a point cloud is created.

2.4 Point Cloud Transformation
For transforming point clouds to the camera frame, the transform_point_cloud.py script utilizes rotation matrices obtained from Section 1.3. It ensures correct transformations between the camera and pose frames.

2.5 Combined Point Cloud
The combine_point_clouds.py script joins all point clouds to create a combined point cloud of the environment. Visualizations include point cloud stitching and camera frame movement trajectory.

2.6 Occupancy Grid Maps
To create occupancy grid maps from different heights, explore the occupancy_grid_maps.py script. Functions within the script generate these maps and visualize the environmental variations.
