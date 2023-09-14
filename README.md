# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
<br>
Write a code to translation of the image.

### Step3:
<br>
Write a code for scaling of the image.

### Step4:
<br>
Find reflection of image. 

### Step5:
<br>
Display all the Transformed images.

## Program:

Developed By:Praveen s
Register Number:212222240077
i)Image Translation
```python
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv


image = cv.imread("771203.jpg")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()



rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))


plt.imshow(translated_image)
plt.show()



```


ii) Image Scaling
```python
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.imshow(scale_image)
plt.show()


```


iii)Image shearing
```python

M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()

```


iv)Image Reflection

```python
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()


```


v)Image Rotation

```python
M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()
ang=np.radians(10)

mat=np.float32([[np.cos(ang),-np.sin(ang),0],[np.sin(ang),np.cos(ang),0],[0,0,1]])

Rotated_image=cv.warpPerspective(image,mat,(cols,rows))

plt.axis("off")
plt.imshow(Rotated_image)


```


vi)Image Cropping
```python
crop_img = image[100:800 ,400:1200]

plt.axis("off")
plt.imshow(crop_img)
plt.show()


```





## Output:
### i)Image Translation

![1](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/5204e325-7b3c-419ab26d-5dba6031bd6a)
![2](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/25be0067-8d6e-4f65-ad5f-e53c3a442117)



### ii) Image Scaling
![](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/d8b18011-9e97-4f49-a7ad-b97be97acd8d)


### iii)Image shearing

![1](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/8999b210-87a9-44c8-9831-d1a256dddaf8)
![2](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/a7543f42-9260-49a3-9248-a9a5bf98a43f)

### iv)Image Reflection

![3](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/0c2fb47a-be57-4aba-aaea-3b45660b2e76)

![4](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/0d7dfd2e-c30e-4185-a923-2596ec9caeec)

### v)Image Rotation

![5](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/eec5056f-6dff-4c60-9794-15261c5468d8)



### vi)Image Cropping

![6](https://github.com/praveenst13/IMAGETRANSFORMATION/assets/118787793/77551f19-9d3c-4da2-9c8f-7cf5a8b90ba1)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
