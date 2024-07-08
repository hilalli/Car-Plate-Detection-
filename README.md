## YOLOv8-Based Automatic Vehicle License Plate Detection and Recognition System ##
This project aims to detect and recognize vehicle license plates using the YOLOv8 model and EasyOCR library. Below are the components and usage steps of the project.

Table of Contents
Project Description
Requirements
Installation
Data Preparation
Training
Viewing Results
Demo and Application
Additional Information
Project Description
This project implements an automatic vehicle license plate detection and recognition system using the YOLOv8 model and EasyOCR library. The YOLOv8 model is trained using deep learning techniques to detect vehicle license plates, while EasyOCR is utilized for optical character recognition (OCR).

Requirements
Python 3.x
Anaconda or Virtualenv
YOLOv8 model
EasyOCR library

Installation
Clone this repository to your local machine:


git clone https://github.com/hilalli/Car-Plate-Detection-
cd repo

Install required Python dependencies:
pip install -r requirements.txt

Data Preparation
Download and incorporate the dataset from Roboflow. Then, prepare the dataset for YOLOv8 model training.

Training
To train the YOLOv8 model, use the following command:

python train.py model=yolov8m.pt data=data.yaml epochs=200 imgsz=640

Viewing Results
To view training results and model performance, use the following command:

ls runs/detect/train

Demo and Application
To run the project as a demo, follow these steps:

Use the model to perform license plate recognition on video or image:

python predict.py model='best.pt' source='demo.mp4'

Note: The best.pt file, which contains the trained model weights, is not included in this repository due to its large size. You need to obtain it separately and place it in the appropriate directory (/content/drive/MyDrive/ in this case).

View the results as a compressed video:

ffmpeg -i runs/detect/train/demo.mp4 -vcodec libx264 result_compressed.mp4


Additional Information
Detailed instructions on configuring and training the YOLOv8 model are provided within the project.
Information on performing optical character recognition (OCR) using the EasyOCR library is also included.
This README file provides essential steps to get started with and use the project effectively. For detailed information, please refer to the relevant code files and documentation.

