---
layout: page
title: CNN vs Traditional Image Classification
description: The project aims to showcase a straightforward neural network for basic geometric shape classification and how it compares with traditional image processing methods, highlighting the potential of neural networks in real-world scenarios.
img: assets/img/12.jpg
importance: 1
category: work
related_publications: false
---

Shape recognition is vital in computer vision, widely used in fields such as robotics and manufacturing. Due to limitations in traditional methods, there's been a shift towards using convolutional neural networks (CNNs), which excel in learning from data and performing complex image analysis tasks.

In the end, I also showcased their application of pre-trained models in more complex image recognition scenario fo fun.

MAKING THE DATASET:

A python script is used to automatically generate and process a dataset of images, each depicting one of three geometric shapes—circle, square, or triangle—with various visual modifications. Using OpenCV, the script creates images of specified shapes with transformations like rotation, occlusion and noise.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/samples.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample images generated (circle, square and triangle)
</div>

CNN MODEL NETWORK ARCHITECTURE:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cnn.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The model uses Adam optimizer, Categorical Crossentropy loss, and measures accuracy.
</div>

EVALUATION:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/training_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/training_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left is- Training 1: 50 images, 20 epochs. On the right is- Training 2: 100 images, 50 epochs.
</div>

The traditional approach utilizes the OpenCV library in Python.

The process begins with the image being loaded and converted to grayscale using the cvtColor function, and smoothed with Gaussian Blur to reduce noise. Next, edge detection is performed using the Canny edge detector to identify object boundaries by detecting significant changes in pixel intensity. Following this, contour detection retrieves and simplifies the external contours of objects to reduce shape complexity. Finally, shape classification is conducted by analyzing the contours with the approxPolyDP function to categorize shapes based on their number of vertices.

ACCURACY COMPARISON:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/accuracy.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

OBSERVATIONS:

I noticed that as I decreased the amount of transformations and noise in the generated images, the traditional approach was catching up. Also, it mattered how big of/what kind of dataset I train my neural network on. But all this makes sense since neural networks are supposed to be used on much larger and complex datasets.

Therefore, the project confirms that neural networks outperform traditional image processing methods in shape recognition. CNNs' ability to adaptively learn from data enhances pattern recognition capabilities across various computational vision applications, validating their use for more complex image recognition tasks.


PREDICTIONS OF PRE-TRAINED MODELS (trained on ImageNet):

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pretrained.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left is- VGGNet's prediction: lakeside. On the right is- ResNet's prediction: valley.
</div>

The difference in predictions likely arises from the models' architectures and feature extraction methods.

