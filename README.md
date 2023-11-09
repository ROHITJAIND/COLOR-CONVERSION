# EX-3 COLOR CONVERSION
### AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE:** 30.08.2023
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
#### i) Convert BGR and RGB to HSV and GRAY

```Python
import cv2
img = cv2.imread('blue.jpg',1)
img = cv2.resize(img,(300,200))
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
- Output
![Screenshot 2023-09-09 203410](https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/6bf52123-6088-4327-a65e-955e29c9d3e8)


#### ii) Convert HSV to RGB and BGR

```Python
import cv2
img = cv2.imread('blue.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

- Output
<img height=10% width=80% src="https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/9db83a67-8f12-4b07-9c32-35acfa47944e">

#### iii)Convert RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('blue.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

- Output
<img height=10% width=80% src="https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/3e1e4442-e10d-464a-8af7-b33c98f9a3c9">


#### iv) Split and Merge RGB Image

```Python
import cv2
img = cv2.imread('blue.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

- Output
![Screenshot 2023-09-10 104449](https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/672f040a-85db-4507-9fe1-e1bec2d6bdf8)

#### v) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("blue.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
- Output
![Screenshot 2023-09-10 105218](https://github.com/ROHITJAIND/COLOR-CONVERSION/assets/118707073/21cdd022-5e3c-4e02-9f43-dbc3e82d3605)
### Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
