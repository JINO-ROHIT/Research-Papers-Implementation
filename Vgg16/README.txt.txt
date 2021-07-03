# Vgg16

The Vgg16 talks about the waste of computation using Local
Reponse Normalisation and it had no added advantage either. The accuracy was more or less the same and even worse off.
In this architecture, they prove by using a (3,3) filters instead of the previous (11,11) or (7,7) filters with non linear activations
at each layer performed way better and even converges faster with less training time. This shows the importance of depth in image based
tasks even when you can address the overfitting properly.

## The Architecture
![arch](vgg16.png)