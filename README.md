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
### Developed By: A.ARUVI.
### Register Number: 212222230014.


## Output:

### i) Read and display the image
```
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/89903bc9-3f4f-42d1-96f8-b81bc3172710)


### ii)Write the image
```
import cv2
    image=cv2.imread('images.jpg',0)
    cv2.imwrite('natural.jpg',image)
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/0f290868-d4cf-44f6-b42d-015feeda7810)


### iii)Shape of the Image

```
import cv2
    image=cv2.imread('images.jpg',1)
    print(image.shape)
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/e5e5e834-6934-4933-a4cd-c53a4b83229e)

### iv)Access rows and columns
```
import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/1a490233-ebe6-4e13-8265-f21bc5a6aa7f)


### v)Cut and paste portion of image
```
 import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/a006adc3-9af9-4b38-87b2-e575a4ac37f5)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('images.jpg',1)
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
### OUTPUT:
![image](https://github.com/user-attachments/assets/8d4c5e6e-afb0-4551-9b53-d772e19d2233)

![image](https://github.com/user-attachments/assets/db54a1c8-d359-47d8-af2e-110405a31fec)

![image](https://github.com/user-attachments/assets/8e9498d4-7844-4f33-bcf2-0aa9c85d03b0)

![image](https://github.com/user-attachments/assets/0990a7c3-fbec-49a8-a92f-0cea32572082)

![image](https://github.com/user-attachments/assets/62bec632-c460-4e22-8524-7b5444766461)

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
````
### OUTPUT:
![image](https://github.com/user-attachments/assets/f87c6ab5-e303-45d9-99d9-56f71e67678a)

![image](https://github.com/user-attachments/assets/91ff00e2-0c6f-4c60-bedb-c37eb8d47cc1)

![image](https://github.com/user-attachments/assets/550c78d5-b83a-42b2-839c-722d89fe8781)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/c018c45f-cac3-4f08-855c-6d3e5ab71dbe)

![image](https://github.com/user-attachments/assets/af955f04-7ce2-4573-9af9-d8f3eecf05d3)

![image](https://github.com/user-attachments/assets/0fa496da-954e-4c9b-9afe-b47678c3639d)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('images.jpg',1)
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
### OUTPUT:
![image](https://github.com/user-attachments/assets/74b1e369-4619-4839-bdfb-77be9608e5da)

![image](https://github.com/user-attachments/assets/a448bb4e-c5f3-40ad-afbd-a37957b0e2eb)

![image](https://github.com/user-attachments/assets/b63b4969-9b4b-4a35-a708-f9577c371e16)

![image](https://github.com/user-attachments/assets/c7d052c7-e638-472c-a073-e9fd2235735e)

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("images.jpg",1)
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
### OUTPUT:
![image](https://github.com/user-attachments/assets/7ff42abd-dfc2-4672-bd23-f27f59fb35e4)

![image](https://github.com/user-attachments/assets/b97aade3-3a9f-4bbc-b947-450b5c38d79f)

![image](https://github.com/user-attachments/assets/620e16bf-dabe-4fa1-9050-25aafade8b81)

![image](https://github.com/user-attachments/assets/9aecb7a6-e1dc-4c8c-940e-c6d21188b389)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







