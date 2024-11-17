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
```python
# Developed By: dharshan V
# Register Number:212222230031

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('flower.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [255], [0, 255])
# Plot histogram of the original grayscale image
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [255], [0, 255])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 255])

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-09-30 162812 (1)](https://github.com/user-attachments/assets/290952b8-6f52-465d-87d7-5d0fd4c13438)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-09-30 162824](https://github.com/user-attachments/assets/a7bb2f35-798a-4fc5-bebb-79d4895c620f)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-09-30 162833](https://github.com/user-attachments/assets/50a0384b-2457-4a0a-97b1-e7e1596da1bc)

### Histogram of the equalized image
![Screenshot 2024-09-30 162843](https://github.com/user-attachments/assets/85006b57-b40d-42a3-ba8d-913a49bf003c)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
