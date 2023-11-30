# Pneumonia Detection Model using X-ray Images

## Introduction
This project focuses on detecting pneumonia using X-ray images, employing Convolutional Neural Networks (CNNs) and transfer learning. The development process we used in this project is outlined below, highlighting the rationale and choices made during each step.

## 1. Dataset Acquisition
The dataset is obtained from an Amazon S3 bucket using the `wget` command, ensuring reliable and scalable access.

## 2. Module Import and Dataset Extraction
Relevant modules, including TensorFlow and data visualization tools, are imported. The dataset is extracted into a new folder ('xray_dataset') for easy access.
Stored the xray_dataset in this structure 
![image](https://github.com/SrkPrasadChangala/pneumoniaDetection/assets/77905636/7a807f94-5d4f-4f50-9878-c0c5fe604cd6)


## 3. Data Exploration
Image counts in each class (normal and pneumonia) for both training and test sets are calculated, providing insights into the dataset's distribution and size.
There a total of 5857 x-ray images in this dataset out of which
Images in train dataset
 	Normal Images: 1349 	 Pneumonia Images: 3884
Images in test dataset
 	Normal Images: 234 	 Pneumonia Images: 390 

## 4. Visualization
Random sample images from each class are visualized, offering a qualitative understanding of the data. Class distribution is also visualized using a bar chart.

## 5. Image Size Analysis
Histograms analyze image size distributions (width and height), and sample images with labels showcase the dataset's diversity.

## 6. Data Preprocessing
Directory paths, batch size, image size, and validation split are defined for data preprocessing. ImageDataGenerator is utilized for data augmentation and normalization.

## 7. Model Development (CNN)
A basic CNN model is developed with essential layers. The model is compiled with an Adam optimizer and binary crossentropy loss. Training is performed on the training set with validation on a subset.

## 8. Model Improvement (CNN with Data Augmentation)
Data augmentation is introduced for enhanced model generalization. Dropout is added for regularization, and the model is recompiled and trained with early stopping.

## 9. Transfer Learning (ResNet50)
The ResNet50 model, pretrained on ImageNet, is utilized with additional layers for pneumonia detection. The model is compiled, and training is performed with early stopping.

## 10. Model Evaluation
The performance of both the CNN and ResNet models is evaluated on the test set, reporting test accuracy for each model.

## Conclusion
The development process involves crucial steps such as dataset acquisition, exploration, visualization, preprocessing, model development, and evaluation. The use of both a basic CNN and a transfer learning approach (ResNet50) demonstrates the flexibility and adaptability in choosing models based on the project requirements. The final evaluation provides insights into the models' performance on previously unseen data, which is vital for real-world applications.
