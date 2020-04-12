# GenderAgePred
Gender and Age Prediction using OpenCV and Pretrained CNN Model


In the above mentioned prediction model for increasing the efficiency of the model, apart from training the model from the scratch we use pre-trained Convolutional Neural Network Model for gender and age prediction. 
These models are the Caffe Models for Age Prediction and Gender Prediction.

Dependencies :-

OpenCV
Numpy
Argparse

Dataset :-

Adience Benchmark
The data included in this collection is intended to be as true as possible to the challenges of real-world imaging conditions. In particular, it attempts to capture all the variations in appearance, noise, pose, lighting and more, that can be expected of images taken without careful preparation or posing.

Experiment :-

Predict the gender and age of a given image where the age is a classification problem which contains age groups of "(0-2)", "(4-6)", "(8-12)", "(15-20)", "(25-32)", "(38-43)", "(48-53)", "(60-100)".

Proposed Method :- 

In the Age and Gender Prediction Model the proposed problem is a classification problem as age and gender prediction becomes hard when the person in the image is having makeup or has altered his normal look by less illumination or odd camera angle leading to distorted image. The age and gender model is using Pretrained Convolutional Neural Network which is trained on Adience Dataset.
	The project has 3 Phases in all. These are :-
1.	Face Detection 
2.	Gender Prediction
3.	Age Prediction

Novelty :-

	In the project we have used Deep Neural Network Face Detector in OpenCV. It is based on Single-Shot-Multibox detector and uses ResNet-10 Architecture as backbone. The model was trained using images available from the web. 
In this, the image is converted to a blob and passed through the network using the forward() function. The output detections is a 4-D matrix, where the 3rd dimension iterates over the detected faces. The fourth dimension contains information about the bounding box and score for each face. For example, detections [0,0,0,2] gives the confidence score for the first face, and detections [0,0,0,3:6] give the bounding box.
The output coordinates of the bounding box are normalized between [0,1]. Thus the coordinates should be multiplied by the height and width of the original image to get the correct bounding box on the image.
Advantages of using DNN Face Detection over Haar Cascades:-
1.	Works for different face orientations – up, down, left, right, side-face etc.
2.	Works even under substantial occlusion
3.	Detects faces across various scales ( detects big as well as tiny faces )

The above mentioned DNN Face Detector is better Haar Cascades for face detection as it produces less false positives and works on non-frontal images.

