# EX-6 EDGE-DETECTION
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
## PROGRAM:
```
DEVELOPED BY: PRAVINRAJJ G.K
REGISTER NUMBER: 212222240080
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("flo.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/98f2f6f1-f862-4623-bf1a-ae646577988c)

### SOBEL EDGE DETECTOR:
![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/fdc7ec22-940d-40be-b498-18233f013888)

![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/c49ee671-3626-4b03-ae9e-60a7448297ff)

![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/a2e3a7a7-3b06-436c-8c8d-ef70339a1408)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/307504c8-c110-4853-9c59-bf37f66c6a01)

### CANNY EDGE DETECTOR
![image](https://github.com/Pravinrajj/EDGE-DETECTION/assets/117917674/3dfb3196-c175-48e8-9da7-11fb35a1e4b6)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
