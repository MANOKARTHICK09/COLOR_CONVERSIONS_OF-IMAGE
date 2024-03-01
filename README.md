![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/f9dc54b6-d0dc-494f-94cf-0efc53ce95a3)# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:MANOKARTHICK  
### Register Number:22002165 




### i) Read and display the image
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Original Image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/6bc94562-9f90-4b39-88f3-e3de26b26142)


### ii)Write the image
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',0)
    cv2.imwrite('demos.jpg',image)

## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/eb1ee3dd-653a-49c9-810e-d570421d8f87)


### iii)Shape of the Image
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
    print(image.shape)

## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/9c274909-7e9e-4757-8f2a-001271188e86)


### iv)Access rows and columns
    import random
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/730318b4-02f0-4858-b4d3-9961d23a271e)


### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/a3a25bbd-eb8b-41c9-8ee9-2a5fedd16f5a)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
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
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/4da8bd49-f5d9-4963-834f-79dfad4f8f39)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg')
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
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/a492b3c1-71c4-47d5-a28a-b5dfbab303dc)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/8c04c935-d94f-4d58-877b-795fe5945c99)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
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
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/64fc71ab-944e-446b-836e-a89a758f2f4e)

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("pristine-reflective-lake-show-image-260nw-2305485315.jpg",1)
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
## Output:
![image](https://github.com/MANOKARTHICK09/COLOR_CONVERSIONS_OF-IMAGE/assets/121785458/be1d9a0b-1dea-4a34-82bd-6dc50beafe95)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







