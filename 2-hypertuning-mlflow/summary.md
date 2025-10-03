# Summary week 2
Results of the notebook from lesson 2:

## 1. Study more layers to add
I have looked at the links provided:
- Dropout https://pytorch.org/docs/stable/generated/torch.nn.Dropout.html
- normalization layers https://pytorch.org/docs/stable/nn.html#normalization-layers

Especially the normalization layers are quite interesting. There are a lot of ways to normalize the layer. 

## 2. Results 03_mlflow.py

### 2.1 Original 3 epochs
The model included in the original 03_mlflow.py has been run. The accuracy of the model is around 0.711. I also adjusted some paths in the code to organize the ran models a bit better. The other .py models will be based on this file.

### 2.2 Increased epochs to 12
I increased the epochs to 12 to see how long it took. Every run now takes a few minutes. The accuracy has increased a lot.

The accuracy is now across the 3 trained models between 0.83, 0.78, and 0.77. The differences between the loss\train and loss\test are quite small (max 0.02). This means the models are not overfitting.

## 3. Add dropout and normalization layers to your model

## 3.1 Original 3 epochs
### 3.1.1 Dropout
I added two Dropout layers (both probability of 0.5). They are added at the last linear and conv2d layer before the output layer as mentioned in the instructions. I ran 9 models.

I see in mlflow that most of the models have an accuracy around 0.66. The ranges of accuracies vary between 0.64-0.70. These models perform worse compared to the models without dropout.

### 3.1.2 Normalization
I added an BatchNorm1d layer after the linear layers but not the output in the sequential layer. I ran 9 models.

Most of the models in mlflow have a lower accuracy compared to the 0.71. I see accuracies in the range from 0.40 to 0.70. The mean of the ran models will be around 0.57. These models perform worse compared the the models without normalization.

## 3.2 Increased epochs to 12
### 3.2.1 Dropout
The dropout is added before the last ReLU function in the Sequential layers. So after dropout only the ReLU and final linear layer. Dropout is tested for 0.5, 0.2, and 0.8

#### Dropout of 0.5
The accuracies of the three models are 0.84, 0.81, and 0.78. I notice that the losses between train and test are higher. The differences are now between 0.5 and 0.6 now. The differences are probably from the better generalization that is expected from dropout. Some neurons now learn more independently from other neurons. So this is what I expected.

#### Dropout of 0.2
The accuracies of the three models are 0.78, 0.77, and 0.78. The accuracies are quite lower than the dropout of 0.59. The differences of the train and test loss are now smaller (below 0.01) in two of the three ran models, because less neurons are deactivated in every run. So this is what I expected. 

#### Dropout of 0.8
The accuracies of the three models are 0.71, 0.70, and 0.77. The accuracies are the lowest of all the dropouts. The model is now underfitting the data. The differences between train and test are really big (0.13 to 0.40). The model learns to little because a lot of neurons are deactivated in every run.

## 4. Use logging
In the 03_mlflow.py, I added some extra logging in the with mlflow.start_run():. This included the amount of epochs, used optimizer, learning rate, used device, mlflow.set_tag("device", device), and the model architecture.

Also made sure the logging is also tracked in the format of the TensorBoard and the TOML files.

## 5. Adding convolutional and pooling layers
I one extra layer of Conv2d (including ReLU) and removed 1 pooling layer.

Most of the models in mlflow have a lower accuracy compared to the 0.71. I see accuracies in the range from 0.56 to 0.69. The mean of the ran models will be around 0.65. These models perform worst compared to the models without changing the layers.

[Go back to Homepage](../README.md)
