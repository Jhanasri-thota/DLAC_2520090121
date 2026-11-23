# 🚦 VISIONPORT – Deep Learning Skill Lab
## SKILL-5: COCO Dataset Exploration – Indian Traffic Images, Categories and Bounding-Box Annotations

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![Dataset](https://img.shields.io/badge/Dataset-COCO128-green)
![Domain](https://img.shields.io/badge/Domain-Deep%20Learning-purple)

## 📌 1. Project Overview

VISIONPORT Skill-5 focuses on exploring the COCO128 dataset using Python and computer vision techniques.

The experiment analyzes traffic-related images, identifies relevant object categories, examines YOLO-format bounding-box annotations, and generates visual representations of the dataset.

The project demonstrates how object detection datasets can be explored and analyzed before training deep learning models.

## 🎯 2. Objectives

- Understand the structure of the COCO128 dataset.
- Upload and extract the dataset in Google Colab.
- Explore traffic-related images.
- Identify vehicle and road-related object categories.
- Read and interpret YOLO bounding-box annotations.
- Visualize images with bounding boxes.
- Analyze object category distributions.
- Generate statistical charts and reports.
- Export dataset analysis results into CSV and TXT files.

## 🛠️ 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Ultralytics | YOLO dataset support |
| OpenCV | Image processing |
| NumPy | Numerical operations |
| Pandas | Dataset analysis |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Pillow | Image processing |

## 📂 4. Dataset Information

**Dataset:** COCO128

COCO128 is a sample object-detection dataset containing 128 images with annotations covering 80 COCO object categories.

Dataset structure:

```text
coco128/
│
├── images/
│   └── train2017/
│       ├── image1.jpg
│       ├── image2.jpg
│       └── ...
│
└── labels/
    └── train2017/
        ├── image1.txt
        ├── image2.txt
        └── ...
```

Each image has a corresponding annotation file containing object class IDs and bounding-box coordinates.

## 🚗 5. Traffic-Related Categories

The experiment focuses on the following COCO categories:

| Class ID | Category |
|---|---|
| 0 | Person |
| 1 | Bicycle |
| 2 | Car |
| 3 | Motorcycle |
| 5 | Bus |
| 7 | Truck |
| 9 | Traffic Light |
| 11 | Stop Sign |
| 12 | Parking Meter |

These categories help explore road users, vehicles and traffic-related objects.

## 📦 6. Implementation Workflow

### Step 1: Library Installation
Install and import the required Python libraries.

### Step 2: Dataset Upload
Upload the COCO128 ZIP file using Google Colab's file upload interface.

### Step 3: Dataset Extraction
Extract the ZIP file and locate the image and annotation directories.

### Step 4: Image Exploration
Read dataset images and identify traffic-related objects.

### Step 5: Annotation Analysis
Read YOLO-format annotation files and extract:
- Class IDs
- Normalized center X coordinates
- Normalized center Y coordinates
- Bounding-box width
- Bounding-box height

### Step 6: Bounding-Box Visualization
Display traffic images with their corresponding bounding boxes and category labels.

### Step 7: Statistical Analysis
Analyze:
- Object category distribution
- Number of objects per image
- Bounding-box width distribution
- Bounding-box height distribution

### Step 8: Result Generation
Generate CSV files, statistical charts and a text report.

## 📊 7. Visualizations

The experiment generates the following visualizations:

1. Traffic image samples with bounding boxes.
2. Object category distribution bar chart.
3. Object category distribution pie chart.
4. Bounding-box width and height histogram.
5. Objects-per-image distribution histogram.

These visualizations help understand the distribution and characteristics of traffic-related objects.

## 📁 8. Output Files

The analysis results are saved in:

```text
traffic_analysis_results/
│
├── traffic_annotations.csv
├── traffic_category_summary.csv
└── traffic_dataset_report.txt
```

**File descriptions:**

- `traffic_annotations.csv` – Contains extracted object annotation details.
- `traffic_category_summary.csv` – Contains category-wise object statistics.
- `traffic_dataset_report.txt` – Contains the dataset analysis summary.

## 💻 9. Execution Environment

Platform: Google Colab

Execution steps:

1. Open the Skill-5 notebook in Google Colab.
2. Install the required dependencies.
3. Upload the COCO128 ZIP dataset.
4. Execute the notebook cells sequentially.
5. Observe the image visualizations and statistical charts.
6. Check the generated output directory.

## 📚 10. Learning Outcomes

After completing this experiment, we understand:

- COCO dataset organization and structure.
- Object detection annotation formats.
- YOLO bounding-box coordinate representation.
- Traffic-related object identification.
- Image visualization using Python.
- Exploratory data analysis for computer vision.
- Statistical analysis of object detection datasets.
- Exporting analysis results into CSV and text formats.

## ⚠️ 11. Dataset Limitation

COCO128 is a general-purpose object detection dataset. It is not exclusively an Indian traffic dataset.

The experiment focuses on traffic-related categories available in the dataset. Therefore, the selected images should not be assumed to represent exclusively Indian roads or traffic conditions.

## 👩‍💻 12. Project Information

**Project:** VISIONPORT – Deep Learning Skill Lab

**Skill:** Skill-5

**Experiment:** COCO Dataset Exploration – Indian Traffic Images, Categories and Bounding-Box Annotations

**Platform:** Google Colab

**Dataset:** COCO128

---

⭐ **VISIONPORT – Exploring Computer Vision Through Deep Learning**
