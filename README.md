# EX 05:Implementation-of-filter
### NAME : VISHAL M.A
### REG NO: 212222230177
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
```py
Developed By   : VISHAL M.A
Register Number: 212222230177
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("eiffel.png")
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
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

![ORG IMG 1](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/53bf3140-c04a-410f-b86d-01256664aa00)
![AVG IMG 1](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/bbba82ae-63cc-4129-be25-7ea1b59f1be0)






ii) Using Weighted Averaging Filter

![ORG IMG 2](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/b2701ca9-313c-4e4b-92b6-2b9fee19380d)
![AVG IMG 2](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/100932c5-b5ab-41a7-bc93-013f45244a05)





iii) Using Gaussian Filter

![ORG IMG 3](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/4117f7bd-eb74-4e11-b19c-908c1a549359)
![GSSN IMG 1](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/f4b7ecdd-16e5-4f06-be49-b91b7592c830)




iv) Using Median Filter

![ORG IMG 4](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/4df7ed01-9fe9-427d-93a5-b6c505cc3374)
![MED IMG](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/309e3974-4ad0-4b2d-aebc-6f203c2d4758)






### 2. Sharpening Filters

i) Using Laplacian Kernal

![ORG IMG 5](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/2b5164d7-db7e-47ac-ab0b-edb4886d6dc4)
![LAP IMG 1](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/2763e887-00ae-47e6-9e80-32e445bbfcec)





ii) Using Laplacian Operator


![ORG IMG 6](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/f748505f-e541-4e2b-a31a-079bc8ef1033)
![LAP OP IG](https://github.com/vishal21004/Implementation-of-filter/assets/119560110/6cf0f1a7-89a2-458f-8799-b5c715a9ad8e)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
