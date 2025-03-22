# Medical Image Segmentation: Deep Learning Exploration
The goal of this project is to develop and analyze deep learning models for medical image segmentation. Using the Kvasir-Instrument dataset, we evaluate the effectiveness of various segmentation models and techniques. The project is structured into phases to ensure thorough experimentation and analysis.

---
## Dataset: Kvasir-Instrument
The [Kvasir-Instrument dataset](https://datasets.simula.no/kvasir-instrument/) (size: 170 MB) contains:
- **590 endoscopic tool images** with corresponding ground truth masks.
- Image resolutions ranging from **720x576 to 1280x1024**.
- Image files encoded using **JPEG compression**.

---


## Project Workflow

### 1. Setup & Data Preparation
- Form a team with clear roles (e.g., project manager, data scientist, developer).
- Download the **Kvasir-Instrument dataset**.
- Explore and understand the dataset, focusing on image formats, resolutions, and train/test splits.
- Choose a baseline segmentation model (e.g., **DeepLabV3+**).
- Set up the development environment and install the necessary libraries and dependencies.

---

### 2. Model Selection
Models under consideration:
- [DUCK-Net](https://github.com/SJTUzhou/DUCK-Net-3D-Pytorch)
- [SwinV2 Transformer](https://github.com/KerrFitzgerald/Polyp_FCB-SwinV2Transformer/blob/main/Train_FCBSwinV2Transformer.ipynb)
- [EfficientNet](https://github.com/lukemelas/EfficientNet-PyTorch)
- Other state-of-the-art models: [Papers with Code - Kvasir Segmentation](https://paperswithcode.com/sota/medical-image-segmentation-on-kvasir-seg)

---

### 3. Experiments
#### Experiment 1: Image Resolution
- Define multiple resolution levels for testing.
- Adapt preprocessing functions to include resizing.
- Train and evaluate the model at each resolution.

#### Experiment 2: Data Augmentation
- Apply augmentation techniques using libraries like Albumentations.
- Train models with and without augmentation for comparison.

#### Experiment 3: Training Data Size
- Create subsets of the dataset to evaluate the impact of training data size.
- Train and analyze model performance on these subsets.

#### Experiment 4: Optimization Methods
- Compare various optimizers (e.g., Adam, SGD).
- Train models using each optimizer and analyze their impact.

#### Experiment 5: Activation Functions
- Test multiple activation functions in the model architecture.
- Train models with each function and evaluate their impact on predictions.

---

### 4. Implementation Techniques
- **Learning Rate Scheduler**: Utilize tools like `StepLR` for efficient training.
- **Early Stopping**: Implement criteria to halt training when performance plateaus.

---

### 5. Evaluation Metrics
Key metrics for performance evaluation:
- **Dice Similarity Coefficient (DSC)**
- **Jaccard Index (IoU)**
- **Precision, Recall, and Overall Accuracy**
- **Average Precision (AP)** at IoU threshold 50
- **Overall IoU**

---

### 6. Analysis and Reporting
- Record all experimental results, including metrics and observations.
- Visualize findings through tables and graphs.
- Compile a comprehensive report summarizing methodologies, results, and insights.



