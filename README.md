# COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By: Rohith
### Register Number: 212222230121


## Output:

### i) Read and display the image
```
    import cv2
    image=cv2.imread('dipt.png',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Lathikesh',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![Screenshot 2024-02-14 091346](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/f6250d9a-9a07-458b-8b0a-1920815f9b22)

<br>
<br>

### ii)Write the image
```
    import cv2
    image=cv2.imread('dipt.png',0)
    cv2.imwrite('lk.jpg',image)
```
![Screenshot 2024-02-14 092345](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/cf13492e-c0e8-4388-9c7a-4934bf7a44b5)

<br>
<br>

### iii)Shape of the Image
```
import cv2
image=cv2.imread('dipt.png',1)
print(image.shape)
```
![Screenshot 2024-02-14 092403](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/30a5e786-c98b-46e7-a2ed-6d74c0ce121c)

<br>
<br>

### iv)Access rows and columns
```
import random
import cv2
image=cv2.imread('dipt.png',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
        random.randint(0,255),
        random.randint(0,255)] 
cv2.imshow('image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-14 092557](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/49e52da8-235f-4c16-b579-c43ec3f1ee8f)

<br>
<br>

### v)Cut and paste portion of image
```
     import cv2
     image=cv2.imread('dipt.png',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
![Screenshot 2024-02-14 092720](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/26b71783-ebc0-46bd-b176-d6f9f0cedfda)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```
    import cv2
    img = cv2.imread('dipt.png',1)
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
![image](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/f409a02b-8ff2-4fa6-b40a-ced0e60f97b2)

<br>
<br>

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dipt.png')
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
![image](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/d389be5e-761b-4d2d-a3ba-0c5887db833c)

<br>
<br>

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dipt.png')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/2acc4eb1-30e6-4a2d-bc88-9588bc2888c7)

<br>
<br>

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dipt.png')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/0f7b555d-f238-4065-a80c-afe5703e9912)

<br>
<br>

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dipt.png",1)
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

![image](https://github.com/LATHIKESHWARAN/COLOR_CONVERSIONS_OF-IMAGE/assets/119393556/b634a5ba-47b1-4546-acc5-35aac65f8f15)

<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







