# Credit card fraud detection - Autoencoder neural network architecture

Autoencoders are a special type of neural network architectures in which the output is same as the input. Autoencoders are
trained in an unsupervised manner in order to learn the exteremely low level repersentations of the input data. These low
level features are then deformed back to project the actual data. An autoencoder is a regression task where the network is
asked to predict its input (in other words, model the identity function). These networks has a tight bottleneck of a few
neurons in the middle, forcing them to create effective representations that compress the input into a low-dimensional code
that can be used by the decoder to reproduce the original input.


We will create an autoencoder model in which we only show the model non-fraud cases. The model will try to learn the best
representation of non-fraud cases. The same model will be used to generate the representations of fraud cases and we expect
them to be different from non-fraud ones.

We will use only 2000 rows of non fraud cases to train the autoencoder. Additionally, We do not need to run this model for a
large number of epochs.

The choice of small samples from the original dataset is based on the intuition that one class characteristics (non fraud)
will differ from that of the other (fraud). To distinguish these characteristics we need to show the autoencoders only one
class of data. This is because the autoencoder will try to learn only one class and automaticlly distiguish the other class.
