# Image Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:

Import the necessary libraries and read the original image and save it as a image variable.

### Step 2:

Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 3:

Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 4:

Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step 5:

Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step 6:

Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:

Crop the image using cropped_img=input_img[20:150,60:230]

### Step 8:

Display all the Transformed images.

## Program:
### Developed By: KAYALVIZHI M
### Register Number: 212220230024
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("dream.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
```
### i) Image Translation
```python

M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

```
### ii) Image Scaling
```python

M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

```
### iii) Image shearing
```python

M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

```
### iv) Image Reflection
```python

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

```
### v) Image Rotation
```python

angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

```
### vi) Image Cropping
```python

cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i) Image Translation

![img1](https://user-images.githubusercontent.com/75413726/166099042-397e5c32-59af-445f-aac7-1fa4c69a5d9c.jpg)

### ii) Image Scaling

![img2](https://user-images.githubusercontent.com/75413726/166099051-2591ac97-604a-451b-bf47-794be6bb333b.jpg)


### iii) Image shearing

![img3](https://user-images.githubusercontent.com/75413726/166099061-2b2faf6f-20b4-4ed7-8ee8-948960723114.jpg)


### iv) Image Reflection

![img4](https://user-images.githubusercontent.com/75413726/166099072-74893a1a-d2f9-4e41-874f-add881a46770.jpg)



### v) Image Rotation

![img5](https://user-images.githubusercontent.com/75413726/166099080-834f2237-3898-4726-b409-142e825db30b.jpg)



### vi) Image Cropping

![img6](https://user-images.githubusercontent.com/75413726/166099084-d590089f-ad16-4122-ae1b-27e7202880bd.jpg)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
