# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Read the image using cv2.imread()

### Step2:
convert the BGR image to HSV and HSV to BGR using cv2.cvtColor() and display it using imshow()

### Step3:
split the BGR image using image[:,:,0] like array or cv2.split()

### Step4:
merge the image using cv2.merge() and display it using imshow()

### Step5:
close the window using cv2.waitKey() and cv2.destroyAllWindows()

## Program:
# Developed By:Karthikeyan.K
# Register Number:212221230046
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
BGR_image=cv2.imread('bgr.jpg')
cv2.imshow('BGR_Image',BGR_image)
#BGR2HSV
hsv_image=cv2.cvtColor(BGR_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
cv2.imwrite('hsv.jpg',hsv_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```
import cv2
HSV_image=cv2.imread('hsv.jpg')
cv2.imshow('HSV_Image',HSV_image)
#HSV2BGR
bgr_image=cv2.cvtColor(HSV_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgr_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
BGR_image=cv2.imread('bgr.jpg')
cv2.imshow('BGR_Image',BGR_image)
#BGR2YCrCb
YCrCb_image=cv2.cvtColor(BGR_image,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iv)Split and Merge RGB Image
```
import cv2
BGR_image=cv2.imread('bgr.jpg')
blue=BGR_image[:,:,0]
green=BGR_image[:,:,1]
red=BGR_image[:,:,2]
cv2.imshow('BGR_Blue',blue)
cv2.imshow('BGR_Green',green)
cv2.imshow('BGR_Red',red)
merge_bgr=cv2.merge((blue,green,red))
cv2.imshow('merge_bgr',merge_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# v) Split and merge HSV Image
```
import cv2
hsv_image=cv2.imread('hsv.jpg')
h, s, v = cv2.split(hsv_image)
cv2.imshow('h',h)
cv2.imshow('s',s)
cv2.imshow('v',v)
merge_hsv=cv2.merge((h,s,v))
cv2.imshow('merge_hsv',merge_hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY

BGR

![op](op1_1.png)

BGR to HSV

![op](op1_2.png)

### ii) HSV to RGB and BGR

HSV

![op](op2_1.png)

HSV to BGR

![op](op2_2.png)

### iii) RGB and BGR to YCrCb
BGR

![op](op3_1.png)

BGR to YCrCb

![op](op3_2.png)

### iv) Split and merge RGB Image

BLUE

![op](op4_1.png)

GREEN

![op](op4_2.png)

RED

![op](op4_3.png)

MERGED

![op](op4_4.png)

### v) Split and merge HSV Image

H

![op](op5_1.png)

S

![op](op5_2.png)

V

![op](op5_3.png)

MERGED

![op](op5_4.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
