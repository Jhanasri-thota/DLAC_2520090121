# 🚀 VISIONPORT – Deep Learning Object Detection

## SKILL – 3: Inference Request Trace

### 1. Project Overview

VISIONPORT is a Deep Learning Object Detection project developed using the YOLOv8 model. 

SKILL-3 focuses on **Inference Request Tracing**, which tracks the complete lifecycle of an image inference request, from API input to model execution and final response generation.

The experiment uses FastAPI to create an inference API and YOLOv8 Nano to perform real-time object detection.

The system records execution timestamps and measures the processing time of individual inference lifecycle stages.

### 2. Objectives

- Implement an image inference API using FastAPI.
- Integrate the YOLOv8 Nano object detection model.
- Accept images through API requests.
- Perform image preprocessing and validation.
- Execute object detection using YOLOv8.
- Extract detected objects, confidence scores and bounding boxes.
- Track individual inference lifecycle stages.
- Measure actual execution latency.
- Visualize inference performance using Matplotlib.
- Generate downloadable inference trace reports.

### 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| Google Colab | Development Environment |
| YOLOv8 | Object Detection Model |
| Ultralytics | Deep Learning Framework |
| PyTorch | Model Execution |
| FastAPI | API Development |
| Uvicorn | API Server |
| OpenCV | Image Processing |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Requests | API Communication |
| Pillow | Image Loading and Conversion |

### 4. System Architecture

The VISIONPORT inference pipeline consists of the following stages:

```text
             CLIENT IMAGE
                   |
                   v
           API INPUT REQUEST
                   |
                   v
          IMAGE PREPROCESSING
                   |
                   v
           YOLOv8 INFERENCE
                   |
                   v
             POSTPROCESSING
                   |
                   v
          DETECTION EXTRACTION
                   |
                   v
          ANNOTATED IMAGE
                   |
                   v
            JSON RESPONSE
                   |
                   v
          REQUEST TRACE REPORT
                   |
                   v
          LATENCY VISUALIZATION
```

### 5. Inference Lifecycle Stages

**Stage 1: API Input / Request Ingestion**

- Accepts an uploaded image through FastAPI.
- Validates the uploaded file.
- Records request information.
- Measures API input processing time.

**Stage 2: Image Preprocessing**

- Reads the uploaded image.
- Converts the image into RGB format.
- Extracts image dimensions.
- Prepares the image for model execution.

**Stage 3: YOLOv8 Model Execution**

- Loads the YOLOv8 Nano model.
- Performs object detection.
- Uses GPU when available, otherwise CPU.
- Measures model execution time.

**Stage 4: Postprocessing / Detection Extraction**

- Extracts detected object classes.
- Calculates confidence scores.
- Retrieves bounding box coordinates.
- Organizes detection results.

**Stage 5: Annotation / Response Preparation**

- Generates an annotated image.
- Encodes the output image.
- Prepares the inference response.
- Records response preparation time.

### 6. API Endpoints

The experiment implements the following FastAPI endpoints:

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Displays project information |
| GET | `/health` | Checks API health |
| POST | `/predict` | Performs object detection |

API documentation is available through:

```text
http://127.0.0.1:8002/docs
```

### 7. Performance Measurement

The system measures the execution time of each inference lifecycle stage.

The recorded metrics include:

- API Input Processing Time
- Image Preprocessing Time
- YOLOv8 Model Execution Time
- Postprocessing Time
- Response Preparation Time
- Total Server Processing Time
- Client API Round-Trip Time

All stage timings are measured using Python's `time.perf_counter()`.

### 8. Visualizations

The experiment generates the following visualizations:

**1. Original vs Annotated Image**

Displays the original uploaded image alongside the YOLOv8 detection output.

**2. Lifecycle Latency Breakdown**

A horizontal bar chart representing the execution time of each inference lifecycle stage.

**3. Latency Distribution**

A pie chart showing the percentage contribution of each lifecycle stage to the measured stage durations.

**4. Object Detection Confidence**

A bar chart displaying the confidence scores of detected objects.

### 9. Execution Procedure

1. Open the `SKILL_3_DLAC.ipynb` notebook in Google Colab.
2. Install the required Python dependencies.
3. Import the necessary libraries.
4. Configure the execution hardware.
5. Load the YOLOv8 Nano model.
6. Initialize the FastAPI application.
7. Start the API server.
8. Upload an input image.
9. Send the image to the `/predict` endpoint.
10. Execute the object detection pipeline.
11. Generate the inference request trace.
12. Visualize the latency measurements.
13. Save the annotated image and JSON trace report.

### 10. Generated Output Files

The experiment generates the following files:

| File Name | Description |
|---|---|
| `VisionPort_SKILL_3_Output.jpg` | Annotated object detection image |
| `VisionPort_SKILL_3_Trace.json` | Inference request trace report |

The JSON report contains:

- Project and experiment information.
- Request ID.
- Input filename.
- Model information.
- Execution hardware.
- Individual lifecycle stage timings.
- Total detected objects.
- Total server processing time.
- Client round-trip time.

### 11. Expected Results

After successful execution:

- FastAPI starts successfully.
- The YOLOv8 Nano model loads successfully.
- An input image is uploaded.
- Object detection is performed.
- Detected objects and confidence scores are extracted.
- Bounding boxes are generated.
- Inference request timestamps are recorded.
- Actual stage-wise latency is measured.
- Performance graphs are generated.
- Annotated output and JSON trace files are saved.

### 12. Conclusion

SKILL-3 successfully demonstrates the inference request lifecycle of the VISIONPORT deep learning object detection system.

By integrating FastAPI with YOLOv8, the experiment provides an API-based object detection pipeline with request tracing and performance measurement.

The system captures the execution time of individual lifecycle stages, helping analyze the processing overhead and identify performance-intensive components.

This experiment establishes a foundation for further optimization of deep learning inference systems.

---

**Project:** VISIONPORT – Deep Learning Object Detection  
**Experiment:** SKILL-3 – Inference Request Trace  
**Model:** YOLOv8 Nano  
**Environment:** Google Colab  
**Language:** Python
