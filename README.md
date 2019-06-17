# Self-Driving-Car
Autonomous driving field is very popular these days. The goal of this project is to explore how Deep Learning is used in various self-driving car algorithms. The objective here is to train a deep learning model (Keras CNN) that can make predictions for the steering angle based on input camera images and the last known state of the vehicle. The dataset is from Microsoft AirSim https://aka.ms/AirSimTutorialDataset.
# Overview of Technology:
## Dataset:
This link has a good collection of data from the AirSim simulation environment. https://github.com/Microsoft/AirSim). The images produced by the simulator in training mode are 148X256. The data is in `tsv` file that includes path to image and associated steering angle, throttle, brake and speed for each frame
Dataset Size: 3.5 GB   Format of Data File: TSV
## High Level Overview of Steps:
1.	Download and install AirSim from here approx. 17 GB
2.	Download and Setup dataset. https://aka.ms/AirSimTutorialDataset.
3.	Install Python Jupiter Notebook to clean and aggregate data. 
4.	Include visualizations to help determine next step. 
5.	Train the model without Data Augmentation and with Data Augmentation
6.	Test the model on simulator

## Hardware:
HP Z-book laptop running Windows 10 on an Intel® Core™ i7-7820 CPU processor with 32 GB RAM. 
AWS EC2 p3.8Xlarge instance for training model.

## Software:
AirSim Simulator (https://github.com/Microsoft/AirSim), 
Python 3.6.3, h5py 2.8.0, Keras 2.1.3, msgpack-python 0.5.6, msgpack-rpc-python 0.4.1, opencv-python 3.4.0.12, tensorflow-gpu 1.10.0, tornado 4.5.3

## Lessons Learned:
•	Working with large dataset is a challenge. We should have appropriate hardware to deal with them. 
•	If you want to work on AWS with large datasets, make sure you take into account the addional time and memory needed. 
•	AirSim needed msgpack-rpc-python. Conda could not install it on mylaptop. So make sure your hardware is compatible with all the requirements of the installations you’re going to make. 
•	For self-driving cars even 3.5 GB of data are not enough to get a good model for real life scenarios and in reality the cars train on peta bytes of data. 
•	Remember to stop the instance after it’s usage and not to run the model more than an hour if you’re not sure if it will converge.
