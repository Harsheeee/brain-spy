# Task 1 Edge Detection
Harshit Tripathi -- 240443

## Introduction
This task includes implementation of various edge detection method from scratch. I have used Sobel, Scharr and Canny Edge detection and this notebook (ipynb) demonstrates all of them on a sample image.
I have used NumPy and OpenCV.

## Sobel
1. Two ```sobel_x``` and ```sobel_y``` kernels are used for this method for gradient computation in each direction.
2. A custom function ```convolution``` is used to apply these kernels on the ```grayScale``` image.
3. Gradient magnitude is computed using $\sqrt{gx^2+gy^2}$.

The output highlights the edges but is sensitive to the noise.
## Scharr
1. Two ```scharr_x``` and ```scharr_y``` kernels are used.
2. ```convolution``` function is applied on the ```grayScale``` image.
3. Gradient magnitude is computed.

Output provided is better and has clearer edges than Sobel but the differnce is very negligible.
## Canny Edge
1. Gaussian Blur is applied to reduce noise.
2. Gradients is computed using Sobel filters.
3. Gradient direction (```θ```) is calculated using ```arctan2```.
4. Non-Maximum Suppression done to thin out the edges.
5. Double Thresholding is done differentiate between strong, weak, and non-relevant pixels.
6. Hysteresis is applied to connect weak edges to strong ones if adjacent.

It detects fine and well-defined edges as well. It provides the best output among all other methods implemented in this ipynb.
