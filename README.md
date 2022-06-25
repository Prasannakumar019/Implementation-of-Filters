## EX NO:06
## DATE:3.5.22
# <p align="center">Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary modules.

### Step 2:
For performing smoothing operation on a image.

Average filter
```python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
Weighted average filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
Gaussian Blur
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
Median filter
```python
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.

Laplacian Kernel
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.
## Program:
  ```python
  Developed By   :Prasannakumar M 
  Register Number:212220230035
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("hhusskyy.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![Screenshot (307)](https://user-images.githubusercontent.com/75235090/167666159-e89bfdef-c573-4ffd-af23-27b815823462.png)

ii) Using Weighted Averaging Filter

![Screenshot (308)](https://user-images.githubusercontent.com/75235090/167666482-8f6c0b10-4331-4c5c-912e-f93892f0a843.png)

iii) Using GaussianFilter

![Screenshot (311)](https://user-images.githubusercontent.com/75235090/167667180-5e9141e3-d2f1-4384-b977-676c36a955ef.png)

iv) Using Median Filter

![Screenshot (312)](https://user-images.githubusercontent.com/75235090/167667535-7b8ac49c-9d40-4fa9-9956-9af25b8025c9.png)


### 2. Sharpening Filters


i) Using Laplacian Kernal
  
![Screenshot (311)](https://user-images.githubusercontent.com/75235090/167667726-d9d98687-7db0-4b68-bb4b-f4c243b02221.png)
  
ii) Using Laplacian Operator
  
![Screenshot (312)](https://user-images.githubusercontent.com/75235090/167667862-48da57bf-ad1e-4e28-8853-65d80efbe923.png)
  
 ``` 
## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
