# COLOR CONVERSION
### AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.
### Software Required:
Anaconda - Python 3.7
### Algorithm:
- Step1:Import cv2.
- Step2:Read the image file.
- Step3:Store the converted color in a variable.
- Step4:Display the color converted image windows.
- Step5:Destory and close the windows
### Program:

```
Developed By:  ROHIT JAIN D
Register Number: 212222230120
```
- i) Convert BGR and RGB to HSV and GRAY

```Python
import cv2
img = cv2.imread('blue.jpg',1)
img = cv2.resize(img,(400,300))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
- ii)Convert HSV to RGB and BGR

```Python
import cv2
img = cv2.imread('blue.jpg')
img = cv2.resize(img,(400,300))
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

- iii)Convert RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('blue.jpg')
img = cv2.resize(img,(400,300))
cv2.imshow('Original HSV Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

- iv)Split and Merge RGB Image

```Python
import cv2
image = cv2.imread('blue.jpg',1)
img = cv2.resize(img,(400,300))

blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]

cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)

merged = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
- v) Split and merge HSV Image
```Python
import cv2
image = cv2.imread("blue.jpg",1)
image = cv2.resize(image,(400,300))
image=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)

H,S,V=cv2.split(image)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',H)
cv2.imshow('Gray',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
- i) BGR and RGB to HSV and GRAY
![Screenshot 2023-09-09 203410](https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/6bf52123-6088-4327-a65e-955e29c9d3e8)

- ii) HSV to RGB and BGR
  ![Screenshot 2023-09-09 205114](https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/9db83a67-8f12-4b07-9c32-35acfa47944e)

- iii) RGB and BGR to YCrCb


- iv) Split and merge RGB Image

- v) Split and merge HSV Image

### Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
