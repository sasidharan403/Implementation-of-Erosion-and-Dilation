# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2: 
Create the Text using cv2.putText.

## Step3: 
Create the structuring element.

### Step4:
Erode and Dilate the image.

### Step5:
End Program.



 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(image,'SASI',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(image)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(image,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(image,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()

```
## Output:

### Display the input Image
![dip 1](https://user-images.githubusercontent.com/94154712/174130493-b5abf482-fdfd-4c60-b023-b61b036341e0.png)

<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
![dip10 2](https://user-images.githubusercontent.com/94154712/174130546-fe6ae90c-5205-4d1c-bb00-bcc920a95094.png)

<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
![dip 10 3](https://user-images.githubusercontent.com/94154712/174130603-cc24785e-17bd-4b1d-aa19-747427d0b3ee.png)

<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
