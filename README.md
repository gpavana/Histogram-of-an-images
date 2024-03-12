# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

# Developed By: PAVANA.G
# Register Number: 212222230105

## Grayscale image and Color image:
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat.jpg")
color_image = cv2.imread("bird.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat.jpg")
Color_image = cv2.imread("bird.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
## Histogram of Color image
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram equalization of Grayscale image
```python

import cv2
gray_image = cv2.imread("bird.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/gpavana/Histogram-of-an-images/assets/118787343/97daf977-a8c7-46d2-81f4-9095ef5acdb9)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/gpavana/Histogram-of-an-images/assets/118787343/bee63b2d-4eca-4487-bc7f-63a0e3bc0833)
![image](https://github.com/gpavana/Histogram-of-an-images/assets/118787343/418c8d72-c2bc-4097-a9e4-4e2ae08b8a5f)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-12 114320](https://github.com/gpavana/Histogram-of-an-images/assets/118787343/84e31c01-4c3f-4d84-b616-89b1f92db2ab)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
