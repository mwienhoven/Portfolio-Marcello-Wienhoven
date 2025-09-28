# Summary week 3

## 1 Original model

The original GRU model of the original notebook had a accuracy of around 0.50-0.55 after running the notebook.

## 1.1 Increased epochs to 16

This model obtained an accuracy of 0.91, which is higher than the stated 90% that can be obtained. For the rest of the notebook, the 16 epochs stays the same.

## 1.2 Increased hidden size to 256

This model also obtained an accuracy of 0.91, which is the same as 1.1.

## 1.3 Decreased hidden size to 16

This model obtained an accuracy of 0.92, which is higher compared to 1.2 and 1.1. I will keep the hidden size of 16 in the model. The model could probably be slightly overfitted?

## 1.4 Added dropout of 0.2
This model obtained an accuracy of 0.89. This is lower compared to other models. The dropout made the model worse in this case.

## 1.5 Added dropout of 0.8
This model obtained an accuracy of 0.89. This is lower compared to other models. The dropout made the model worse in this case. The 0.89 is also the same as the dropout of 0.2.

[Go back to Homepage](../README.md)
