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
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/5a80b7b5-53cf-43e9-89a5-0a4a63044f0c" height=300 width=400>

<br>

### SOBEL EDGE DETECTOR
<br>
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/5e80faca-3675-42fc-8e83-d2b595f009bf" height=300 width=400>

<br>
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/5ee25fb1-05a3-4a0f-9a8f-a766c3bb3ae0" height=300 width=400>

<br>
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/53371e6b-7bdf-4d1c-8789-70f583ba9730" height=300 width=400>


### LAPLACIAN EDGE DETECTOR
<br>
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/8d170931-20a2-438b-8b96-6d31deb28d2c" height=300 width=400>

<br>

### CANNY EDGE DETECTOR
<br>
<img src="https://github.com/Jenishajustin/EDGE-DETECTION/assets/119405070/86297d00-4b03-4399-bc69-a50bf787d49c" height=300 width=400>

<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
