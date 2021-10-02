## Conceptual overview
Input windows X(shape=[batch size, #time steps, #dims]) -> Recurrent Layer -> Recurrent Layer -> Dense Layer -> Forecasts

## Shape of the inputs to RNN
![image](/pic/rnn.png)

## Outputting a sequence
![image](/pic/rnn2.png)
input_shape = [None, 1]: TF assuems that the first dimension is the batch size, that it can have any size at all, the next dimension the is the number of timestamps, which we can set to None, which means that the RNN can handle sequences of any length. The last dimension is just one because we're using a unit vary of time series.

## Lambda layers
![image](/pic/rnn3.png)
- Lambda layer: performs arbitrary operations to effectively expand the functionality of TensorFlow's kares
- Lambda layer1: using lambda we expand the array by one dimension by setting input shape to none, we're saying that the model can take sequences of any length
- Lambda layer2: if we scale up the ouputs by 100 we can help training, the default activation function in RNN layer is tan H which is the hyperbolic tangent activation, this outpus values between negative one and one, since the time seriese values are in that order usually in the 10s like 40s, 50s, 70s, then scaling up the outputs to the same ballpark can help us with learning
