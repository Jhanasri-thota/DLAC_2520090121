# 🚀 VISIONPORT – End-to-End Deep Learning System Architecture

### SKILL_2: FastAPI, Triton, TensorRT, YOLOv8 and GPU Integration


---

## 📌 1. Project Overview

**VISIONPORT** is an End-to-End Deep Learning Object Detection System developed using YOLOv8 and FastAPI.

This experiment focuses on understanding how deep learning models can be integrated into an API-based architecture for image processing and object detection.

The system accepts an image from a client, sends it through a FastAPI REST API, performs object detection using a pretrained YOLOv8 Nano model, and returns detection results in JSON format.

The experiment also examines GPU availability, TensorRT installation, and Triton Inference Server readiness to understand the infrastructure required for production-level deep learning deployment.

## 🎯 2. Objectives

- Understand end-to-end deep learning system architecture.
- Integrate YOLOv8 with FastAPI.
- Develop REST API endpoints for model inference.
- Understand HTTP GET and POST requests.
- Perform image-based object detection.
- Monitor CPU and GPU availability.
- Check TensorRT and Triton infrastructure readiness.
- Generate JSON-based prediction responses.
- Analyze model inference time and API response time.
- Visualize system architecture and performance metrics.

## 🛠️ 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| YOLOv8n | Object Detection Model |
| Ultralytics | Deep Learning Framework |
| FastAPI | REST API Development |
| Uvicorn | ASGI Server |
| PyTorch | Deep Learning Backend |
| OpenCV | Image Processing |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| TensorRT | GPU Inference Optimization Technology |
| Triton | Model Serving Technology |
| Google Colab | Development Environment |

## 🏗️ 4. System Architecture

The VISIONPORT system follows an API-based deep learning inference architecture.

### Architecture Workflow

```text
        CLIENT / GOOGLE COLAB
                 |
                 ▼
          IMAGE UPLOAD
                 |
                 ▼
          FASTAPI REST API
                 |
                 ▼
           HTTP POST
            /predict
                 |
                 ▼
        YOLOv8 INFERENCE ENGINE
                 |
                 ▼
           GPU / CPU
                 |
                 ▼
          OBJECT DETECTION
                 |
                 ▼
       BOUNDING BOX GENERATION
                 |
                 ▼
           JSON RESPONSE
                 |
                 ▼
          CLIENT RECEIVES
          DETECTION RESULTS
```

### Optional Infrastructure

- **Triton Inference Server:** Can be integrated for scalable model serving.
- **TensorRT:** Can be integrated to optimize compatible models for NVIDIA GPU inference.

Note: Triton and TensorRT are checked for availability in this experiment but are not directly integrated into the actual inference pipeline.

## 🧠 5. Model Information

**Model:** YOLOv8 Nano (YOLOv8n)

YOLOv8 is a pretrained deep learning model developed by Ultralytics for object detection.

The model identifies objects in uploaded images and generates bounding boxes, class labels, and confidence scores.

### Model Configuration

| Parameter | Value |
|---|---|
| Model | YOLOv8n |
| Model File | yolov8n.pt |
| Confidence Threshold | 0.25 |
| Input Image Size | 640 |
| Inference Type | Image-based Detection |
| Execution | CPU / GPU |
| Framework | Ultralytics |

## ⚙️ 6. Installation and Execution

This experiment is implemented using Google Colab.

### Step 1: Open Google Colab

Open the notebook using Google Colab.

### Step 2: Install Dependencies

```python
!pip install -q ultralytics fastapi uvicorn python-multipart requests pillow
```

### Step 3: Import Libraries

```python
import cv2
import torch
import numpy as np
import matplotlib.pyplot as plt

from ultralytics import YOLO
from fastapi import FastAPI, UploadFile, File
import uvicorn
```

### Step 4: Check Hardware Configuration

The system checks whether an NVIDIA GPU is available using PyTorch.

```python
gpu_available = torch.cuda.is_available()

if gpu_available:
    print(torch.cuda.get_device_name(0))
else:
    print("CPU Execution")
```

### Step 5: Load YOLOv8 Model

```python
model = YOLO("yolov8n.pt")
```

### Step 6: Create FastAPI Application

```python
app = FastAPI(
    title="VisionPort Inference API",
    description="End-to-End Deep Learning Object Detection API",
    version="2.0"
)
```

