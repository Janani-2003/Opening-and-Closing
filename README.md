# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening operation.
<br>
### Step5:
Use Closing Operation.
<br>
### Step6:
Print the output and end the program.

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt 

# Create the Text using cv2.putText
image = np.zeros((100,250),dtype = 'uint8')
img=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"JANANI",(5,70),font,2,(204,0,102),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(img,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
opening_image = cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')

# Use Closing Operation
closing_image = cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
```
## Output:

### Display the input Image
![org](https://github.com/Janani-2003/Opening-and-Closing/assets/94288340/3b63a5dd-bfaf-4c91-85ac-96256555c5fa)
<br>
### Display the result of Opening
![open](https://github.com/Janani-2003/Opening-and-Closing/assets/94288340/98c36715-3bf1-4ea3-930d-840840aa300f)
<br>
### Display the result of Closing
![close](https://github.com/Janani-2003/Opening-and-Closing/assets/94288340/2d800715-a6d4-49ea-a608-3ca2a25d94e7)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
