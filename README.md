🧠 Mayo Clinic Strip AI – Classifying Stroke Blood Clot Origins from Whole Slide Pathology Images
This project, Mayo Clinic Strip AI, uses deep learning to classify the etiology of acute ischemic stroke (AIS) by analyzing whole slide digital pathology images. It employs a Modified VGG-16 (MVGG-16) model to distinguish between two primary AIS subtypes: Cardioembolic (CE) and Large Artery Atherosclerosis (LAA). The data comes from the Kaggle Mayo Clinic STRIP AI Challenge, and the model aims to help identify the origin of blood clots for improved post-stroke care.

🔬 Research Motivation
Accurately determining stroke etiology is crucial for:

Tailoring medical interventions
Reducing chances of recurrence
Enhancing diagnostic workflows through automation
Traditional methods often lack speed and precision. This project seeks to bridge that gap by integrating digital pathology with AI.

🧠 Methodology
🗂 Dataset
Source: Mayo Clinic via Kaggle
Format: .tif whole slide pathology images
Classes: CE, LAA
Total: 754 training images
🔄 Preprocessing
Artifact removal
Color normalization
Intensity scaling
Tissue/clot detection
🏗️ Models Implemented
Model	Accuracy	Notes
VGG-11	Moderate	Baseline CNN model
VGG-16	Better	Captures more complex features
MVGG-16	Best	Custom layers + dropout + improved generalization

Export to Sheets
MVGG-16 Enhancements:

Custom convolutional stacks
Dropout for regularization
Transfer learning from ImageNet
Improved robustness to variation in resolution/noise
📈 Results
The MVGG-16 model consistently outperforms both VGG-11 and VGG-16 on validation and test sets. Training and validation graphs demonstrate superior convergence and generalization for MVGG-16.

✅ Key Features
Full pipeline: preprocessing → feature extraction → classification
Modular design using Keras + transfer learning
High accuracy on digital pathology tasks
Easily extendable to other medical image datasets
🙏 Acknowledgments
Mayo Clinic for providing the dataset via Kaggle.
The original VGG architectures by Visual Geometry Group, Oxford.
Inspired by clinical needs for rapid stroke etiology classification.
