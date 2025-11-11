# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:

Create the Text using cv2.putText.
### Step3:

Create the structuring element.

### Step4:
Use Opening operation.
### Step5:

Use Closing Operation.

 
## Program:
# Name: Shruthi D N
# Reg No: 212223240155

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Shruthi D N', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))

# Use Opening operation
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

# Use Closing Operation
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")




```
## Output:

### Display the input Image
<img width="773" height="175" alt="image" src="https://github.com/user-attachments/assets/87748359-a9f4-4658-974b-1de84acf9f3a" />


### Display the result of Opening
<img width="836" height="183" alt="image" src="https://github.com/user-attachments/assets/731caf98-5f90-4966-a2bf-a51162bb2ad6" />


### Display the result of Closing
<img width="939" height="181" alt="image" src="https://github.com/user-attachments/assets/94b78ea6-0451-4e40-95eb-581d42abb7a2" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
