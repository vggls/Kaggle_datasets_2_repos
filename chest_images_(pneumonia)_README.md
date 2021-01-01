In this repo we build classifiers for the following Kaggle dataset : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia ,
which consists of 5863 chest x-ray images of people who suffer from pneumonia and of healthy people.

The code file is structured as follows :

1) **We explore the dataset**

2) **1st classifier : CNN model with Image Augmentation**

     2.1) Build the augmented image set
                  
     2.2) The model : We train on the augmented image set a hyper-tuned classifier which consists of a sequence of CNN and DNN layers.
                  
     2.3) Model evaluation (learning curves, predictions on unseen data & confusion matrix)

3) **2nd classifier : Use CNN layers of pre-trained ResnetNN for feature extraction.**

     3.1) The model : We train a DNN classifier on the features obtained by the resnet model
                  
     3.2) Model evaluation (learning curves, predictions on unseen data & confusion matrix) 
                  
4) **Summary of the aforementioned classifiers**

We make remarks on the learning curves and the accuracy of the models over unseen data.

Overall, as expected, we see that **the model with the pre-trained layers performs better** with respect to all performance metrics.

5) **Additional material to be added in the future**

  - We are going to build a **3rd classifier** by **fine-tuning a pre-trained ResnetNN**. More specifically, we will adapt a DNN   classifier on the top of the CNN layers and we will train the last (already pre-trained) CNN layers along with the DNN layers.

  - We will deal with the overfitting signs of the **2nd classifier** by adding a **regularization term** in an attempt to improve its performance even more.
