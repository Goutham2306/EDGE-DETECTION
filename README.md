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


## Output:


![output](./sobel.png)

### LAPLACIAN EDGE DETECTOR
![output](./laplacian.png)


### CANNY EDGE DETECTOR
![output](./canny.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
