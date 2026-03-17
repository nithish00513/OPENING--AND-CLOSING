# OPENING--AND-CLOSING
### Name - NITHISH KUMAR S
### Register Number - 212224230190
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

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NITHISH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')




# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="502" height="493" alt="image" src="https://github.com/user-attachments/assets/a0221aa7-b28c-44c4-a396-36e7af1eaec0" />





### Display the result of Opening
<img width="549" height="508" alt="image" src="https://github.com/user-attachments/assets/3bb4346b-3bd4-41a7-95b6-a3e483b2a76d" />



### Display the result of Closing
<img width="514" height="475" alt="image" src="https://github.com/user-attachments/assets/587b5602-3eab-4aeb-8c4f-59688e3b697a" />



<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
