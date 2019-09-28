# Lung-Cancer-Classfication
Lung Cancer Classfication using various Pre-Trained models available in pytorch.
The code is written using Fastai library built on top of Pytorch.
Since the models used are pre trained, they are fine tuned for a 1000 class classification on ImageNet dataset. We wish to perform a two class 
classification so, the head of the CNN should be changed. i.e the last fully connected layers are modified to perform binary classification.
The weights of the model are not initialised randomly. Various state of the art techniques are used to improve the performance.
Main techniques are Learning rate finder, fit one cycle proposes by Leslie Smith, Discriminative Learning rates.
Before using Learning rate finder, we train the model for two or three epochs to get to a stable point on the loss landscape.
It was observed that the variation of loss during initial training process is very high and the loss jumps from one local minima to the other.
The initial training is done to reduce the variance of loss in later training. Rectified Adam optimizer is proposed to overcome this variance.

Various loss functions such as focal loss, tversky loss, hinge loss, weighted binary cross entropy were tested during the training process.
