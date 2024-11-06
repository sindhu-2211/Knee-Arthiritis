# Knee-Arthiritis
# Knee Arthritis Severity Classification using X-Ray Images
# Overview
This project focuses on automating knee arthritis severity classification through X-ray images. We utilize advanced feature extraction and classification algorithms to improve diagnostic accuracy, aiding early detection and assessment of arthritis severity levels.

# Dataset
Knee Osteoarthritis Dataset: Initially containing five classes. For this project, we focus on Classes 0, 3, and 4, balancing the dataset through data augmentation to ensure uniform representation across these categories.

# Methodology
# Data Preprocessing:
Resizing images to 224x224 pixels.
Normalizing pixel values using ImageNet's mean and standard deviation.

# Models Trained:
HOG + SVM: Histogram of Oriented Gradients (HOG) is used for feature extraction to capture essential shape information. Support Vector Machine (SVM) is applied on these features, achieving the highest validation accuracy of 81.78% and test accuracy of 82.80%.

Cascade Model: This model follows a cascading approach with EfficientNet -> ResNet -> DenseNet. If a prediction is incorrect, it falls back to the next model in sequence to handle the misclassification. This cascade improves accuracy through multiple model stages, leveraging the strengths of each model 

CBAM Model: In this approach, we used a combination of InceptionResNetV2, MobileNetV2, and EfficientNetB5, integrated with a Convolutional Block Attention Module (CBAM). CBAM applies channel and spatial attention, refining features for better classification performance. This model showed the highest accuracy across all approaches tested .

# Results
CBAM Model: Achieved the best performance, with high accuracy and a balanced classification across severity levels which is around 96.6%.
Cascade Model: Showed improved performance by leveraging a multi-stage classification process with around of 92.33%.
HOG + SVM: Provided robust accuracy, especially with simpler features, reaching 81.78% on validation and 82.80% on the test set.

# How to Run
Clone the repository.

Install dependencies with pip install -r requirements.txt.

# Train models:

HOG + SVM: python train_hog_svm.py

Cascade Model: python train_cascade_model.py

CBAM Model: python train_cbam_model.py

Evaluate models on the test set using: python evaluate_model.py

# Authors
Oladri Renuka
Bodapatla Sindhu Priya
Avula Jhansy
