# EX.NO : 07
# DATE :

# <p align="center">Edge Detection</p>
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image.

### Step6:
Using Canny operator from cv2,detect the edges of the image.
 
## Program:

``` Python
# Import the packages

import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise

image=cv2.imread("butterfly.jpg")
image1=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("IMAGE",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

img=cv2.GaussianBlur(image1,(3,3),0)
plt.figure(1)
plt.imshow(img,cmap='gray')
plt.title('Original')
plt.xticks([])
plt.yticks([])

# SOBEL EDGE DETECTOR

sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.imshow(sobelx,cmap='gray')
plt.title('Sobel x')
plt.xticks([])
plt.yticks([])
plt.imshow(sobely,cmap='gray')
plt.title('Sobel y')
plt.xticks([])
plt.yticks([])
plt.imshow(sobelxy,cmap='gray')
plt.title('Sobel xy')
plt.xticks([])
plt.yticks([])

# LAPLACIAN EDGE DETECTOR

laplacian=cv2.Laplacian(img,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])

# CANNY EDGE DETECTOR

canny_edges=cv2.Canny(img,120,150)
plt.imshow(canny_edges,cmap='gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])

```
## Output:
### SOBEL EDGE DETECTOR
<br>
<img width="218" alt="image" src="https://user-images.githubusercontent.com/75235554/168246808-66e87a86-aa2c-41d8-9e3d-9eac4df47e19.png">
<br>
<img width="205" alt="image" src="https://user-images.githubusercontent.com/75235554/168246873-6dfa82cb-ef68-419c-93ad-00c726fba6a8.png">
<br>
<img width="190" alt="image" src="https://user-images.githubusercontent.com/75235554/168246916-5fcc84f7-cf0d-41bd-973c-26c8ec04c214.png">
<br>

### LAPLACIAN EDGE DETECTOR
<br>
<img width="215" alt="image" src="https://user-images.githubusercontent.com/75235554/168247188-cd912bd5-bdb5-48c6-ab7f-a1ae0d7d4de8.png">
<br>


### CANNY EDGE DETECTOR
<br>
<img width="193" alt="image" src="https://user-images.githubusercontent.com/75235554/168247292-bb077cdd-4365-471e-a119-7ca8423a3986.png">
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
