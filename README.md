# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: A.ARUVI.
### Register Number: 212222230014.


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('vvijay.jpg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/5fdc7d90-89d4-4c01-96ac-08fde28a56da)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread("vvijay.jpg")

# Convert the image to RGB
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Get the dimensions of the image
height, width, _ = image.shape

# Draw a line across the full image
res = cv2.line(image, (0, 0), (width, height), (200, 100, 205), 10)

# Display the image
plt.imshow(res)
plt.axis('off')
plt.show()

```
![image](https://github.com/user-attachments/assets/d69afec5-623c-497e-86a7-93ed0001b465)

2. Draw a circle at the center of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image = cv2.resize(image,(500,500))
res = cv2.circle(image,(250,250), 150, (255, 0, 0), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/9a879bde-606f-4656-8752-2de4f6d868c4)

3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
import matplotlib.pyplot as plt

# Load and process the image
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Get image dimensions
height, width, _ = image.shape

# Draw a rectangle that spans the full image
top_left = (0, 0)  # Top-left corner
bottom_right = (width, height)  # Bottom-right corner
color = (200, 0, 0)  # Rectangle color in RGB (red)
thickness = 10  # Thickness of the rectangle border

res = cv2.rectangle(image, top_left, bottom_right, color, thickness)

# Display the resulting image
plt.imshow(res)
plt.axis('off')  # Hide the axes for better visualization
plt.show()

```
![image](https://github.com/user-attachments/assets/ee456a69-b4cc-4849-b596-b76289d6599f)


4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
res = cv2.putText(image,"VIJAY", (5,150), font,1.5, (0, 0, 0),5)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/93dd8e68-1081-425f-bef0-b858aa624ab5)


### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("VVIJAY.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
hsv2 = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
plt.imshow(hsv2)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/bb2ec5a9-96ca-4262-88c3-a04e388fc5c0)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
gray2 = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
plt.imshow(gray2)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/053aab58-a4d3-4fa4-99fb-abb361e3863d)



(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
YCrCb1 = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/e60ec037-b0dd-4946-85ae-84c5fc1667a8)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
BGR = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/2b0fbe17-faeb-4e78-96f7-d3709bc47905)

### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("vvijay.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
image[199, 199] = [255, 255, 255]
plt.imshow(image)
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/d6bdf9fe-fce0-4cb8-9d35-55fbcc23c5eb)



### v)Image Resizing:
Resize the original image to half its size and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("VVIJAY.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
resized_img = cv2.resize(image, (900, 1000))
plt.imshow(resized_img)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/163c18ad-5a4f-4229-904f-6bd87fb27298)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("VVIJAY.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
roi = image[50:50 + 425, 50:50 + 425]
plt.imshow(roi)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/f7ebc1ba-30d3-4e00-9374-918940a04dd1)

### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("VVIJAY.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res=cv2.rotate(image,cv2.ROTATE_180)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/e1481311-4249-455f-8171-7cce566b61af)


(2) Flip the original image vertically and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("VVIJAY.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(image)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/ce06b560-dd2d-460f-b7ef-288306fd6433)


### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("VVIJAY.jpg")
cv2.imwrite('VVIJAY_JOS.jpg',img)
```
![image](https://github.com/user-attachments/assets/90c899f7-0383-4345-9ff7-1509eba38c9f)

## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.






