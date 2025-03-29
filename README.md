# Performance Analysis of YOLOv8 in Detecting Computer Components
_Presented in International Conference on Information Technology and Education (ICITE), SolBridge International School of Business, South Korea_
# 📌 Project Overview
This project explores the performance of YOLOv8 (You Only Look Once, version 8) in detecting various computer components such as CPUs, GPUs, RAM sticks, and motherboards. The experiment involves training a custom object detection model using Ultralytics' YOLOv8 framework and evaluating its accuracy in real-world scenarios.

The research findings were presented at the International Conference on Information Technology and Education (ICITE), where it was accepted and recognized for its contribution to the field of machine learning and computer vision.

## 🌐 Live Demo

Simple integration with react + flask web app 👉👉 [Visit the Website](https://detect-computer-parts.vercel.app/)

## 🚀 Setup and Installation
__1. Clone the Repository__

    git clone https://github.com/JamesManalili/Computer-part-Detection-Using-YOLOv8.git
    cd Computer-part-Detection-Using-YOLOv8

__2. Install Dependencies__

    pip install ultralytics==8.0.196
    pip install albumentations==1.4
    pip install roboflow

__3. Check NVIDIA GPU (Optional but Recommended or You can Use google colab)__

    !nvidia-smi

__4. 📂 Dataset Preparation__

We use Roboflow to manage and download the dataset. If you don't have a Roboflow API key, sign up at roboflow.com and replace "your_api_key", "your_workspace", and "your_project_name" in the code below:

    from roboflow import Roboflow
    
    rf = Roboflow(api_key="your_api_key")
    project = rf.workspace("your_workspace").project("your_project_name")
    dataset = project.version(1).download("yolov8")

## 🎯 Model Training
To train YOLOv8 on the dataset (you can adjust the number of epochs):

    yolo task=detect mode=train model=yolov8s.pt data={dataset.location}/data.yaml epochs=45 imgsz=800 plots=True

## 📊 Results and Findings
The trained YOLOv8 model achieved outstanding performance in detecting computer components:

✅ Mean Average Precision (mAP): 97.9%

✅ Precision: 96.0%

✅ Recall: 96.2%

## 🏆 Achievements

✔ Paper Accepted at ICITE (International Conference on Information Technology and Education) – [Read Here]()

✔ Presented at SolBridge International School of Business, South Korea

✔ Received 4 Certificates of Recognition – [View Certificates]()


