# Indoor-Dataset

The indoor dataset is collected using ZED-m camera for training and evaluating the network in real-time. The collected dataset is used for two objectives:
1. Predict depth maps for an indoor-environment scene.
2. Used predicted deph map for robot palletization (pick-n-place task).

## Task-1: Predict Depth Maps for an Indoor-environment Scene.
Using ZED-m camera multiple videos of the indoor scene (our workplace) is collected. From the video, stereo-rectified pair of images are obtained. We collected around 12,000 frames for training the network. Some randomly sampled images, their depth and confidence maps predicted by the trained model are shown in the figure below:

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1.png) 
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4.png)

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1_d.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2_d.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4_d.png)

![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/1_c.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/2_c.png)
![alt text](https://github.com/vbhutani/Indoor-Dataset/blob/master/Sample-Images/4_c.png)
