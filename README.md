# EXP -5 Implementation-of-filter
## MANASA S
## 212224220059
## Aim

To implement filters for smoothing and sharpening images in the spatial domain.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import the required libraries.

### Step 2
Read the image and convert it from BGR to RGB.

### Step 3
Apply the required smoothing and sharpening filters to the image separately.

### Step 4
Plot and display the original and filtered images using `matplotlib.pyplot`.

### Step 5
End the program.

## Program

**Developed By:** MANASA S

**Register Number:** 212224220059

## 1. Smoothing Filters

### i) Using Averaging Filter

```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("sv.jpeg")
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

### ii) Using Weighted Averaging Filter

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
plt.show())
```

### iii) Using Gaussian Filter

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

### iv) Using Median Filter

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

## 2. Sharpening Filters

### i) Using Laplacian Linear Kernel

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

### ii) Using Laplacian Operator

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

## Output

### 1. Smoothing Filters

#### i) Using Averaging Filter

<img width="897" height="583" alt="image" src="https://github.com/user-attachments/assets/c31f2baa-79c5-479a-b882-282776deeae5" />

#### ii) Using Weighted Averaging Filter

<img width="656" height="427" alt="image" src="https://github.com/user-attachments/assets/1db3148b-b272-48d5-9748-5ad3bcddf524" />


#### iii) Using Gaussian Filter

<img width="642" height="430" alt="image" src="https://github.com/user-attachments/assets/2f34e0da-0c22-48e8-bda2-18b7f1d2b148" />


#### iv) Using Median Filter

<img width="887" height="577" alt="image" src="https://github.com/user-attachments/assets/e12d7107-c157-405f-bec0-9a88ed61ddc1" />


### 2. Sharpening Filters

#### i) Using Laplacian Kernel

<img width="633" height="422" alt="image" src="https://github.com/user-attachments/assets/6aaba8e1-5d18-4fe9-b2c0-0fe07f0c2b5f" />


#### ii) Using Laplacian Operator
<img width="637" height="417" alt="image" src="https://github.com/user-attachments/assets/e809a108-2f03-4d9a-9aac-8016e5d37b2c" />


## Result

Thus, filters were implemented for smoothing and sharpening images in the spatial domain using OpenCV and Python.
