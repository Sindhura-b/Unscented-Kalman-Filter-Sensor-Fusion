# Sensor Fusion and Object Tracking using Unscented Kalman Filter

In this project unscenteded kalman filter has been utilized to estimate the state of a moving object of interest with noisy lidar and radar measurements. The developed algorithm is tested on two different different datasets provided in the Udacity's Simulator and experimented till the RMSE values that determine the accuracy of algorithm are below the specified threshold. The values of process covariance matrix are tuned using Normalized Innovation Squared (NIS) consistency check, which is the difference between actual and predicted measurements and follows chi squared distribution.

[//]: # (Image References)
[image1]: ./result_dataset1.png
[image2]: ./result_dataset2.png
[image3]: ./Laser_nis.jpg
[image4]: ./NIS_radar.jpg

---

## Instructions to run

The main program can be built and run by doing the following from the project top directory.

1. cd build
2. cmake ..
3. make
4. ./UnscentedKF
5. Open term-2 Simulator and click start 

The programs that are written to accomplish the project are present in folder src - ukf.cpp, ukf.h, main.cpp, tools.cpp, and tools.h

INPUT: values provided by the simulator to the c++ program

["sensor_measurement"] => the measurment that the simulator observed (either lidar or radar)

OUTPUT: values provided by the c++ program to the simulator

["estimate_x"] <= kalman filter estimated position x
["estimate_y"] <= kalman filter estimated position y
["rmse_x"]
["rmse_y"]
["rmse_vx"]
["rmse_vy"]

## Results

![alt text][image1]

![alt text][image2]

Satisfactory NIS plots of lidar and radar measurements obtained after tuning process measurement noise parameters.

![alt text][image3]

![alt text][image4]

