# Indoor-Dataset

The indoor dataset is collected using [ZED Mini](https://www.stereolabs.com/developers/release/) camera for training and evaluating the network in real-time. The collected dataset is used for two objectives:
1. Predict depth maps for an indoor-environment scene.
2. Used predicted deph map for Robot Palletization (pick-n-place task).

## Task-1: Predict Depth Maps for an Indoor-environment Scene.
Using ZED-m camera multiple videos of the indoor scene (our workplace) is collected. From the video, stereo-rectified pair (left and right) of images are obtained. We collected around 12,000 frames for training the network. Some randomly sampled images, their depth, confidence maps and reconstructed point clouds are shown in the figure below:

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1.png) 
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4.png)

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1_d.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2_d.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4_d.png)

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1_c.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2_c.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4_c.png)

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1_pc.jpg)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2_pc.jpg)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4_pc.jpg)

## Task-2: Used predicted depth map for Robot Palletization task.
We created a setup with multiple boxes placed on a table having different sizes and placed at different orientations. The setup is created so as to enable the robotic arm to perform pick and place task of a box after navigating to its centroid position. Using ZED Mini the dataset is created of the setup and network is trained with the collected dataset. 

We captured a RGB image of the setup and using the trained model we predict the depth map of it. With the RGB image and the depth map, we created a 3D point-cloud of the setup. On the point-cloud then applied region growing algorithm to locate the box and move the UR10 collaborative robotic arm to its centroid to pick the box. We also used confidence maps for masking out those pixels having confidence values less than the threshold value (90% for our case) to test the authenticity of the predicted confidence maps.
