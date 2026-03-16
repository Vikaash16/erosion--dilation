# Implementation-of-Erosion-and-Dilation
## DEVELOPED BY :Vikaash P
## REG NO : 212223240180
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

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype="uint8")

# Create the Text using cv2.putText
text = "SAJITH AHAMED"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)


# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))



# Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")



# Dilate the image

dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")



```
## Output:

### Display the input Image
<img width="507" height="506" alt="image" src="https://github.com/user-attachments/assets/e7c3e4eb-aee0-464e-b552-235839933d35" />


### Display the Dilated Image
<img width="709" height="544" alt="image" src="https://github.com/user-attachments/assets/99fee06e-64c2-4e49-aaaf-eabce98734ec" />



### Display the Eroded Image
<img width="384" height="383" alt="image" src="https://github.com/user-attachments/assets/fde58c97-5efd-4b37-9ee6-4b2a83499076" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
