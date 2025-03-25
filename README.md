**Deep Learning Project: Brain Tumor Segmentation with Optimized Res-U-Net**
**Project Overview**
This repository contains the research paper and implementation details for a deep learning-based approach to brain tumor segmentation using multi-modal MRI scans. The project focuses on developing an optimized Res-U-Net model to accurately segment tumor regions, including the whole tumor, tumor core, and enhancing tumor, from the BraTS 2020 dataset. The goal is to improve early diagnosis and treatment planning for brain tumor patients.

**Key Features**

1.Dataset: Utilizes the BraTS 2020 dataset, which includes 1,845 MRI scans (369 training folders and 125 validation folders) with T1, T1ce, T2, and FLAIR modalities.

2.Models:

   Model 1: Res-U-Net without nearest neighbor interpolation.

   Model 2: Optimized Res-U-Net with nearest neighbor interpolation for improved segmentation accuracy.

3.Performance:

  Model 1: Training accuracy ~99%, validation accuracy ~96%.

  Model 2: Training accuracy ~99.5%, validation accuracy ~98%, test accuracy ~98.23%.

4.Segmentation Targets:

  Whole Tumor (WT)

  Tumor Core (TC)

  Enhancing Tumor (ET)

**Repository Structure**

DL PROJECT REPORT: Detailed research paper with methodology, results, and discussion.

Code snippets and architecture diagrams for model implementation (embedded in the report).

**How to Use**
  
  1.Dataset: Download the BraTS 2020 dataset and preprocess the MRI scans (NIfTI format).

  2.Model Training:

   Implement the Res-U-Net architecture as described in the report.
  
   Train the model using the provided data splits (80% training, 20% testing).

3.Evaluation: Use the trained model to segment tumor regions and evaluate performance using metrics like Dice Coefficient, accuracy, and loss.

4.Visualization: Generate segmentation masks and overlay them on original MRI scans for qualitative analysis.

**Dependencies**

1.Python 3.x

2.Libraries: TensorFlow/Keras, NumPy, Matplotlib, OpenCV, NiBabel (for NIfTI files).

3.Hardware: GPU recommended for faster training.

**Results**

Model 2 (Optimized Res-U-Net) outperformed Model 1, achieving:

Training Accuracy: 99.5%

Validation Accuracy: 98%

Test Accuracy: 98.23%

Dice Coefficients:

Whole Tumor: 0.87 (training), 0.43 (validation)

Enhancing Tumor: 0.78 (training), 0.47 (validation)

Necrotic Tumor: 0.77 (training), 0.37 (validation)

