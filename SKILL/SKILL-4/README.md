# VISIONPORT – Skill-4
## Project Repository, Git Workflow and PyTorch–CUDA Development Environment Setup

## 1. Overview

This experiment focuses on setting up a structured development environment for the VisionPort Deep Learning project. It demonstrates project repository creation, Git version control, PyTorch environment verification, CUDA availability checking, CNN model implementation, and CPU/GPU performance benchmarking.

The experiment uses a Convolutional Neural Network (CNN) to demonstrate deep learning model execution using PyTorch.

## 2. Objectives

- Create a structured VisionPort project repository.
- Organize project folders and essential files.
- Initialize and configure a Git repository.
- Perform Git add, commit, branch, and merge operations.
- Verify the Python and PyTorch environment.
- Check CUDA and GPU availability.
- Implement and execute a CNN model.
- Save the model weights.
- Measure CPU and GPU inference execution time.
- Visualize the project architecture and Git workflow.

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| PyTorch | Deep learning framework |
| CUDA | GPU acceleration |
| Git | Version control |
| Matplotlib | Data visualization |
| Google Colab | Development environment |
| CNN | Deep learning architecture |

## 4. Project Structure

```text
VisionPort/
│
├── app/
│
├── models/
│   └── model.py
│
├── inference/
│
├── preprocessing/
│
├── tests/
│
├── outputs/
│   └── visionport_model.pth
│
├── docs/
│   └── environment.txt
│
├── README.md
├── requirements.txt
└── .gitignore
```

## 5. Experiment Implementation

### Task 1: Project Repository Creation

Created the main VisionPort project directory and organized it into separate folders for application development, models, inference, preprocessing, testing, outputs, and documentation.

### Task 2: Project File Creation

Created the following essential files:

- `README.md` – Project documentation.
- `models/model.py` – CNN model implementation.
- `requirements.txt` – Required Python dependencies.
- `.gitignore` – Files excluded from Git tracking.

### Task 3: Git Version Control Workflow

Initialized a Git repository and configured the Git username and email.

Performed the following Git operations:

```bash
git init -b main
git config user.name "VisionPort Student"
git config user.email "student@example.com"

git add .
git commit -m "Initial VisionPort project setup"

git switch -c feature/environment-setup

git add .
git commit -m "Add development environment documentation"

git switch main
git merge --no-ff feature/environment-setup
```

This demonstrates repository initialization, staging, commits, feature branch creation, and branch merging.

### Task 4: PyTorch and CUDA Environment Verification

Verified the development environment using PyTorch.

Checked:

- Python version.
- Operating system.
- PyTorch version.
- CUDA availability.
- GPU name.
- CUDA version.
- GPU memory.

The execution device is selected automatically:

- CUDA GPU when available.
- CPU when CUDA is unavailable.

### Task 5: CNN Model Implementation

Implemented a Convolutional Neural Network using PyTorch.

The model contains:

- Convolutional layers.
- ReLU activation functions.
- Max pooling layers.
- Adaptive average pooling.
- Fully connected classification layer.

The model accepts RGB image tensors of shape:

```text
Batch Size: 4
Channels: 3
Height: 64
Width: 64
```

The model generates 10 output scores for each input image.

### Task 6: Model Execution and Saving

Executed the CNN using sample input data and generated prediction scores.

Saved the model parameters using:

```python
torch.save(
    model.state_dict(),
    "visionport_model.pth"
)
```

**Note:** The model uses randomly initialized weights and sample input data. It demonstrates inference execution but is not trained on a real dataset.

### Task 7: CPU and GPU Performance Benchmarking

Measured the average model execution time using CPU and, when available, CUDA GPU.

The benchmark performs warm-up iterations followed by repeated inference executions.

Execution time is calculated in milliseconds.

### Task 8: Architecture Visualization

Generated a graphical representation of the VisionPort workflow:

```text
Client
  ↓
FastAPI
  ↓
Preprocessing
  ↓
PyTorch Model
  ↓
GPU / CUDA
  ↓
Prediction
```

### Task 9: Performance Comparison

Generated a Matplotlib bar chart to compare average inference execution time between CPU and CUDA GPU, when CUDA is available.

### Task 10: Git Workflow Visualization

Created a graphical representation of the Git version control process:

```text
Working Directory
       ↓
   Staging Area
       ↓
 Local Repository
       ↓
  Feature Branch
       ↓
     Merge
       ↓
      Main
```

## 6. Expected Outputs

The experiment produces the following outputs:

1. VisionPort project directory structure.
2. Required project files.
3. Git repository initialization and commit history.
4. Main and feature branch information.
5. PyTorch and CUDA environment details.
6. CNN model architecture.
7. Input and prediction tensor shapes.
8. Saved model weights.
9. CPU/GPU execution time measurements.
10. Architecture, performance, and Git workflow diagrams.

## 7. Important Notes

- CUDA execution requires a compatible GPU runtime.
- If CUDA is unavailable, the experiment automatically executes using CPU.
- CPU and GPU performance can vary depending on hardware and runtime conditions.
- The CNN is a demonstration model and does not represent a trained production model.
- The Git repository is initialized locally. A GitHub remote and push operation are not configured in this experiment.

## 8. Result

Successfully created the VisionPort project repository, organized the project structure, performed Git version control operations, verified the PyTorch and CUDA development environment, implemented and executed a CNN model, saved the model weights, and performed CPU/GPU performance benchmarking.

The experiment demonstrates the essential development workflow required for a structured PyTorch-based deep learning project.

## 9. Conclusion

This experiment provided practical experience in repository management, Git branching and merging, deep learning environment configuration, PyTorch model development, CUDA verification, and performance benchmarking.

It establishes a foundation for developing and managing larger deep learning applications using the VisionPort project structure.
