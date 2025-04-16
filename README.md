# Eye Diseases Classification 👁️
## Introduction
Eye diseases are a leading cause of visual impairment and blindness worldwide, affecting millions of individuals and significantly impacting quality of life. Conditions such as diabetic retinopathy, glaucoma, age-related macular degeneration, and cataracts often develop gradually and may go unnoticed until irreversible damage has occurred. Early and accurate diagnosis is therefore essential for timely treatment and vision preservation. This project focuses on developing a system for eye disease classification, aiming to support ophthalmologists in identifying and differentiating between common eye conditions more efficiently and accurately. 

## Problem Statement
Despite the critical importance of early diagnosis, many eye diseases remain undetected until they reach advanced stages, often leading to irreversible vision loss or blindness. There is a growing need for an automated, reliable, and efficient system that can assist in the early detection and classification of common eye diseases. This project aims to address this gap by developing a machine learning-based solution capable of accurately classifying eye diseases from retinal images.

## Dataset
The dataset has 10 clasess: Diabetic Retinopathy, Glaucoma, Macular Scar, Optic Disc Edema, Central Serous Chorioretinopathy (CSCR), Retinal Detachment, Retinitis Pigmentosa, Myopia,Pterygium , and Healthy. The total of images 5335  were collected from Anwara Hamida Eye Hospital in Faridpur and BNS Zahrul Haque Eye Hospital in Faridpur district with the help of the hospital authorities. Then from these original images, a total of 15090 augmented images are produced by using brightness to adjusts the brightness of the input image to increase the number of data to make the dataset balance. The dataset can be downloaded here: https://data.mendeley.com/datasets/s9bfhswzjb/1
### Example 

![image](download.png)
 

## Model
The model is a deep learning architecture built for multi-class image classification. We use a pre-trained DenseNet121 as its feature extractor, which allows it to benefit from the rich feature representations learned from the large-scale ImageNet dataset. The input to the model is an image with shape (224, 224, 3), representing a standard-sized RGB image.
On top of the DenseNet121 base, the model includes normalization, dense layers, dropout for regularization, and a final softmax layer to classify the images into multiple categories. It is compiled with categorical cross-entropy loss and optimized using the Adamax optimizer with a low learning rate, ensuring stable convergence during training.
This design enables the model to effectively learn complex patterns in medical images while maintaining good generalization to new data.

## Results
The model was trained over 20 epochs, and the performance metrics at the final epoch indicate strong learning and generalization on the eye disease classification task:
Training Accuracy: 97.49%

Validation Accuracy: 92.67%

Test Accuracy: 92.91%

These results suggest that the model has effectively learned the features from the training data while maintaining strong generalization to unseen data. The close alignment between validation and test accuracy reflects a well-trained and balanced model with no overfitting.


### Prediction
![image](download2.png) 
![image](download3.png) 

## Demo
