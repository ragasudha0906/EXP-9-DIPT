# EXP 09 - Record-IMPLEMENTATION OF EROSION AND DILATION
## NAME : RAGASUDHA R
## REG NO :212224230215

## AIM

To implement Erosion and Dilation operations on an image using OpenCV to observe the shrinking and expanding effects on text.

## PROCEDURE

1.Start the program and import the required libraries (cv2, numpy, and matplotlib.pyplot).
2.Create a blank image using np.zeros().
3.Add text to the image using cv2.putText().
4.Display the input image containing the text using matplotlib.pyplot.
5.Create a 3×3 kernel using np.ones().
6.Apply Erosion using cv2.erode() to shrink the text and Dilation using cv2.dilate() to expand the text.
7.Display the Eroded and Dilated images using matplotlib.pyplot and stop the program.

## CODE
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'RAGASUDHA R', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## OUTPUT

<img width="907" height="852" alt="image" src="https://github.com/user-attachments/assets/1c8bcf5f-6b8d-42d3-b7bb-c22784c90ed4" />
<img width="965" height="597" alt="image" src="https://github.com/user-attachments/assets/0d7ce851-5790-485d-aed0-d7c7e66fa3cd" />
<img width="1040" height="605" alt="image" src="https://github.com/user-attachments/assets/180f88db-388a-48b0-bba5-f4586c956e11" />
<img width="922" height="585" alt="image" src="https://github.com/user-attachments/assets/7a012eeb-7eaa-4f95-94c8-91c9ec8c703b" />


## RESULT
Erosion and Dilation operations are successfully implemented using OpenCV. The eroded image shows thinner text, while the dilated image shows thicker text compared to the original image.
