# Image-Segmentation

Image segmentation involves converting an image into a collection of regions of pixels that are represented by a mask or a labeled image. By dividing an image into segments, you can process only the important segments of the image instead of processing the entire image.


In digital image processing and computer vision, image segmentation is the process of partitioning a digital image into multiple image segments, also known as image regions or image objects (sets of pixels). The goal of segmentation is to simplify and/or change the representation of an image into something that is more meaningful and easier to analyze.Image segmentation is typically used to locate objects and boundaries (lines, curves, etc.) in images. More precisely, image segmentation is the process of assigning a label to every pixel in an image such that pixels with the same label share certain characteristics.

The result of image segmentation is a set of segments that collectively cover the entire image, or a set of contours extracted from the image (see edge detection). Each of the pixels in a region are similar with respect to some characteristic or computed property, such as color, intensity, or texture. Adjacent regions are significantly different color respect to the same characteristic(s). When applied to a stack of images, typical in medical imaging, the resulting contours after image segmentation can be used to create 3D reconstructions with the help of interpolation algorithms like marching cubes.

In this architecture, we have used Conv2DTranspose(strides=(2,2)) into the decoder-generator part.

One generated example:-
![One generated image](https://github.com/acfilok96/Image-Segmentation/blob/main/Image%20Segmentation%20Using%20U-Net%20and%20PixToPixGAN/Stage%201/GeneratedImg.png)



In this architecture, we have used UpSampling2D(size=2,2) in place of Conv2DTranspose(strides=(2,2)) into the decoder-generator part, as we are doing segmentation so, we need to capture border information (i.e. error between side by side pixel should be negligible).

One generated example:-

![One Generated Image](https://github.com/acfilok96/Image-Segmentation/blob/main/Image%20Segmentation%20Using%20U-Net%20and%20PixToPixGAN/Stage%202/Generated_Image_ok.png)
