# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
# Developed By:Karthikeyan.K
# Register Number:212221230046
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
BGR_image=cv2.imread('bgr.jpg')
cv2.imshow('BGR_Image',BGR_image)
#BGR2HSV
hsv_image=cv2.cvtColor(house_color_image,cv2.COLOR_BGR2HSV)
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
bgr_image=cv2.cvtColor(house_color_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgr_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
house_color_image=cv2.imread('bgr.jpg')
cv2.imshow('BGR_Image',house_color_image)
#BGR2YCrCb
YCrCb_image=cv2.cvtColor(house_color_image,cv2.COLOR_BGR2YCrCb)
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
house_color_image=cv2.imread('hsv.jpg')
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
<br>
<br>

### ii) HSV to RGB and BGR
<br>
<br>

### iii) RGB and BGR to YCrCb
<br>
<br>

### iv) Split and merge RGB Image
<br>
<br>

### v) Split and merge HSV Image
<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
