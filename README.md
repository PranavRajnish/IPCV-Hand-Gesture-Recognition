# IPCV-Hand-Gesture-Recognition
Repo for PES IPCV course project.

## Setup
For this project we are using an anaconda virtual environment with python 3.9

`conda create -n myenv pip python=3.9`

TensorFlow version 2.5.0 for building the model.

`pip install --ignore-installed --upgrade tensorflow==2.5.0`

TensorFlow object detection API

https://github.com/tensorflow/models

The Tensorflow Object Detection API uses Protobufs to configure model and training parameters. 
Before the framework can be used, the Protobuf libraries must be downloaded and compiled.

https://github.com/protocolbuffers/protobuf/releases

Once extracted add the path to protobuf bin into your path variables.

TensorFlow object detection API need COCO API as a dependency.

`pip install cython
pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI`

Installing the object detection API:
Inside of Tensorflow\models\research run the commands

`cp object_detection/packages/tf2/setup.py .
python -m pip install --use-feature=2020-resolver`

OpenCV for accesing webcam footage for realtime object detection.

`pip install opencv-python`

## Running the model

To run the model execute the run.ipynb file


## Note 

For the object detection, we have cloned the git repo https://github.com/nicknochnack/RealTimeObjectDetection, which is face mask detection training template.
We have then adapted the model to work for hand gesture recognition by changing the number of classes, feeding into it our custom datset, and changing the config parameters of the model.
