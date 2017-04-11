# **HyperFace-with-SqueezeNet**
Two multitasking CNNs for simultaneous face detection, landmarks estimation and visibility, pose estimation and gender recognition.  

## **hyperface.py** 
It concatenates feature maps from initial, mid and final layers of the network and then branches out to different heads.  

## **multiout.py** 
It branches from the final layer of the network to different heads. 

## **DataGen2.py** 
It is the Data Generator used for reading multiple labels from json files. It is a modified version of Keras's default Data Generator.  

## Sample Outputs
SampleOut1.JPG, SampleOut2.JPG, SampleOut3.JPG are the results of the hyperface model. On the left is the visualization of the head pose of the person while on the right are the estimated landmarks, their visibility and the predicted gender.

## Reference
The idea is based on the following paper -  [1] R. Ranjan, V. M. Patel, and R. Chellappa. Hyperface: A deep multitask learning framework for face detection, landmark localization, pose estimation, and gender recognition. CoRR, abs/1603.01249, 2016.  

This implementation is slightly different. The original HyperFace architecture is built on top of AlexNet while the implementation here uses another architecture called SqueezeNet.
