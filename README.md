# EDGE-DETECTION
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

## PROGRAM :
## Developed By : Goutham.K
## Register Number : 212223110019
## Importing packages,load and convert to gray image

```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('rose.jpeg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### SOBEL EDGE DETECTOR
## Sobel X:
```
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y:
```
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
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
## GRAY IMAGE:
![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/56790ab8-bdb9-4e04-b304-5110cc8671f0)

### SOBEL EDGE DETECTOR
### SOBEL X:
![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/67562ce2-fcbc-4e2d-ae11-fd192e3d5635)

### SOBEL Y:
![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/31ac9743-854c-4619-9e3c-3c2fe20d2194)

### SOBEL XY:

![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/85547c81-b827-4527-891e-27c6bfdbddf0)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/dca49614-205c-4cb4-b201-f4ba79f88e6d)

### CANNY EDGE DETECTOR

![image](https://github.com/Goutham2306/EDGE-DETECTION/assets/138971154/9dc24b46-4144-41fb-8bdf-ba3af1c4452c)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
