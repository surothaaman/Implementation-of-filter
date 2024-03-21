## EX-5  Implementation-of-filter

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Install the open cv by using pip install opencv-python

### Step2
Import cv2 for reading and changing it smooth and sharpen image

### Step3
import numpy for give the width and size of a image

### Step4
import matplotlib.pyplot for display the image.

## Program:
### Developed By   : Surothaaman R
### Register Number: 212222103003
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Orignal')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image4 = cv2.filter2D(image2, -1, kernel2)
plt.imshow(image4)
plt.title('Weighted Averaging Filtered')
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

gaussian_blur = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)
plt.imshow(gaussian_blur)
plt.title(' Gaussian Blurring Filtered')
```

iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

median=cv2.medianBlur (src=image2, ksize=11)
plt.imshow(median)
plt.title(' Median Blurring Filtered')
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel3 = np.array([[0,1,0], [1, -4,1],[0,1,0]])
image5 =cv2.filter2D(image2, -1, kernel3)
plt.imshow(image5)
plt.title('Laplacian Kernel')
```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('moon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

new_image = cv2.Laplacian (image2, cv2.CV_64F)
plt.imshow(new_image)
plt.title('Laplacian Operator')
```
### OUTPUT:
### 1. Smoothing Filters
#### i) Using Averaging Filter
![image](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/fdf51d7d-520f-45c9-a530-26bffbb507b6)

#### ii) Using Weighted Averaging Filter
![Screenshot 2024-03-22 011445](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/1db811c3-e0a1-46e5-889f-a838338c760e)

#### iii) Using Gaussian Filter
![Screenshot 2024-03-22 011542](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/5bbd9d15-27ea-4338-89db-1b625fa07b5c)

#### iv) Using Median Filter
![Screenshot 2024-03-22 011634](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/dd9a4bdf-5288-4556-8230-fe8d768d2a97)

### 2. Sharpening Filters
##### i) Using Laplacian Kernal
![Screenshot 2024-03-22 011754](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/8347c1d1-b574-4263-8989-70039bb664e0)

#### ii) Using Laplacian Operator
![Screenshot 2024-03-22 011902](https://github.com/surothaaman/Implementation-of-filter/assets/133313653/f72ce989-2840-4d69-9f52-2084e854f3b7)

### Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
