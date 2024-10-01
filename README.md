# Histogram-of-an-images

## Aim:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program and Output:
```
Developed By: Gopika R
Reg No: 212222240031
```
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('img-1.jpg')
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.axis('on')
plt.show()
```
![Screenshot 2024-10-01 175310](https://github.com/user-attachments/assets/9bcb126b-cd31-4214-bd7c-a6aff97b6bf8)

```
color_image=cv2.imread('img-2.jpg')
plt.imshow(color_image)
plt.axis('on')
plt.show()
```
![Screenshot 2024-10-01 175318](https://github.com/user-attachments/assets/4eb414e8-3742-47b6-bdd4-510e40d07cc4)

### Histogram of Grayscale Image and any channel of Color Image

```
import numpy as np
Gray_image = cv2.imread("img-1.jpg")
Color_image = cv2.imread("img-2.jpg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
gray_hist = cv2.calcHist([grey],[0],None,[1100],[0,1100])
plt.figure()
plt.imshow(grey)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
![Screenshot 2024-10-01 175327](https://github.com/user-attachments/assets/51a3ee17-24fd-4207-a86e-1e13f80fa3a6)
![Screenshot 2024-10-01 175339](https://github.com/user-attachments/assets/95205326-eb08-44ef-bb38-bf55676db566)

```
color_hist = cv2.calcHist([Color_image],[0],None,[2600],[0,2600])
plt.figure() 
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
```
![Screenshot 2024-10-01 175350](https://github.com/user-attachments/assets/d07f4add-0dda-44ee-b87b-33b360d510db)
![Screenshot 2024-10-01 175359](https://github.com/user-attachments/assets/b824f7a0-3332-496e-b7d5-3175697af66a)


### Histogram Equalization of Grayscale Image
```
gray_image = cv2.imread("img-1.jpg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.show()
```
![Screenshot 2024-10-01 175408](https://github.com/user-attachments/assets/d408809f-cdfa-4491-89fe-032c6f8a74e4)
```
equ = cv2.equalizeHist(grey)
plt.imshow(equ)
plt.show()
```
![Screenshot 2024-10-01 175417](https://github.com/user-attachments/assets/c0f1150b-3bb8-447e-9aab-fa614c83d6ae)

```
color_image=cv2.imread('img-2.jpg')
grey=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
plt.imshow(color_image)
plt.show()
```
![Screenshot 2024-10-01 175429](https://github.com/user-attachments/assets/69e8a3f0-5946-406d-a44a-94ef7dcc35a3)
```
eq = cv2.equalizeHist(grey)
plt.imshow(eq)
plt.show()
```
![Screenshot 2024-10-01 175454](https://github.com/user-attachments/assets/6b8716da-4401-40df-9345-4eeacf5df194)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
