[//]: # (Image References)
[image1]: ./output_images/RMSE.png

### Compiling

The code can be compiled by using cmake and make.

---
### Accuracy

My px, py, vx, and vy RMSE should are less than or equal to the values [.11, .11, 0.52, 0.52]. My RMSE values together with the aqcuired predicted trajectory are shown in the image below.

![alt text][image1]

---
### Follows the correct algorithm

#### 1. Your Sensor Fusion algorithm follows the general processing flow



---
#### 2. Your Kalman Filter algorithm handles the first measurements appropriately

I recorded the positions of positive detections in each frame of the video.  From the positive detections over last 10 frames (This helped to reduce the noise and false postives as well) I created a heatmap and then thresholded that map to identify vehicle positions.  I then used `scipy.ndimage.measurements.label()` to identify individual blobs in the heatmap.  I then assumed each blob corresponded to a vehicle.  I constructed bounding boxes to cover the area of each blob detected.

#### 3. Your Kalman Filter algorithm first predicts then updates



---
#### 4. Your Kalman Filter can handle radar and lidar measurements



---
### Code Efficiency



