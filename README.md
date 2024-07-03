# Introduction
This project aims to propose a deep learning model which will be able to classify a given eye fundus image to be normal, cataract, DR or Glaucoma. We have used **Transfer Learning** of ShuffleNet V2 Architecture pretrained on the ImageNet Dataset and fine tune it for eye disease classification. The model was trained and tested on a publically available eye-fundus image dataset.

# Dataset
We used a open source dataset available on Kaggle which consisted of eye fundus images of 4 classes, namely Normal Eye, Cataract, Diabetic Retinopathy and Glaucoma. Our baseline model was trained on roughly 4000 images and presented an accuracy of 87%.

Dataset Link - https://www.kaggle.com/datasets/gunavenkatdoddi/eye-diseases-classification

# Methodology
We have proposed the following Augmentation Techniques to be performed on Eye-Fundus images. Augmentation was performed using Albumentations and Imgaug liabraries.

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

The pre-trained model is retrained using the augmented dataset. We added two fully connected layers and a softmax classifier for model to learn. Model is trained using Adam Optimiser and Cross Entropy Loss.

# Results
Model showed a training accuracy of 91%.

