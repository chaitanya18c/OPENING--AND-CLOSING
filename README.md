# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step1: Import the necessary packages

Step2: Give the input text using cv2.putText()

Step3: Perform opening operation and display the result

Step4: Similarly, perform closing operation and display the result

 
## Program:
```python
NAME : CHAITANYA P S
REG : 212222230024
```
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ASTA',(5,70), font,2,(255),5,cv2.LINE_AA)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

```
## Output:

### Display the input Image
![image](https://github.com/chaitanya18c/OPENING--AND-CLOSING/assets/119392724/c6900704-6c94-42eb-8941-a0ffbc99c018)


### Display the result of Opening
![image](https://github.com/chaitanya18c/OPENING--AND-CLOSING/assets/119392724/aaae1b44-d860-4280-b708-2de51d3009bf)


### Display the result of Closing
![image](https://github.com/chaitanya18c/OPENING--AND-CLOSING/assets/119392724/9dc4e70d-ce2b-4ecc-8b19-80d2a68ca5f2)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
