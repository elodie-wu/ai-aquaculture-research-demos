# 🐟 Salmon Health Classification

This project explores salmon health classification using a simple Convolutional Neural Network (CNN).

The goal is to classify salmon images into two classes:

- `FreshFish`
- `InfectedFish`

## 📊 Dataset

**Dataset:** SalmonScan

The dataset contains:

- 456 FreshFish images
- 752 InfectedFish images
- 1208 images in total

The images were divided into training, validation, and test sets.

## 🎯 Project Goal

This project investigates whether a simple CNN can distinguish fresh salmon from infected salmon using image features.

The project also uses Grad-CAM to explore which image regions influence the model's predictions.

## 🧠 Method

The workflow includes:

- image resizing and normalization
- train / validation / test split
- Simple CNN classification
- model validation and best-model selection
- test-set evaluation
- confusion matrix analysis
- misclassification analysis
- Grad-CAM visualisation

### Simple CNN Structure

The CNN contains:

- two convolutional layers
- ReLU activation
- max pooling
- two fully connected layers

The model learns image features and predicts whether a salmon image belongs to the FreshFish or InfectedFish class.

## 📈 Main Results

The Simple CNN achieved:

- **Test Accuracy:** 0.9396
- **Precision:** 0.9204
- **Recall:** 0.9811
- **F1 Score:** 0.9498

The high recall means that most infected fish were correctly detected.

### Confusion Matrix

The model classified:

- 67 FreshFish correctly
- 104 InfectedFish correctly
- 9 FreshFish as InfectedFish
- 2 InfectedFish as FreshFish

Only a small number of infected fish were missed.

## 🔍 Error Analysis

Some FreshFish and InfectedFish images look very similar.

The misclassified samples suggest that colour, texture, lighting, and other visual patterns may influence the model's predictions.

## 🔥 Grad-CAM Analysis

Grad-CAM was used to visualise which image regions influenced the CNN predictions.

For correctly classified infected fish, the model often focused on local regions of the fish body.

However, some predictions also showed attention on background or non-disease visual patterns.

This suggests that the CNN may not always rely only on disease-related features.

## ⚠️ Limitations

- The dataset is relatively small.
- The two classes are not perfectly balanced.
- Some fresh and infected fish look visually similar.
- The model may learn background or image-specific patterns.
- The dataset only contains two classes, so the model cannot identify specific fish diseases.

## 🚀 Future Work

Possible future improvements include:

- using data augmentation to improve generalisation
- comparing the Simple CNN with transfer learning models such as ResNet18
- testing the model on New Zealand Chinook salmon images
- extending the task to specific fish-disease classification
- using larger and more diverse aquaculture image datasets
- exploring anomaly detection using healthy fish images as the normal class

## 🛠 Technologies

Python, PyTorch, Torchvision, Scikit-learn, NumPy, Matplotlib, OpenCV
