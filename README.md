
# Head pose estimation

## Introduction

* This is a project to detect head pose estimation using mediapipe library to detect face mesh and ML to train over AFLW2000.

* The dataset can be downloaded from [here](https://www.kaggle.com/datasets/kameo4189/aflw2000-300wlp?select=AFLW2000-3D).

## Required libraries

* numpy
* os
* scipy
* math
* pandas
* mediapipe
* os
* sklearn
* shutil
* joblib
* warnings

## Main functions

* get_mesh_of_dir:

        Takes a path of a directory as an argument and returns two normalized lists of the Xs and Ys of the mesh points of the faces of all images in the directory using media pipe.

* get_mesh:

        Takes an image as an argument and returns the face mesh points in the image. It works as a helper function for get_mesh_of_dir function.

* make_feature:

        Takes a list or numpy array of Xs or Ys of faces' meshs and a column name string and returns them as a dataframe.

* get_angles_from_dir:

        Takes a directory path and returns all the pitch, raw, roll angles of all .mat files in this directory.

* draw_axis:

        Takes an image, 3 angles (pitch, yaw, roll), the x and y position of the nose (to draw the axes starting from the nose) and the size of the drawing.

* predict:

        Takes an image path or an image, loads a model, predict the 3 angles of the face and returns the 3 angles and the nose indices.

* stream_predict:

        The same as predict but it works with tha labtop or pc camera stream.

## Results

* On Images:
![image](https://github.com/Gooda97/Head-Pose-Estimation-Using-ML-And-Mediapipe/blob/main/results/frame11.jpg)

* On Streaming video:
https://github.com/Gooda97/Head-Pose-Estimation-Using-ML-And-Mediapipe/blob/main/results/2023_02_20_00_39_IMG_0454.MOV

* On external Video:
https://github.com/Gooda97/Head-Pose-Estimation-Using-ML-And-Mediapipe/blob/main/results/new%20video.mp4

        
