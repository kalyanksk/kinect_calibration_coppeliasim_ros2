# kinect_calibration_coppeliasim_ros2
This is illustration of how kinect can be calibrated using coppeliasim and ros2.

# Requirements
1. CoppeliaSim
2. Ros Humble
3. Ubuntu 22.04 / Linux Mint 21.2

# Usage
1. Clone this repository or download the scene file.
2. Open CoppeliaSim and load the kinect_calibrate.ttt scene.
3. Follow the [camera calibration](https://navigation.ros.org/tutorials/docs/camera_calibration.html) tutorial to install camera calibration package for ros2.
4. In CoppeliaSim start the loaded scene and open terminal to run script for camera calibration.
   ```
   ros2 run camera_calibration cameracalibrator --no-service-check --size 7x9 --square 0.02 --ros-args -r image:=/kinect_rgb -p camera:=/kinect/camera_info
   ```
6. After enough data is available for calibration the CALIBRATE button will light up. Click it to see the results.
   ![calibrate](https://github.com/kalyanksk/kinect_calibration_coppeliasim_ros2/assets/94881228/86eb6bc6-c432-44dd-8293-f633f17b026c)
7. After the calibration is completed the save and commit buttons light up. And you can also see the result in terminal.
   ![calibrate3](https://github.com/kalyanksk/kinect_calibration_coppeliasim_ros2/assets/94881228/7f71d4ea-f1bc-4818-ab69-7310c59526d2)![calibrate4](https://github.com/kalyanksk/kinect_calibration_coppeliasim_ros2/assets/94881228/3c5229a5-f9f4-4ac3-8998-9660d9dab6f4)

   
