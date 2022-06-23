# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

### Step3:
Scale the image using 
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

### Step4:
Shear the image using 
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

### Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

### Step8:
Display all the Transformed images.


## Program:
### Developed By: DIVYA MEENAKSHI A
### Register Number:212220230014
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
original_img=cv2.imread("bts.jpeg")
original_img=cv2.cvtColor(original_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(original_img)
row,col,dim=original_img.shape
```
i)Image Translation
```python
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)
```
ii) Image Scaling
```python
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)
```
iii)Image Shearing
```python
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)
```

iv)Image Reflection
```python
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

```

v)Image Rotation
```python
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)



```
## Output:
### i)Image Translation
![Screenshot (281)](https://user-images.githubusercontent.com/75235402/166115744-3fc47fb2-3a53-4bc0-a1b9-262506f85a0d.png)


### ii) Image Scaling

![Screenshot (282)](https://user-images.githubusercontent.com/75235402/166115747-3ae6cd2d-85d6-4dd0-874c-3b9760a5875e.png)


### iii)Image shearing
![Screenshot (285)](https://user-images.githubusercontent.com/75235402/166115749-ed5c426a-e9e7-40d2-a3e3-ecfb96c3769e.png)



### iv)Image Reflection
![Screenshot (283)](https://user-images.githubusercontent.com/75235402/166115754-115e3fd8-4412-4115-9301-f8295238f643.png)


### v)Image Rotation
![Screenshot (284)](https://user-images.githubusercontent.com/75235402/166115791-11da3748-7d8b-4ce0-964d-2b0430c457bd.png)




### vi)Image Cropping
![Screenshot (284)](https://user-images.githubusercontent.com/75235402/166115752-01a8d994-608b-42b9-aad7-847894d19b61.png)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
