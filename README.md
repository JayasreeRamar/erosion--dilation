# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'JAYASREE' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:

### Display the input Image
<img width="406" height="124" alt="Screenshot 2025-11-12 113405" src="https://github.com/user-attachments/assets/3f59a919-b1b4-4f02-9173-be69abc33429" />

### Display the Eroded Image

<img width="397" height="119" alt="Screenshot 2025-11-12 113409" src="https://github.com/user-attachments/assets/11ccd226-0dd9-4298-86e3-d04982d2f330" />

### Display the Dilated Image
<img width="403" height="122" alt="Screenshot 2025-11-12 113416" src="https://github.com/user-attachments/assets/cca279b8-1779-4977-9771-5f59b5a1141f" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
