# Summary week 2
Results of the notebook from lesson 2:

## 1. Study more layers to add
I have looked at the links provided:
- Dropout https://pytorch.org/docs/stable/generated/torch.nn.Dropout.html
- normalization layers https://pytorch.org/docs/stable/nn.html#normalization-layers

Especially the normalization layers are quite interesting. There are a lot of ways to normalize the layer. 

## 2. Results 03_mlflow.py
The model included in the original 03_mlflow.py has been run. The accuracy of the model is around 0.711. I also adjusted some paths in the code to organize the ran models a bit better. The other .py models will be based on this file.

## 3. Add dropout and normalization layers to your model

## 4. Use logging
In the 03_mlflow.py, I added some extra logging in the with mlflow.start_run():. This included the amount of epochs, used optimizer, learning rate, used device, mlflow.set_tag("device", device), and the model architecture.

Also made sure the logging is also tracked in the format of the TensorBoard and the TOML files.

## 5. Adding convolutional and pooling layers

Find the [instructions](./instructions.md)

[Go back to Homepage](../README.md
