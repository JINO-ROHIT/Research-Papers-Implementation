# DCGAN
The DCGAN is a class of CNNs called deep convolutional generative adversarial networks that was introduced for more training stability and faster convergence.

## The Architecture Guidelines by Ian Good fellow
* Replace any pooling layers with strided convolutions (discriminator) and fractional-strided convolutions (generator).
* Use batchnorm in both the generator and the discriminator.
* Remove fully connected hidden layers for deeper architecture.
* Use ReLU activation in generator for all layers except for the output, which uses Tanh.
* Use LeakyReLU activation in the discriminator for all layers.