### Step 7: Start API Server

The FastAPI application runs using Uvicorn on port 8001.

### Step 8: Perform Object Detection

The uploaded image is sent through an HTTP POST request to the `/predict` endpoint.

The YOLOv8 model processes the image and returns detection information.

## 🌐 7. API Endpoints

The system provides three main API endpoints.

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Displays project information |
| GET | `/health` | Checks API and model health |
| POST | `/predict` | Performs object detection |

### Example JSON Response

```json
{
    "status": "success",
    "filename": "sample.jpg",
    "model": "YOLOv8 Nano",
    "hardware": "CPU",
    "total_objects": 2,
    "inference_time_ms": 45.23,
    "total_processing_time_ms": 48.65,
    "detections": [
        {
            "object": "person",
            "confidence": 96.45,
            "bounding_box": [120, 80, 350, 480]
        },
        {
            "object": "car",
            "confidence": 91.32,
            "bounding_box": [400, 200, 650, 430]
        }
    ]
}
```

*Note: The values above are illustrative. Actual results depend on the uploaded image and execution hardware.*

## 📊 8. Performance Analysis

The experiment generates graphical representations of system performance.

### A. Object Detection Visualization

Displays:
- Original uploaded image.
- Detected image.
- Bounding boxes.
- Object labels.
- Confidence scores.

### B. Object Confidence Graph

Displays the confidence percentages of detected objects using a horizontal bar chart.

### C. System Performance Graph

Compares:
- API Round Trip Time.
- Model Inference Time.
- Server Processing Time.

These measurements help understand the performance of the inference pipeline.

## 🔍 9. Hardware and Infrastructure Monitoring

The system checks the following components:

| Component | Monitoring |
|---|---|
| CPU | Available for inference |
| NVIDIA GPU | CUDA availability |
| PyTorch | Version information |
| TensorRT | Installation availability |
| Triton Client | Installation availability |
| Triton Server | Health endpoint availability |

**Implementation status:**

- FastAPI REST API: Implemented.
- YOLOv8 inference: Implemented.
- GPU/CPU execution: Implemented.
- TensorRT: Availability check only.
- Triton: Availability check only.

## 📁 10. Project Structure

```text
VISIONPORT/
│
├── SKILL_1/
│   ├── SKILL_1_DLAC.ipynb
│   └── README.md
│
├── SKILL_2/
│   ├── SKILL_2_DLAC.ipynb
│   ├── README.md
│   └── outputs/
│       └── VisionPort_SKILL_2_Output.jpg
│
└── README.md
```

## 💡 11. Applications

- Intelligent surveillance systems.
- Smart traffic monitoring.
- Automated image analysis.
- Real-time object recognition.
- Computer Vision applications.
- Deep Learning model deployment.
- API-based AI applications.

## 🚀 12. Future Enhancements

- Actual Triton Inference Server integration.
- TensorRT model optimization.
- Real-time webcam detection.
- Video-based object detection.
- Object tracking and monitoring.
- Docker-based deployment.
- Cloud-based inference services.
- Scalable GPU-based model serving.

## ⚠️ 13. Limitations

- The experiment uses a pretrained YOLOv8 model.
- Detection performance depends on image quality and hardware.
- GPU availability depends on the Google Colab runtime.
- Triton and TensorRT are not used for actual inference in this implementation.
- The FastAPI server runs locally within the Colab environment.

## ✅ 14. Conclusion

The VISIONPORT SKILL_2 experiment demonstrates an end-to-end API-based Deep Learning Object Detection System using FastAPI and YOLOv8.

The experiment successfully integrates image acquisition, REST API communication, model inference, object classification, bounding box generation, JSON response handling, and performance visualization.

It also introduces important production-level infrastructure concepts such as GPU acceleration, TensorRT optimization, and Triton model serving.

This experiment provides a practical foundation for understanding how deep learning models can be deployed and accessed through REST APIs.

---

### 📌 Project Information

**Project:** VISIONPORT

**Experiment:** SKILL_2 – End-to-End Deep Learning System Architecture

**Domain:** Deep Learning and Computer Vision

**Model:** YOLOv8 Nano

**API Framework:** FastAPI

**Development Platform:** Google Colab

**Primary Focus:** API-Based Deep Learning Inference and System Architecture
