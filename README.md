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
Random sample images from each class are visualized, offering a qualitative understanding of the data. 
These are the sample visualizations of the x-ray data images used in the project.
![image](https://github.com/SrkPrasadChangala/pneumoniaDetection/assets/77905636/b6be27d6-9e46-4863-b5cc-a0eb97b5e40f)
![image](https://github.com/SrkPrasadChangala/pneumoniaDetection/assets/77905636/f8c6e256-97ea-4b3e-bbca-2305cf0a93ad)

Class distribution is also visualized using a bar chart. It is as shown in the image given
![image](https://github.com/SrkPrasadChangala/pneumoniaDetection/assets/77905636/fb9c8cab-f247-44f2-ad27-3206b3cb6d1a)
As seen the dataset has a higher number of pneumonia images close to 4274 and lesser number of normal images which is close to 1583. Speaking in percentages, the dataset contains 72.9% of Pneumonia images and 27.1% of dataset contains normal images.


## 5. Image Size Analysis
Histograms analyze image size distributions (width and height), and sample images with labels showcase the dataset's diversity. The histograms indicate that image widths and heights in the dataset are normally distributed, peaking around 1250 and 1000 pixels respectively, with few images exceeding 2500 pixels in either dimension. This suggests that standardizing image sizes to a common dimension like 256x256 pixels for model input might be appropriate, balancing detail retention with computational efficiency.
![image](https://github.com/SrkPrasadChangala/pneumoniaDetection/assets/77905636/0370eaf5-459b-4b46-8356-182ca8ca0e27)


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
