# AICTE-Internship-crop-disease-detection-

This project was developed as part of the **Edunet Foundation AI Virtual Internship 2025**. The goal is to help farmers detect crop diseases using AI and receive advisory recommendations to improve crop health and yield.


##  Project Overview

This deep learning-based application detects diseases in crop leaves (such as tomato, potato, and pepper) using a pretrained CNN model (MobileNetV2) and provides advisory messages based on the diagnosis.

##  Dataset Used

Dataset Name: [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease)
  Classes: 15 plant conditions (healthy + various diseases)
  Source: Kaggle (emmarex/plantdisease)
  Format: Labeled images (RGB)

Model Architecture
Base Model**: `MobileNetV2` (Pretrained on ImageNet)
Custom Layers:
   Global Average Pooling
   Dense (128 units, ReLU)
   Output Layer (Softmax for 15 classes)

  Loss Function: categorical_crossentropy
  Optimizer: `Adam`
  Epochs Trained: 5
  Validation Accuracy: ~92.31%
 Testing the Model

Upload an image of a crop leaf and run it through the model using the provided `test_model(img_path)` function. The model will return:
  Predicted disease label
  An advisory message based on the result
Example Output
shell
Predicted Class: Tomato_Early_blight  
Advisory: ⚠️ Disease detected. Remove infected parts and apply recommended treatment.
