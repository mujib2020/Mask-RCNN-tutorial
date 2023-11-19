# Mask-RCNN-tutorial

## What is Mask R-CNN?

It is an extension of the Faster R-CNN object detection algorithm that adds an additional branch for predicting segmentation masks on each Region of Interest (RoI), in parallel with the existing branch for classification and bounding box regression. It is designed for the task of instance segmentation, which combines object detection and semantic segmentation.
 
- CNN – Convolutional Neural Network​
- R-CNN – Region-based Convolutional Neural Network​
- Faster R-CNN – Faster Region-based Convolutional Neural Network​
- Mask R-CNN – Mask (faster) Region-based Convolutional Neural Network​

As mentioned above, Mask R-CNN is built using Faster R-CNN​. In addition to class label and bounding box, Mask R-CNN outputs an object mask. ​Mask RCNN Uses a trick called ROIAlign to locate relevant areas down to pixel level. ​
