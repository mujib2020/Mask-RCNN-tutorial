# Mask-RCNN-tutorial

## What is Mask R-CNN?

It is an extension of the Faster R-CNN object detection algorithm that adds an additional branch for predicting segmentation masks on each Region of Interest (RoI), in parallel with the existing branch for classification and bounding box regression. It is designed for the task of instance segmentation, which combines object detection and semantic segmentation.
 
- CNN – Convolutional Neural Network​
- R-CNN – Region-based Convolutional Neural Network​
- Faster R-CNN – Faster Region-based Convolutional Neural Network​
- Mask R-CNN – Mask (faster) Region-based Convolutional Neural Network​

As mentioned above, Mask R-CNN is built using Faster R-CNN​. In addition to class label and bounding box, Mask R-CNN outputs an object mask. ​Mask RCNN Uses a trick called ROIAlign to locate relevant areas down to pixel level. ​

## How Mask R-CNN works? 
Here's a breakdown of how it works:

**Backbone Network:** Mask R-CNN uses a backbone CNN for feature extraction from images. Common backbone architectures include ResNet or VGG.

**Region Proposal Network (RPN):** On top of the backbone, a Region Proposal Network proposes candidate object bounding boxes.

**RoI Pooling:** The proposed bounding boxes (or RoIs) are then pooled to a fixed size using an operation called RoI Align, which is an improvement over the RoI Pooling used in Faster R-CNN. RoI Align accurately preserves spatial information by avoiding any quantization, which is crucial for predicting pixel-accurate masks.

**Branches for Prediction:** For each RoI, three predictions are made:

- The class of the object.
- The bounding box offsets (to refine the RoI).
- The object mask, which is a binary mask that indicates the pixels where the object is present.
