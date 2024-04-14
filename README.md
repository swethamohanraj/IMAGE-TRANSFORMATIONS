# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and read the original image.
<br>
### Step2:
Translate the image.
<br>
### Step3:
Scale the image.
<br>
### Step4:
Shear the image.
<br>
### Step5:
Find reflection of image.
<br>
### Step 6:
Rotate the image.
<br>
### Step 7:
Crop the image.
<br>
### Step 8:
Display all the Transformed images.

## Program:
```python
# Developed By: K.M.Swetha
# Register Number: 212221240055

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("penguin.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape

# i)Image Translation
M = np.float32([[1,0,100],
               [0,1,200],
               [0,0,1]])
translated_image = cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

# ii) Image Scaling
M = np.float32([[1.5,0,0],
               [0,1.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()

# iii)Image shearing
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.5,1,0],
                 [0,0,1]])
sheared_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
plt.show()

# iv)Image Reflection
M_x = np.float32([[1,0,0],
                 [0,-1,rows],
                 [0,0,1]])
M_y = np.float32([[-1,0,cols],
                 [0,1,0],
                 [0,0,1]])
reflected_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflected_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_yaxis)
plt.show()

# v)Image Rotation
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_image = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_image)
plt.show()

# vi)Image Cropping
cropped_image = input_image[100:300,100:300]
plt.axis('off')
plt.imshow(cropped_image)
plt.show()







```
## Output:
### Original Image:
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/87a5b25e-146c-4896-92d1-149778d09375)

### i)Image Translation
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/00c9b285-8c56-409d-bbd3-940f217f0fb4)

<br>
<br>
<br>
<br>

### ii) Image Scaling
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/76eb3d47-b2b8-426a-866b-d5de0df680f4)

<br>
<br>
<br>
<br>


### iii)Image shearing
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/9f2632b9-9ad1-4a08-a5c7-492098e6ebf7)

<br>
<br>
<br>
<br>


### iv)Image Reflection
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/bfc66a33-76ea-4bbf-86d0-b8e8a779c862)

<br>
<br>
<br>
<br>



### v)Image Rotation
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/9374c0dc-dc03-4f17-a448-e019dacd2e7e)

<br>
<br>
<br>
<br>



### vi)Image Cropping
![image](https://github.com/swethamohanraj/IMAGE-TRANSFORMATIONS/assets/94228215/e7750480-ec94-47c7-916f-c2a419214dc0)

<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
