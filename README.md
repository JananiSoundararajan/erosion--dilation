# Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:<br>
Import the necessary pacakages

### Step2:<br>
Create the text using cv2.putText

### Step3:<br>
Create the structuring element

### Step4:<br>
Erode the image


### Step5: <br>
Dilate the Image

 
## Program:


##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Janani',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:

#### Display the input Image

![ii](https://github.com/JananiSoundararajan/erosion--dilation/assets/119477549/a8280e64-d3d3-489a-8152-42f06e0eaf30)

#### Display the Eroded Image

![EI](https://github.com/JananiSoundararajan/erosion--dilation/assets/119477549/dba569de-b6f0-4a28-9b35-a1cfea87c995)

#### Display the Dilated Image

![di](https://github.com/JananiSoundararajan/erosion--dilation/assets/119477549/2cfb408d-b11b-431f-b73f-39b62f545156)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
