## Histogram-Equalization-Using-OpenCV

## Aim:

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

## The program performs the following operations:

* Read and display a grayscale image.
* Plot histogram of the grayscale image.
* Apply histogram equalization on grayscale image.
* Read and display a color image.
* Plot histogram of B, G, R channels.
* Convert image to HSV color space.
* Apply histogram equalization on the Value (V) channel.
* Convert the enhanced image back to BGR format.
* Display original and enhanced images with histograms.

## Software Used:

* Anaconda – Python 3.7.
* Jupyter Notebook / VS Code.
* OpenCV (cv2).
* NumPy.
* Matplotlib.

## Algorithm:

## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Read the image parrot.jpg in grayscale format.

## Step 3:
Display the grayscale image and plot its histogram.

## Step 4:
Apply histogram equalization using cv2.equalizeHist() to enhance contrast.

## Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

## Step 6:
Read the same image in color format.

## Step 7:
Split the image into B, G, R channels and plot their histograms.

## Step 8:
Convert the image from BGR to HSV color space.

## Step 9:
Apply histogram equalization on the V (Value) channel.

## Step 10:
Merge the channels and convert the image back to BGR format.

## Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

## Program:

Developed By: SARAN RAJ M

Register No: 212225240138

## Import Python necessary libraries:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

## Display the Equalized Histogram:

```
img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')
```

```
plt.imshow(img_eq, cmap='gray')
plt.title('Original Image')
plt.show()
```

## Histogram Equalization for Grayscale Images

```
img = cv2.imread('loki1.jpeg', cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()
```

```
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
```

## To display Histogram Equalization for Color Images:

```
img = cv2.imread('loki1.jpeg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
plt.imshow(img_eq[:,:,::-1]); plt.title('Equalized Image');plt.show()
```

## To Display Equalized Histogram:

```
plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
```

## To Display Original Color Image and Equalized Image:

```
plt.figure(figsize = (20,10))
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.show()
```

## To Display Original Image and Histogram Equalized Image:

```
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```

## OUTPUT:

## To Display Original Image:

<img width="510" height="347" alt="image" src="https://github.com/user-attachments/assets/26e322d1-1c9e-483e-b1f4-e0d32d949a25" />


<img width="565" height="382" alt="image" src="https://github.com/user-attachments/assets/e1146fe5-cc33-464a-b137-5e8be2dd0b8a" />


## Display the Equalized Histogram:

<img width="547" height="372" alt="image" src="https://github.com/user-attachments/assets/a1931528-dd2b-4a37-9034-6c242637d740" />


## Histogram Equalization for Grayscale Images:
<img width="517" height="347" alt="image" src="https://github.com/user-attachments/assets/45daa12d-0532-44da-9dd5-f9827fd2c78e" />

## To Display Equalized Histogram:

<img width="486" height="377" alt="image" src="https://github.com/user-attachments/assets/2f79bb4b-ae9d-4f24-842e-19ca199742e9" />


## To Display Original Color Image and Equalized Image:

<img width="511" height="157" alt="image" src="https://github.com/user-attachments/assets/6ac5dd45-403d-4b38-b8ac-68d30fcf9e22" />


## To Display Original Image and Histogram Equalized Image:

<img width="512" height="150" alt="image" src="https://github.com/user-attachments/assets/7ea70649-1198-4f63-88ee-1dbb67fbd2c2" />



## Grayscale Histogram Equalization:

* Original grayscale image is displayed.
* Histogram of original grayscale image is plotted.
* Enhanced image after histogram equalization is displayed.
* Histogram of enhanced grayscale image shows improved contrast.

## Color Image Histogram Equalization:

* Original color image is displayed.
* Histogram of B, G, R channels is plotted.
* Enhanced image after HSV-based equalization is displayed.
* Histogram of enhanced image shows better intensity distribution.

## Result:

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
