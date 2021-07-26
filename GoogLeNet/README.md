# GoogLeNet

This architecture is also known as Inception v1. The central idea of this paper talks about using different size filters operating on the same layer with different dimension of images.
The outputs can then be cancatenated and pushed to the next level . This helps to make the network wider than deeper , called the Naive Inception. But more convolutions mean more 
mathematical operation and hence more computational cost right? So they also proposed to use 1 x 1 covolutions before the 3 x 3, 5 x 5 to reduce the channels. Although it seems
counter - intuitive that youre adding more operations to perform, 1 x 1 convolutions really works. They also made the switch from fully connected layers to average pooling at the
end of each inception module. Even though you have all this , the model is still deep with 22 layers and it becomes very hard to pass gradients with diminishing or exploding gradients
So they also proposed the use of auxillary classifier during training. Out of the 9 inception modules they had, two modules had softmaxes at the end of the layer and an *auxillary*
loss was calculated. So now instead of taking only the final loss at the end, we use the weighted sum of these auxillary losses as well. Remember , auxillary losses are just for
training and not for inference.
![module](inception_module.png)
