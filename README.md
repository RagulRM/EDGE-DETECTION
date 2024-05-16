# EXP-6 EDGE DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program
### RGB to Gray conversion
```
import cv2
img=cv2.imread('flower.jpg')
gray=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imwrite('flower.jpg',gray)
plt.imshow(gray,cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.show()
```
### Import Packages and load the image
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("flower.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
#### SOBEL X
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
#### SOBEL Y
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
#### SOBEL XY
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### ORIGINAL IMAGE
<br>
(https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/e86dc46a-50a9-4fe0-a458-ef107750282d)

<br>

### SOBEL EDGE DETECTOR
<br>
![image](https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/c07f1d67-4a06-48ce-a984-45c27c78eee4)

<br>
![image](https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/1de55c9b-f254-4527-8ae3-c11d78ade6b1)

<br>
![image](https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/92a28def-ce8d-45fe-889b-f5590cbf9ab8)


### LAPLACIAN EDGE DETECTOR
<br>
![image](https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/83ba9ce9-9c08-4a3d-a4e9-6ba1b9b57489)

<br>

### CANNY EDGE DETECTOR
<br>
![image](https://github.com/RagulRM/EDGE-DETECTION/assets/121609342/78858fa4-7fc2-4af9-a0c3-65e3e05d9e4c)

<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
