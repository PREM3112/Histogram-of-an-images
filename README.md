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
# Developed By: PREM R
# Register Number: 212223240124

import cv2
import numpy as np
import matplotlib.pyplot as plt
gray_image = cv2.imread('Albert_Einstein_1947.jpg', cv2.IMREAD_GRAYSCALE)
plt.title("Grayscale Image")
plt.imshow(gray_image, cmap='gray')
plt.axis('off')
plt.title("Histogram of Grayscale Image")
plt.hist(gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)
plt.tight_layout()
plt.show()
equalized_gray_image = cv2.equalizeHist(gray_image)
plt.title("Histogram of Equalized Grayscale Image")
plt.hist(equalized_gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)
plt.title("Enhanced Grayscale Image")
plt.imshow(equalized_gray_image, cmap='gray')
plt.axis('off')







```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-03-22 143725](https://github.com/user-attachments/assets/89d562de-913f-4e05-ac5a-3652882be751)
![Screenshot 2025-03-22 143740](https://github.com/user-attachments/assets/db6e1456-a91d-4a08-96d4-e4a0da560bd9)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2025-03-22 143901](https://github.com/user-attachments/assets/e9259741-4a86-470b-867f-65c7232a5ef9)
![Screenshot 2025-03-22 143912](https://github.com/user-attachments/assets/ac2cec70-5247-4f46-9099-1c61d9c7f3a3)




### Histogram Equalization of Grayscale Image.
![Screenshot 2025-03-22 144026](https://github.com/user-attachments/assets/41b0c1ce-f57f-49ea-ae2d-1295147f0380)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
