# Histogram-of-an-images
## Aim
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


## Program:
```
# Developed By: Darshan V
# Register Number: 212224230050
```
## Gray Image and Color Image
```python
import cv2
gray_img = cv2.imread('B&W.jpg')
gray_img = cv2.resize(gray_img,(300,200))
color_img = cv2.imread('color.jpg')
color_img = cv2.resize(color_img,(300,200))
cv2.imshow("Gray Image",gray_img)
cv2.imshow("Colour Image",color_img)
cv2.waitKey(0)




```
## Output:

![image](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/7d3555af-9ed8-4d92-b68d-152acf28d13b)


![image](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/82ab73ad-bb90-4c6e-9040-d53249da5ca1)


## Histogram of Grayscale Image

``` python
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('B&W.jpg')
color_img = cv2.imread('color.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```









## Output:
![Screenshot 2024-03-22 111555](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/b54863d4-bada-4114-a7de-0e19ba739879)
## Histogram of Color Image
``` python
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('B&W.jpg')
color_img = cv2.imread('color.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```

## OUTPUT
![image](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/d4c61171-763f-420f-a8e3-bd167a213015)

## Histogram Equilization of GrayScale Image
``` python
import cv2
gray_img = cv2.imread('B&W.jpg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
```

## OUTPUT
![image](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/c0adb7b1-6ec9-43ae-a5a7-833c4a863658)       ![image](https://github.com/Goutham2306/Histogram-of-an-images/assets/138971154/2b207e69-5e92-4a89-942b-8b6f435c0e98)

## RESULT
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.


