# 🕵️ Melanoma detection with CNN
> In this assignment, we built a multiclass classification model using a custom convolutional neural network in TensorFlow.


## Table of Contents
* [General Info](#general-information)
* [Project Pipeline](#project-pipeline)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Contacts](#contact)

<!-- You can include any other section that is pertinent to your problem -->

## 💁 General Information


**Problem statement**: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion
- What is the dataset that is being used?

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## 💡 Project Pipeline

- Data Reading/Data Understanding → Defining the path for train and test images 
- Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
- Model Building & training : 
    - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
    - Choose an appropriate optimiser and loss function for model training
    - Train the model for ~20 epochs
    - Write your findings after the model fit. You must check if there is any evidence of model overfit or underfit.
- Chose an appropriate data augmentation strategy to resolve underfitting/overfitting 
- Model Building & training on the augmented data :
    - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
    - Choose an appropriate optimiser and loss function for model training
    - Train the model for ~20 epochs
- Write your findings after the model fit, see if the earlier issue is resolved or not?
- Class distribution: Examine the current class distribution in the training dataset 
    - Which class has the least number of samples?
    - Which classes dominate the data in terms of the proportionate number of samples?
- Handling class imbalances: Rectify class imbalances present in the training dataset with Augmentor library.
- Model Building & training on the rectified class imbalance data :
- Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~30 epochs
- Write your findings after the model fit, see if the issues are resolved or not?

## 🧠 Conclusions
- **M1 (Base Model)**
    - It is evident from the graph that the model is **overfitting** insanely with training accuracy of 0.8666 and validation accuracy of  0.4586.
    - It is performing excellent on training dataset but performance is poor on validation or unseen dataset.
    - It is clearly a bad model, and could be life threatening, need tackle this problem of overfitting.
- **M2 (With Augmentation)**
    - It is clearly visible that the problem of overfitting is not there as training accuracy is 0.5525 and validation accuracy is 0.4877.
    - Adding a Augmentation Layers handled the overfitting problem, but its not doing anything good either, as performance of model is degraded.
- **Model M3 (With Augmentation and Dropouts)**
    - There no improvement in model by adding dropouts
    - There is a slight decrease in training accuracy (0.4900) as well as validation accuracy (0.4676)
- **Model M4 (With Augmentation, Dropouts and CN layer)**
    - There is an improvement by adding an additional CN layer
    - traning accuracy increase to 0.5307 and validation accuracy increased to 0.5145
    - Moreover, there is no overfitting as traning and validatin are in close proximity
- **Model M5 With Augmentation, Dropouts, CN layer and Batch Normalization**
    - There is an increase in traning accuracy (0.5720) and a drop has been seen validation accuracy (0.4609).
- **Model After Rebalancing the sample in dataset**
    - As compared to all the previous model we have pretty satisfactory results: tranining accuracy of 0.6000 and validation accuracy of 0.5397.
    - Compared to Base Model with training accuracy of 0.8917 and validation accuracy of 0.4855 (**Overfitting**). There is no Overfitting noticed here as validation and traning accuracy are in close proximity or overlapping.
    - We can say that **CLASS REBALANCE** does help alot in training a CNN model.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## ⚙️ Technologies Used
- pandas
- numpy
- tensorflow
- keras
- matplotlib

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->


## 📞 Contact
Conducted by 

- [@gursewak96](https://github.com/gursewak9) - feel free to contact me! 🙋‍♂️
- [@ummefahad](https://github.com/ummefahad) - feel free to contact ! 🙋‍♀️
- [@Munawar-Ali-Sardar](https://github.com/Munawar-Ali-Sardar) - feel free to contact ! 🙋‍♂️


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
