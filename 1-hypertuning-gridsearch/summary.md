# Summary week 1
Results of the notebook from lesson 1:

## Change the number of epochs, eg to 5 or 10.
I expect that the accuracy of the model will increase when the amount of epochs increases.

I have changed the amount of epochs in the range from [5,8,10].

- When epochs=5 the accuracy is around 0.85-0.87;
- When epochs=8 the accuracy increases to 0.875;
- When epochs=10 the accuracy increases to 0.877.

The accuracy does increase when the amount of epochs are increased. The cost is the amount of time it takes to train the model.

## Changing the amount of units1 and units2 to values between 16 and 1024. Use factors of 2 to easily scan the ranges: 16, 32, 64, etc.
I expect that the accuracy of the model will increase when the amount of units increase. I think the model is more capable of understanding the underlying pattern with more units. 

I have trained the model with all combinations from [2**i for i in range(4, 11)] (16 - 1024).

Based on the results, I see a big increase in accuracy in the range from 16 to 256 units (from 0.845 to 0.869). The accuracy is going down when the units are pushed to 512/1024 (accuracy goes down to just above 0.86). The cut-off point is to 256 units. The models with more than 256 units are performing worse (probably because they are overfitting). These models also take a bit longer to train.

## Changing the batchsize to values between 4 and 128. Again, use factors of two for convenience.
I expect that the accuracy of the model will increase when the batchsize goes down. With a lower batchsize, the model has more samples to train with thus can detect the underlying pattern better.

I have changed the batchsize in the range from [4,32,124].

- When batchsize=128 the accuracy is 0.839;
- When batchsize=32 the accuracy is 0.8531;
- When batchsize=4 the accuracy is 0.8533.

The accuracy does increase when the batchsize goes down. The increase from batchsize 128 to 32 is quite a bit. The increase from 32 to 4 is really small at the cost that the batchsize=4 model took way longer than the batchsize=32 model. The optimal batchsize for this ranges of batchsizes is 32.

## Change the depth of your model by adding a additional linear layer + activation function
I expect that adding the additional linear layer + activation function will increase the accuracy of the model. The model is more capable of obtaining more linear regions. Because of the low units I expect that the model will not overfit by definition.

I added an extra linear layer and ReLU activation function. The units could be chosen from [16,32,64,128].

The maximal achieved accuracy is 0.867. This is lower compared to the model trained with 10 epochs above. The accuracy of 0.867 is achieved with 128, 128 and 16 units.

## Changing the learning rate to values between 1e-2 and 1e-5
I expect that the accuracy of the model will increase when the learning rate goes up. I also think there will be a cut-off point where the accuracy will go down when the learning rate goes up. I think there will be an optimal learning rate.

I have changed the learning rate in the range from [1e-2, 1e-3, 1e-4, 1e-5].

- When learningrate=1e-2 the accuracy is 0.855;
- When learningrate=1e-3 the accuracy is 0.857;
- When learningrate=1e-4 the accuracy is 0.807;
- When learningrate=1e-5 the accuracy is 0.651.

The accuracy increases when the learning rate goes up until 1e-3 (0.001). At the learning rate of 1e-2 (0.01), the learning rate goes down compared to 1e-3. The optimal learning rate is 1e-3.

## Changing the optimizer from SGD to one of the other available algoritms at [torch](https://pytorch.org/docs/stable/optim.html)
I expect that the Adam optimizer will perform best. Based on literature of the book "Understanding deep learning" the Adam model is quite popular and frequently used.

I have changed the optimizer to Adam, SGD, and RMSprop (Root Mean Square Propagation).

- When optimizer=Adam the accuracy is 0.855;
- When optimizer=SGD the accuracy is 0.784;
- When optimizer=RMSprop the accuracy is 0.824.

The Adam optimizer performs best with an accuracy of 0.855. Based on the literature, I expected this result. The SGD performs a lot worse compared the Adam. In between, RMSprop also performs slightly worse compared to Adam.

Find the [notebook](./notebook.ipynb) and the [instructions](./instructions.md)

[Go back to Homepage](../README.md)
