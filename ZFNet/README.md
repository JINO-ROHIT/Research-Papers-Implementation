# CAM - CLASS ACTIVATION MAPPING
The key idea of this research paper it to understand what the
model learns in the middle layers since the model interpretability
is very low and if the model fails, we have no clue why.

The central architecture is to use specific convolutional
neural network and produce *heat maps*.

## The architecture 
* Convolutional layers
* Global Average Pooling
* The last fully connected layer to predict the classes

In global average pooling, we sum the elements of the feature maps and divide by the total number of elements in the feature map.

Now to get the CAM Heatmap, instead of mutltiplying the weights with the numbers produced after Pooling on the filters, we multiply the weights directly by the feature maps. So instead of getting a single number , we get a grid of numbers that forms our HeatMap.
