# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

## Step2
Convert the image from BGR to RGB.

## Step3
Apply the required filters for the image separately.

## Step4
Plot the original and filtered image by using matplotlib.pyplot.

## Step5
End the program.

## Program:
```
### Developed By   : S.Harika
### Register Number: 212224240155
```

### 1. Smoothing Filters

i) Using Averaging Filter

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("img.png")
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

```
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

```
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

```
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

```
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

```
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

<img width="950" height="587" alt="Screenshot 2025-09-06 012857" src="https://github.com/user-attachments/assets/a21bf415-e5b3-44bd-8f95-63a75a5e4641" />

ii)Using Weighted Averaging Filter

<img width="749" height="430" alt="Screenshot 2025-09-06 012951" src="https://github.com/user-attachments/assets/f183d981-61ee-4299-8fee-7ae4f5f47d96" />

iii)Using Gaussian Filter

<img width="654" height="440" alt="Screenshot 2025-09-06 013020" src="https://github.com/user-attachments/assets/c75a659f-0998-4793-b0e7-9f0c921bb98f" />

iv) Using Median Filter

<img width="937" height="588" alt="Screenshot 2025-09-06 013048" src="https://github.com/user-attachments/assets/e70d6504-2b10-4761-80d3-19578a74fd3c" />


### 2. Sharpening Filters

i) Using Laplacian Kernal

<img width="648" height="433" alt="Screenshot 2025-09-06 013117" src="https://github.com/user-attachments/assets/47ead650-8aa5-4952-b36c-39c1ec7e3f78" />


ii) Using Laplacian Operator

<img width="701" height="434" alt="Screenshot 2025-09-06 013145" src="https://github.com/user-attachments/assets/d4eb8701-bd83-4a15-b2d1-917a5ca65f51" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
