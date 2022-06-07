# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.




### Step2:
<br>
Create the Text using cv2.putText

### Step3:
<br>
Create the structuring element

### Step4:
<br>
Use Opening operation

### Step5:
<br>
Use Closing Operation

### Step6:
<br>
End the program
 
## Program:

``` Python



# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'VANI',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)















```
## Output:

### Display the input Image
![S1](https://user-images.githubusercontent.com/95198708/172300495-b417ac89-de11-441a-a3a8-8af1ef2a0bc0.png)





### Display the result of Opening
![S2](https://user-images.githubusercontent.com/95198708/172300517-a8a2833a-2e53-42cc-9bbd-d2352b9f3b86.png)


### Display the result of Closing
![S3](https://user-images.githubusercontent.com/95198708/172300536-62b40aea-4a95-48fb-b897-2e41166a53e5.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
