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
* HOG + SVM: Histogram of Oriented Gradients (HOG) is used for feature extraction to capture essential shape information. Support Vector Machine (SVM) is applied 
  on these features, achieving the highest validation accuracy of 81.78% and test accuracy of 82.80%.

* Cascade Model: This model follows a cascading approach with EfficientNet -> ResNet -> DenseNet. If a prediction is incorrect, it falls back to the next model in 
  sequence to handle the misclassification. This cascade improves accuracy through multiple model stages, leveraging the strengths of each model 

* CBAM Model: In this approach, we used a combination of InceptionResNetV2, MobileNetV2, and EfficientNetB5, integrated with a Convolutional Block Attention 
  Module (CBAM). CBAM applies channel and spatial attention, refining features for better classification performance. This model showed the highest accuracy 
  across all approaches tested .

# Results
* CBAM Model: 98.20% on Train set and 96.60% on test set

* Cascade Model: 92.33% on test set and 91.99% on validation set

* HOG + SVM:  85.68% on validation and 84.01% on the test set.


# Authors
Oladri Renuka

Bodapatla Sindhu Priya

Avula Jhansy
