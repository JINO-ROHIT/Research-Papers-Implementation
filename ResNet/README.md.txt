In this , well talk about ResNet and why deeper layers arent always the best.
In the previous architecture Vgg16/19, it was shown that deeper layers helped
in learning more and more complex features and hence better accuracy. But this
works only in theory, why? because if the architecture has too many layers, 
the intermediate layers already learns the features and any further layer
added only degrades the performance.This was called the degradation problem
addressed in this paper. To combat this, they introduced the skip connections.
To explain this in simple terms, say for every two layers we can add the 
activation directly and skip the normal path it takes through the linear
path and activation functions and so on.

Consider x passed through first layer gives a[l] and second layer gives a[l+1],
third layer gives a[l+2]. Supposee our skip connection is from a[l] added to
a[l+2].
Consider the activation to be relu which is max(x,0) --gives only +ve values
we know
![latexeq](latex.png)

here now even if weight term becomes 0, we get the activation of layer l
which becomes an identity mapping and in this way even if the deeper
layers dont learn anything new , it retains the old information