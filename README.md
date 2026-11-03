# Exp5-IMPLEMENTATION-OF-FILTERS

## Implementation-of-filter
### Aim
To implement filters for smoothing and sharpening images in the spatial domain.

### Software Required
Anaconda - Python 3.7
OpenCV
NumPy
Matplotlib
### Algorithm
- Step 1
Import the required libraries.

- Step 2
Read the image and convert it from BGR to RGB.

- Step 3
Apply the required smoothing and sharpening filters to the image separately.

- Step 4
Plot and display the original and filtered images using matplotlib.pyplot.

- Step 5
End the program.

### Program
```
Developed By: RITHIKA K

Register Number: 212225040343
```
1. Smoothing Filters
i) Using Averaging Filter

```
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
plt.show())
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
iv) Using Median Filter
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
2. Sharpening Filters
i) Using Laplacian Linear Kernel
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
ii) Using Laplacian Operator
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
Output
1. Smoothing Filters
i) Using Averaging Filter

<img width="727" height="472" alt="image" src="https://github.com/user-attachments/assets/0cf03959-58c3-4b42-b53a-813a4190276f" />

ii) Using Weighted Averaging Filter

<img width="550" height="345" alt="image" src="https://github.com/user-attachments/assets/09e4a8bf-bdc1-4a2b-9f5b-4b6b00c53f04" />

iii) Using Gaussian Filter

<img width="545" height="360" alt="image" src="https://github.com/user-attachments/assets/a46c44bf-cbe4-458b-b976-ea6ffe89935e" />

iv) Using Median Filter

<img width="717" height="472" alt="image" src="https://github.com/user-attachments/assets/48aea5b4-5f45-4677-966a-77b79564b905" />

2. Sharpening Filters

i) Using Laplacian Kernel

<img width="525" height="357" alt="image" src="https://github.com/user-attachments/assets/8bd95760-f3aa-430d-970a-b33dc971221d" />

ii) Using Laplacian Operator

<img width="867" height="395" alt="image" src="https://github.com/user-attachments/assets/e84e24fb-8167-459b-acf1-29ee1cfbb28d" />

### Result
Thus, filters were implemented for smoothing and sharpening images in the spatial domain using OpenCV and Python.
