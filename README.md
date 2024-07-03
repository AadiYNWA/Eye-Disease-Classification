# Introduction
This project aims to propose a deep learning model which will be able to classify a given eye fundus image to be normal, cataract, DR or Glaucoma. We have used ShuffleNet V2 Architecture, which is pretrained on the ImageNet Dataset, and fine tune it for eye disease classification. The model was trained and tested on a publically available eye-fundus image dataset.

# Dataset
We used a open source dataset available on Kaggle which consisted of eye fundus images of 4 classes, namely Normal Eye, Cataract, Diabetic Retinopathy and Glaucoma. Our baseline model was trained on roughly 4000 images and presented an accuracy of 87%.

Dataset Link - https://www.kaggle.com/datasets/gunavenkatdoddi/eye-diseases-classification

# Methodology
We have proposed the following Augmentation Techniques to be performed on Eye-Fundus images:
* Cataract
  1. Gaussian Blur
  2. 30 degrees Rotation
  3. Horizontal Flip
* Glaucoma
  1. Grid Distortion
  2. 30 degrees Rotation
  3. Horizontal Flip
* Diabetic Retinopathy
  1. Drop Random Pixels
  2. 30 degrees Rotation
  3. Horizontal Flip

We have used ShufflNetV2 as the backbone architechture for the transfer learning model with pretrained weights from the imagenet dataset and is fine-tuned by adding additional fully-connected layers with the Adam optimizer during training.  

# Training

