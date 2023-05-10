# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Bhavishya Reddy',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()


# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))


# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()



# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()




```
## Output:

### Display the input Image
![DIP B11-1](https://github.com/Bhavishya203/Opening-and-Closing/assets/94679395/6f19124c-eb1b-423b-8c2b-dae733467dbf)







### Display the result of Opening
![DIP B11-22](https://github.com/Bhavishya203/Opening-and-Closing/assets/94679395/2bb8a945-7fd0-4433-8ac1-ef41796a6116)







### Display the result of Closing
![DIP B11-3](https://github.com/Bhavishya203/Opening-and-Closing/assets/94679395/08916293-13cf-4967-bfe1-2c9b2676b964)







## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
