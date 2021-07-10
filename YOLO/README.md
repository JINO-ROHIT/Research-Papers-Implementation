# You Only Look Once(YOLO)

This is an object detection model that gives predictions real time with only
a single look. It first divides the image into s*s grid, where each grid predicts
only a single object. The boundary box has (x-cordinate, y-cordinate, width,
height, confidence score). They normalized the box by dividing with image 
width and height. To chose the best bounding box among multiple boxes, it
use Intersection Over Union. Here, it is taken as a regression task and sum
squared error is used as a metric. Now, since majority of the grids have empty
predictions, there will be a class imbalance so they weigh down the loss factor
for those grids. 
