
# Cat Image Segmentation with scikit-image

## Overview

This repository contains code for performing image segmentation on a cat dataset using scikit-image. The segmentation is achieved through the application of various filters and thresholding techniques.

## Dataset

The cat dataset used for this project is not included in this repository. Please visit https://www.robots.ox.ac.uk/~vgg/data/pets/ to access the dataset.

## Language / Libraries

Language: Python

Packages: Scikit-image, Matplotlib, Numpy

## Usage

The code is built on Google Colab on an iPython Notebook.
```bash
Download the repository, upload the notebook and dataset on colab, and execute!
```
## Methods Used

1. ### Filters : Sobel, Prewitt, Scharr
Above mentioned filters were used to highlight edges in the image.
```bash
  sobel_edge  = sobel(gray_image)
  #Apply Prewitt filter to the image 
  prewitt_edge = prewitt(gray_image)
  #Apply Scharr filter to the image 
  scharr_edge = scharr(gray_image)
  ```
2. ### Thresholding :
Thresholding technique was used to separate the cat from the background.
```bash
  thresh = threshold_otsu(gray_image)
  binary = gray_image > thresh
  ```
## Results

1. The filter methods were consistent in highlighting the edges in the images, with less accuracy in cat subjects with noise in the background.
See images below: 
#### Image 1 : No background noise


![2](https://github.com/sri-d1/Image-Segmentation-Using-Skimage/assets/68694495/9efe9bff-f588-4b8e-8712-eb19976cf05e)




#### Image 2 : With background noise

![1](https://github.com/sri-d1/Image-Segmentation-Using-Skimage/assets/68694495/a67f5dd7-c85c-4abb-a615-00ce40e2034a)


2. Thresholding technique produced result with good accuracy on image with no noise , whereas with image having noise and multiple objects result was not very accurate.

#### Image 1 : No background noise
![3](https://github.com/sri-d1/Image-Segmentation-Using-Skimage/assets/68694495/e397afa4-5d3f-494a-a788-ef4bfbd9336e)



#### Image 2 : With background noise 
![4](https://github.com/sri-d1/Image-Segmentation-Using-Skimage/assets/68694495/f168bac0-d0c4-47d0-a578-0b61bda58a61)



## License

[MIT](https://choosealicense.com/licenses/mit/)


