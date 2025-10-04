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

[Go back to Homepage](../README.md)
