# Summary week 3

## 1 First ran experiments
## 1.1 Original model

The original GRU model of the original notebook had a accuracy of around 0.50-0.55 after running the notebook.

## 1.2 Increased epochs to 16

This model obtained an accuracy of 0.91, which is higher than the stated 90% that can be obtained. For the rest of the notebook, the 16 epochs stays the same.

## 1.3 Increased hidden size to 256

This model also obtained an accuracy of 0.91, which is the same as 1.1.

## 1.4 Decreased hidden size to 16

This model obtained an accuracy of 0.92, which is higher compared to 1.2 and 1.1. I will keep the hidden size of 16 in the model. The model could probably be slightly overfitted?

## 1.5 Added dropout of 0.2
This model obtained an accuracy of 0.89. This is lower compared to other models. The dropout made the model worse in this case.

## 1.6 Added dropout of 0.8
This model obtained an accuracy of 0.89. This is lower compared to other models. The dropout made the model worse in this case. The 0.89 is also the same as the dropout of 0.2.

## 1.7 Added conv1d layer
This model obtained an accuracy of 0.89-0.91 with different runs. This is quite good and can be higher than the stated 90% in the assignment. I will keep the conv1d layer in the model.

## 1.8 Increased num layers to 3
This model obtained an accuracy of 0.9656. This is really high. Is this model not overfitting?

## 2 Second ran experiments
## 2.1 Original model

The original models obtain an accuracy of around 0.26 to 0.31. The model did not have enough epochs to update the weights. The model is underfitting extremely.

## 2.2 Increased epochs to 16

The models now obtain an accuracy of 0.92 to 0.94. This is really high! I notice that the loss of the test is always higher than the train. This could potentially be a sign of overfitting. These models are a great upgrade compared to the original epochs=3. The models have enough epochs to train the models.

## 2.3 Changed dropout

The dropout of the models will be varied to 0.5, 0.2, and 0.8 to see the effect of the dropout. The dropout of 0.5 will be kept in future models.

### 2.3.1 Dropout of 0.5

The models now obtain an accuracy of 0.91 to 0.94. I notice that in 2/3 models the train loss is higher than the test loss. This could indicate that the model is generalising better now. This is expected of course with dropout, because the neurons now are partly deactivated and receive input from different neurons at every run.

### 2.3.2 Dropout of 0.2

The models now obtain an accuracy of 0.90 to 0.94. I noticed the best models were not saved, but only the last epoch. I changed this setting from now on. The differences of the test and train losses are slightly higher compared to dropout of 0.5. Less neurons are deactivated and that means the neurons can potentially les generalize this way.

### 2.3.3 Dropout of 0.8

The models now obtain an accuracy of 0.90, 0.93, and 0.95. The accuracy of 0.95 is the highest yet! However, the differences of the test and train losses are really high in all the models (differences of 0.08 - 0.11 (with absolute errors of 0.30 - 0.45)). This means the models are less generalizing and probably are overfitting. A lot of neurons are deactivated every run.

## 2.4 Changed hidden size

The hidden size will be changed to 32, 128, and 256. The original hidden size in the experiments before are 64. In the upcoming experiments, the hidden size of 128 will be used

### 2.4.1 Hidden size of 32

The models now obtain an accuracy of 0.61 to 0.68. This means the models are really bad compared to earlier models. The models are underfitting extremely. 32 neurons per layer is just not enough to capture the hidden relationship. These models also took a lot less time to train, because less calculations had to be made.

### 2.4.2 Hidden size of 128

The models now obtain an accuracy of 0.96 to 0.99 (0.9906 max). These are the highest accuracies so far! The models also took longer to train because there are more calculations to perform. The differences between the train and test loss are also quite small.

### 2.4.3 Hidden size of 256

The models now obtain an accuracy of 0.98 and 0.99. The models took again longer compared to hidden size of 128 because of the added neurons and calculations. The losses of the train are now almost zero, meaning the models are overfitting now.

## 2.5 Change learning rate

The learning rate will be changed from the original 0.001 to 0.0001, 0.01, 0.1, and 1. The models with an learning rate of 0.001 and 0.01 perform quite well. All the other learning rates are just not performing well. Future experiments will be done with the original learning rate of 0.001.

### 2.5.1 Learning rate of 0.0001

These models are just really bad. Accuracies of 0.28 to 0.32. The models were just not updating because the learning rate is way too low.

### 2.5.2 Learning rate of 0.01

These models obtain an accuracy of around 0.97 and 0.98. These models are just comparable with the original learning rate of 0.001. The differences are really small.

### 2.5.3 Learning rate of 0.1
These models are just bad. Accuracies of 0.57, 0.46, and 0.41. 

### 2.5.4 Learning rate of 1
These models are just bad. Accuracies of 0.34, 0.45, and 0.38. These models are even worse as the models with learning rate of 0.1.

## 2.6 Changing the batchsize
The batchsize will be changed from 32 to 4, 16, and 64. The models mostly performed better at an lower batchsize. For the future models, a batchsize of 16 will be used (only 2.7.1 has a batchsize of 4).

### 2.6.1 Batchsize of 4
The models now obtain an accuracy of 0.994, 0.990, and 0.994. I notice that these models take a lot longer (3 min compared to earlier 30 seconds) to train. This is logical, because the models has more samples to train per epoch because the batchsize is smaller. Also the differences in train and test loss is really small, so the model generalizes well.

### 2.6.2 Batchsize of 16
The models now obtain an accuracy of 0.98, 0.98, and 0.985. I notice that the models took a bit longer compared to batchsize of 32 (same reasoning as in 2.6.1). The differences in train and test loss are bigger, model less generalizes.

### 2.6.3 Batchsize of 64
The models took a lot less time to train. The model has less samples of batches per epoch. The models obtain an accuracy of 0.94, 0.95, and 0.94. These models perform less than all other models in 2.6.

## 2.7 Changing number of layers
The number of layers will be changed from 1 to 3,5,7. I only did 2.7.1 with batch 4, the rest is with batch 16.

### 2.7.1 Number of layers of 3
This model tooks the longest to train. This is logical because of the more needed calculations to perform (more weights). The models obtain an accuracy of 0.994, 0.992, and 0.995. Also the losses between train and test are small (but slightly increased compared to number of layers = 1).

### 2.7.2 Number of layers of 5
The models also take longer to train when increasing the number of layers. The models obtain an accuracy of 0.994, 0.985, and 0.995. Differences in train and test loss are quite small. 

### 2.7.3 Number of layers of 7
The models now take longer to train and also achieve less acurracy. I stopped after one model.

## 2.8 LSTM model
I want to compare the model in 2.4.2 to the LSTM. I modelled the LSTM model in the notebook notebook_epoch16_drop0.5_hidsize128_LSTM.ipynb.


[Go back to Homepage](../README.md)
