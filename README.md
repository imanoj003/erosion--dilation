# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:

Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.
### Step 2:

Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.
### Step 3:

Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.
### Step 4:

Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.
### Step 5:

Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.
### Step 6:

Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.
### Step 7:

Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.
 
## Program:
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((300, 600, 3), dtype="uint8")
```


### Create the Text using cv2.putText
```
text = "Manoj"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```
![image](https://github.com/user-attachments/assets/440e96f2-987d-4a7e-b90f-ea17136bb4fa)

### Create the structuring element

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

```


### Original image
```

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
![Screenshot 2024-11-14 153912](https://github.com/user-attachments/assets/170971d6-16da-4b42-9cac-91b89f796503)


### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```

![Screenshot 2024-11-14 153916](https://github.com/user-attachments/assets/481e29b8-94bc-43df-b6fe-77c0623cc07d)


### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```
![Screenshot 2024-11-14 153919](https://github.com/user-attachments/assets/9544306a-c52e-4a1a-994f-5d6aad2afeeb)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
