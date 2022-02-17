# VIO Comparision (VIO- Visual Inertial Odometry)

In this repo we have provided the docker images for different publicly available VIO algorithms.

Docker images is created to make the process of comaprision easy,fast and also to get rid of the dependencies issues while installation of all the algorithms on same system.

We can evaluate the algorithms with (ETH MAV Visual Inertial Datasets with Motion and Structure Ground-Truth)[here](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets) as well as with our own dataset or realtime data.

Every container contains a trajectory recording python script for recording the trajectory in text file which can be further used to calculate RMSE(Root mean square error) of different algorithms with respect to ground truth.(Steps will be given in each readme file)

Docker image of these algorithms is available:( please find the .md files above in code section for docker setup)
1) [VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono)
2) [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)
3) [OKVIS-core](https://github.com/ethz-asl/okvis)
4) [OKVIS-ros](https://github.com/ethz-asl/okvis_ros)
5) [ROVIO](https://github.com/ethz-asl/rovio)
6) [SVO-GTSAM](https://github.com/uzh-rpg/rpg_svo_pro_open)
