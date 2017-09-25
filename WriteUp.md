[//]: # (Image References)
[image1]: ./RMSE1.png
[image2]: ./RMSE2.png

### Compiling

The code can be compiled by using `cmake` and `make`.

---
### Accuracy

My px, py, vx, and vy RMSE should are less than or equal to the values [.11, .11, 0.52, 0.52]. My RMSE values together with the aqcuired predicted trajectories are shown in the images below.

![alt text][image1] ![alt text][image2]

---
### Follows the correct algorithm

#### 1. Sensor Fusion algorithm follows the general processing flow

In the file `kalman_filter.cpp` in lines 27 through 78 are shown the general process flow of the prediction step and the update step for both linear and non-linear measurement case. 

---
#### 2. Kalman Filter algorithm handles the first measurements appropriately

The first measurements are used as a starting point for the algorithm. They are set in `FusionEKF.cpp` in lines 78 through 103.

---
#### 3. Kalman Filter algorithm first predicts then updates

The predict takes place in line 116 in `FusionEKF.cpp` before the update step.

---
#### 4. Kalman Filter can handle radar and lidar measurements

The lidar and radar measurements are separated in `FusionEKF.cpp` and the `Update` and `UpdateEFK` methods of `KalmanFilter` class are used respectively for lidar and radar measurements. This takes place in `FusionEKF.cpp` in lines 122 through 134.

---
### Code Efficiency

The code does not include lot of unnecessary calculation. Few of the calculations could be performed without helping variables, but this is done to make to code also easily readable for debugging reasons.

