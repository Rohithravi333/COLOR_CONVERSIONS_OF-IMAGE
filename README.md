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

##### Program:btech ai&ds
### Developed By:rohith r
### Register Number: 212222230121


### i) Read and display the image
   ```  import cv2
        image=cv2.imread('ro.jpg',1)
        image=cv2.resize(image,(400,300))
        cv2.imshow('rohith',image)
        cv2.waitKey(0)
        cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-02-16 090400](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/6dee557b-3c3a-4cef-a06e-e6af513209da)

### ii)Write the image
```
    import cv2
    image=cv2.imread('ro.jpg',0)
    cv2.imwrite('NOPE.jpg',image)
```
### OUTPUT

![Screenshot 2024-02-16 101901](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/fe248e4b-ecd5-470e-ba32-088317f51988)

### iii)Shape of the Image

```
    import cv2
    image=cv2.imread('ro.jpg',1)
    print(image.shape)
```
### OUTPUT
![Screenshot 2024-02-16 102119](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/7edd9391-39b9-458e-b248-cc0e0851d417)


### iv)Access rows and columns
```
     import random
     import cv2
     image=cv2.imread('ro.jpg',1)
     image=cv2.resize(image,(400,400))
     for i in range (150,200):
       for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
     cv2.imshow('part image',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()```

```
### OUTPUT
![Screenshot 2024-02-16 090400](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/354f7f44-79a4-43ae-9a3e-2cd860d5b82f)

### v)Cut and paste portion of image
```
     import cv2
     image=cv2.imread('ro.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
### OUTPUT
![Screenshot 2024-02-16 091251](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/88fd6e1b-39ac-4152-883f-f050182f7d29)


### vi) BGR and RGB to HSV and GRAY
```
    import cv2
    img = cv2.imread('ro.jpg',1)
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
### OUTPUT
![Screenshot 2024-02-16 092147](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/975daf74-cb9d-4d58-97ba-8f54552bab67)![Screenshot 2024-02-16 091954](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/7eeac46b-fd95-4e31-aa3e-259c764af276)![Screenshot 2024-02-16 091942](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/3f41f87f-c426-4e2d-8c52-dc2375c964d0)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dip.jpg')
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
### OUTPUT
![Screenshot 2024-02-16 110853](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/f2c02d9e-bb12-49fe-9d76-f2a454dd91bd)
![Screenshot 2024-02-16 110902](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/075ad5e1-b5a2-4f63-9085-eefa3aaa22c6)
![Screenshot 2024-02-16 110910](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/8007db55-05fd-43f7-bf8a-27be947c408c)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dip.jpg',1)
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
### OUTPUT

![Screenshot 2024-02-16 111630](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/cd576493-4c12-4faa-a62c-f221af3a398e)
![Screenshot 2024-02-16 111639](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/dd5d5ac9-d529-44fe-b792-e6212dc893ed)
![Screenshot 2024-02-16 111649](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/2f77dc85-784b-40ae-a3ae-e2bfb2d11841)
![Screenshot 2024-02-16 111659](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/7128237f-ed9b-4fc7-8576-0171b37dd040)

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dip.jpg",1)
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
### OUTPUT
![Screenshot 2024-02-16 110139](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/4efeb6e8-54e1-4227-b3e2-89af79c81e9b)
![Screenshot 2024-02-16 110149](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/ab9a592d-8212-4329-ac87-0ddbf3425bfe)
![Screenshot 2024-02-16 110204](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/9c362f85-9316-4e99-8f56-ddcdbb6c353d)
![Screenshot 2024-02-16 110213](https://github.com/Rohithravi333/COLOR_CONVERSIONS_OF-IMAGE/assets/119394126/931b3ca4-b9c9-482d-83d5-7f349d37973e)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







