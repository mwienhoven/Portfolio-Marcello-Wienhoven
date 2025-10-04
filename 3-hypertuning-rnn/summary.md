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

[Go back to Homepage](../README.md)
