### EX NO: 11
### DATE:
# <p align="center">OPENING AND CLOSING</p>

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring element for opening and closing.

### Step 4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:
Plot the images using plt.imshow.
 
## Program:
```
### Developed By   : N Sandhya Charu
### Register Number: 212220230041
```
``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Sandhya",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235167/170851739-13a09a1b-ed5f-4024-b41c-e23fdcddb044.png)

### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235167/170851750-4c611321-4eb2-4f2d-9800-c06d4fada799.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235167/170851753-6171c2d3-666a-4231-99b1-c9d90703ecb3.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
