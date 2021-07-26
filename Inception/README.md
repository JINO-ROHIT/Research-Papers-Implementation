# Inception v2

This paper talks about some upgrades that can be done to Inception v1(GoogLeNet) .
* Reduce representational bottleneck. Neural networks performed better when convolutions didn’t alter the dimensions of the input drastically. 
Reducing the dimensions too much may cause loss of information, known as a “representational bottleneck”
* By using some factorization methods , we can make convolutiona operations less expensive.

For example, the 5 x 5 convolutions are much expensive than two 3 x 3 convolutions. So replace the 5 x 5 and stack with two 3 x 3 convolution.
![1]()

Now if you have a convolution of n x n, , if you factorize it and do it 1 x n followed by n x 1, which is equivalent and much cheaper
![2]()

One last improvement that can be done is to make the filter banks more wider than deeper
![3]()
