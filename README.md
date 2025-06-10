##🧠 Mayo Clinic Strip AI – Classifying Stroke Blood Clot Origins from Whole Slide Pathology Images

###📌 Overview
Mayo Clinic Strip AI is a deep learning project focused on the classification of acute ischemic stroke (AIS) etiology using whole slide digital pathology images. This project implements a Modified VGG-16 (MVGG-16) model to differentiate between two major AIS subtypes:

Cardioembolic (CE)

Large Artery Atherosclerosis (LAA)

The data is sourced from the Kaggle Mayo Clinic STRIP AI Challenge, and the model helps in identifying the origin of blood clots for better post-stroke management.

###🔬 Research Motivation
Accurate determination of stroke etiology is critical for:

Tailoring medical interventions

Reducing chances of recurrence

Enhancing diagnostic workflows through automation

Traditional methods have limitations in speed and precision. This project aims to bridge that gap using digital pathology + AI.

###🧠 Methodology
####🗂 Dataset
Source: Mayo Clinic via Kaggle

Format: .tif whole slide pathology images

Classes: CE, LAA

Total: 754 training images

####🔄 Preprocessing
Artifact removal

Color normalization

Intensity scaling

Tissue/clot detection

####🏗️ Models Implemented
Model	Accuracy	Notes
VGG-11	Moderate	Baseline CNN model
VGG-16	Better	Captures more complex features
MVGG-16	Best	Custom layers + dropout + improved generalization

####MVGG-16 Enhancements:
Custom convolutional stacks

Dropout for regularization

Transfer learning from ImageNet

Improved robustness to variation in resolution/noise

###📈 Results
MVGG-16 outperforms both VGG-11 and VGG-16 on validation and test sets.

Training and validation graphs show better convergence and generalization.

