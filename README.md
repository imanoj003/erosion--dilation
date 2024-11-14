# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt


image = cv2.imread("demo.png")  

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
## Output:

## Display the input Image , Display the result of Opening , Display the result of Closing




![Screenshot 2024-11-14 154825](https://github.com/user-attachments/assets/56c9257c-4c37-4259-b87c-9c168684f2d5)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
