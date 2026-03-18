# Implementation-of-Erosion-and-Dilation
### DEVLOPED BY : SHARON STEFFANI.F
### REG NO: 2122223110049
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.

### Step2:
Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.

### Step3:
Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.

### Step4:
Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.

### Step5:
Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.

### Step6:
Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.

### Step7:
Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.
 
## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype="uint8")

text = "STEFFY"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

eroded_image = cv2.erode(image, kernel, iterations=1)
dilated_image = cv2.dilate(image, kernel, iterations=1)

original_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(12,5))

plt.subplot(1,3,1)
plt.imshow(original_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,3,2)
plt.imshow(eroded_rgb)
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1,3,3)
plt.imshow(dilated_rgb)
plt.title("Dilated Image")
plt.axis("off")

plt.show()


```

## Output:

<img width="970" height="326" alt="image" src="https://github.com/user-attachments/assets/73e458e6-5df9-4747-9bc5-ad6feb4b4083" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
