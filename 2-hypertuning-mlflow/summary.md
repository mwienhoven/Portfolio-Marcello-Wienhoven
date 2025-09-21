# Summary week 2
Results of the notebook from lesson 2:

## 1. Study more layers to add
I have looked at the links provided:
- Dropout https://pytorch.org/docs/stable/generated/torch.nn.Dropout.html
- normalization layers https://pytorch.org/docs/stable/nn.html#normalization-layers

Especially the normalization layers are quite interesting. There are a lot of ways to normalize the layer. 

## 2. Add dropout and normalization layers to your model

## 3. Use logging
In the 03_mlflow.py, I added some extra logging in the with mlflow.start_run():. This included the amount of epochs, used optimizer, learning rate, used device, mlflow.set_tag("device", device), and the model architecture.

## 4. Adding convolutional and pooling layers

Find the [instructions](./instructions.md)

[Go back to Homepage](../README.md
