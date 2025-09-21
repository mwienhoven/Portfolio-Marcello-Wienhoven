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

## Changing the learningrate to values between 1e-2 and 1e-5

## Changing the optimizer from SGD to one of the other available algoritms at [torch](https://pytorch.org/docs/stable/optim.html)

Find the [notebook](./notebook.ipynb) and the [instructions](./instructions.md)

[Go back to Homepage](../README.md)
