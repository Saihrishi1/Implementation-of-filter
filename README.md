# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
```
Developed By   : Sai Hrishi M
Register Number: 212224240140
```

### 1. Smoothing Filters

i) Using Averaging Filter
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("C:/Users/admin/Downloads/Digital images/ex_6_image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
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
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
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
iv)Using Median Filter
```python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
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


<img width="897" height="561" alt="Screenshot 2025-09-24 113936" src="https://github.com/user-attachments/assets/e1e36719-53eb-40fb-9824-9470307ffbdf" />


ii)Using Weighted Averaging Filter


<img width="668" height="411" alt="Screenshot 2025-09-24 113944" src="https://github.com/user-attachments/assets/c74075c6-8283-4b47-a573-29ef9f37b234" />


iii)Using Gaussian Filter


<img width="647" height="426" alt="Screenshot 2025-09-24 113959" src="https://github.com/user-attachments/assets/2c31d81b-cfb8-4703-8b53-730672b1f3a2" />


iv) Using Median Filter


<img width="895" height="574" alt="Screenshot 2025-09-24 114012" src="https://github.com/user-attachments/assets/99c80842-019a-46fd-93cc-fe7856528652" />


### 2. Sharpening Filters


i) Using Laplacian Kernal


<img width="650" height="433" alt="Screenshot 2025-09-24 114019" src="https://github.com/user-attachments/assets/76b43a6f-05b5-4ac6-8837-ea7b1e018d2e" />


ii) Using Laplacian Operator

<img width="655" height="433" alt="Screenshot 2025-09-24 114028" src="https://github.com/user-attachments/assets/96f67c4e-8144-4105-aeac-360ccc7d8af0" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
