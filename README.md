# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image.

### Step3:
Display the histograms.

### Step4:
Equalize the color image.

### Step5:
Display the equalized grayscale image.
## Program:
```python
# Developed By:SHARMILA A
# Register Number:212221230094

```
```
import cv2
import matplotlib.pyplot as plt
```
# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("gray.jpg")
cv2.imshow("Gray Image",Gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import cv2
import matplotlib.pyplot as plt
Color_image = cv2.imread("clrr.jpg")
cv2.imshow("Colour_image",Color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("clrr.jpg")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Write the code to perform histogram equalization of the image. 
```
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```






## Output:
### Input Grayscale Image and Color Image
![e1](https://github.com/Sharmilasha/HISTOGRAM/assets/94506182/d7f1b314-4b79-4128-b4d4-2c11a3de1e72)
![e4](https://github.com/Sharmilasha/HISTOGRAM/assets/94506182/19f11c35-3e46-4860-be23-1011a128c6bf)


### Histogram of Grayscale Image and any channel of Color Image
![e2](https://github.com/Sharmilasha/HISTOGRAM/assets/94506182/babc25b4-a0fc-4675-8591-14f13a089d1c)
![e3](https://github.com/Sharmilasha/HISTOGRAM/assets/94506182/b1681130-939b-4833-9dd6-bd5da4935cc7)


### Histogram Equalization of Grayscale Image
![dip4 5](https://github.com/Sharmilasha/HISTOGRAM/assets/94506182/cf2f5d5e-f26c-495b-8643-ba1cb0ff4ae0)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
