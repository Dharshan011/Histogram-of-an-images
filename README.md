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
```
 Developed By: DHARSHAN V
 Register Number: 212222230031
```
### Input Grayscale Image and Color Image

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("ak.jpeg")
color_image = cv2.imread("vijay.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 135508](https://github.com/user-attachments/assets/b355c916-c89a-4c8e-ba33-ba3cb7fc2051)


### Histogram of Grayscale Image and any channel of Color Image

```python
import numpy as np
Gray_image = cv2.imread("ak.jpeg")
Color_image = cv2.imread("vijay.jpeg")
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

![Screenshot 2024-09-09 140320](https://github.com/user-attachments/assets/3192bfb2-81aa-4b59-a3f1-a362b14b7c47)


#### Grayscale Image



#### Color Image

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
![Screenshot 2024-09-09 140307](https://github.com/user-attachments/assets/25905072-2931-4956-ac2c-ed5c81df5974)



### Histogram Equalization of Grayscale Image.

```python
import cv2
gray_image = cv2.imread("ak.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 140247](https://github.com/user-attachments/assets/5099c354-f784-4601-a83c-26a33a78db5f)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
