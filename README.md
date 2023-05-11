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
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
~~~
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"NAVEEN V",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')



# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')




~~~
## Output:

### Display the input Image
![img1](https://github.com/Naveenvetrivel/Implementation-of-Erosion-and-Dilation/assets/94165322/dfa03f63-528d-497a-916e-caff50364bef)


### Display the Eroded Image
![img2](https://github.com/Naveenvetrivel/Implementation-of-Erosion-and-Dilation/assets/94165322/aa82feb3-9d68-4527-b0c0-2d0068bc5c2e)


### Display the Dilated Image
![img3](https://github.com/Naveenvetrivel/Implementation-of-Erosion-and-Dilation/assets/94165322/c943a8a7-08a2-47ab-87e2-aeca9be3d0f7)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
