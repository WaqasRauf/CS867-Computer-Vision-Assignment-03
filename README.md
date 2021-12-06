# CS867-Computer-Vision-Assignment-03
Semantic Segmentation


Semantic image segmentation is the task of classifying each pixel in an image from a predefined set of classes. In the following example, different entities are classified.

<p align="center">
  <img src="sample_images/1_input.jpg" width="350" title="hover text">
  <img src="sample_images/1_output.png" width="350" alt="accessibility text">
</p>

In the above example, the pixels belonging to the bed are classified in the class “bed”, the pixels corresponding to the walls are labeled as “wall”, etc.
In particular, our goal is to take an image of size W x H x 3 and generate a W x H matrix containing the predicted class ID’s corresponding to all the pixels.

<p align="center">
  <img src="sample_images/3_input.jpg" width="350" title="accessibility text">
</p>

Usually in an image with various entities, we want to know which pixel belongs to which entity, For example in an outdoor image, we can segment the sky, ground, trees, people, etc.

Semantic segmentation is different from object detection as it does not predict any bounding boxes around the objects. We do not distinguish between different instances of the same object. For example, there could be multiple cars in the scene and all of them would have the same label.

In order to perform semantic segmentation, a higher level understanding of the image is required. The algorithm should figure out the objects present and also the pixels which correspond to the object. Semantic segmentation is one of the essential tasks for complete scene understanding.

## Datasets for semantic segmentation

The first step in training our segmentation model is to prepare the dataset. We would need the input RGB images and the corresponding segmentation images. If you want to make your own dataset, a tool like labelme or GIMP can be used to manually generate the ground truth segmentation masks.

Assign each class a unique ID. In the segmentation images, the pixel value should denote the class ID of the corresponding pixel. This is a common format used by most of the datasets


The dataset is a subset of Cityspace Dataset and is already divided into train and test splits.

Following classes are there in the dataset.
"Sky", "Building", "Pole","Road","Pavement","Tree","SignSymbol", "Fence", "Car", "Pedestrian", "Bicyclist"

Given below is the predictions overlapped on the input image for visualization.

<p align="center">
  <img src="sample_images/4_input.jpg" width="350" title="accessibility text">
</p>

## Task : Option 01

You can use CNN architecture of your own choice, i.e., build VGG, or ResNet style architecture using primitive layers or call in the pre-implemented architectures available in Keras / Pytorch, whatever framework you are using.

Use two CNN architectures for semantic segmentation.
1. The first Architecture would be any baseline network, like FCN, U-NET or SegNet. In this baseline network, VGG Net can be used as backbone.
2. In the 2nd Architecture, Experiment with different CNN backbone. E.f if you are using SegNet for semantic segmentation in the first part, then instead of VGG, you may use mobile-net backbone, or resnet back-bone or xception backbone or any other etc.
Compare the results of both the architectures, it is expected that the qualitative and quantitative results from 2nd architecture would be better that first.
