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
<br>

## Program:
```python
Developed By: 212221240055
Register Number: K.M.SWETHA


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
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/aee0e2ce-851e-4ce6-8e6d-fba6c2fc3dfe)

### i)Image Translation
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/4776e95a-7a8e-4900-adb9-46b140bb318b)


<br>
<br>
<br>
<br>

### ii) Image Scaling
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/0a62a5a1-6afa-4f6f-a7ca-357bd05de7d1)

<br>
<br>
<br>
<br>


### iii)Image shearing
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/98e4d6d3-5095-4a0c-9193-588e4963e396)

<br>
<br>
<br>
<br>


### iv)Image Reflection
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/23790199-e845-4e04-84ab-ff496adab958)

<br>
<br>
<br>
<br>



### v)Image Rotation
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/3a2abbb9-9fb7-4d3c-b46c-ea8659d232db)

<br>
<br>
<br>
<br>



### vi)Image Cropping
![image](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/94228215/5cbe8abc-d80c-40b1-bd6b-5f293ae6de3b)

<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
