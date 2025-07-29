# Graduation-Project
#**Project Overview**
This project presents an integrated AI-based pipeline for automated liver tumor diagnosis using 3D MRI scans and automated report generation with a Large Language Model (LLM). The pipeline combines traditional machine learning (SVM), deep learning (U-Net), and MONAI (Medical Open Network for AI) to enhance diagnostic efficiency, accuracy, and clinical interpretability.

Developed by students at Galala University under the Artificial Intelligence Science Program, the system achieves high diagnostic performance while addressing challenges like data heterogeneity, mask alignment, and computational load.

# **Objectives**
Automate liver tumor detection using MRI scans

Achieve accurate segmentation and classification with minimal expert intervention

Integrate a Large Language Model to generate structured medical reports

Develop a GUI and API for user-friendly clinical deployment

# **Project Structure & Workflow**
1. Data Collection & Preprocessing
Input: 3D MRI volumes in NIfTI format

Preprocessing steps:

Mask validation

Histogram clipping

Z-score intensity normalization

Volume resizing to 128×128×64

Bias field correction

Reorientation to a common anatomical frame

2. Model Development
SVM Phase:

Voxel-level classification

Feature extraction: intensity + normalized spatial coordinates

Slice selection based on tumor probability

U-Net Phase:

2D and 3D U-Net segmentation

Attention gates in 3D version

Trained using Dice + Focal loss

High Dice score: 0.9326, Mean IoU: ~0.88

3. Evaluation
Metrics used:

Dice Coefficient

Intersection over Union (IoU)

Pixel-wise accuracy

Precision / Recall for SVM

4. Deployment
GUI:

Upload MRI scan

Run prediction

Visualize segmentation output

API:

Facilitates model integration into external clinical systems

Report Generation:

MONAI-based LLM auto-generates medical reports

# **Contributions**
Developed by the MediCS Team:

Sondos Ahmed Ghoneim

Hazem Almohamdy

Ali Sherif

Kareem Abdelaziz

Loay Hassan

Ahmed Hany
