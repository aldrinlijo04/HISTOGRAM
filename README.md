# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```
# Developed By: Aldrin Lijo J E
# Register Number: 212222240007
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('gray.jpeg')
color_image = cv2.imread('doge.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
Gray Scale Image
![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/24e06dec-a268-4385-9995-bfdb186d3297)


Color Image

![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/812df2e2-8557-4670-a4a8-f420d0316178)

<br>

### Histogram of Grayscale Image and any channel of Color Image
Gray Scale Image
![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/3278b6fd-3ac8-4cb7-a99e-32a4bcc674ff)

Color Image
![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/a9ae9d1c-7864-41ed-b37f-26bb28982908)

<br>

### Histogram Equalization of Grayscale Image

Original Image
![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/6af557a8-e051-4b9e-bf40-d737b9be28e5)



Equalized Image

![download](https://github.com/aldrinlijo04/HISTOGRAM/assets/118544279/57741588-47b5-49ad-beda-84d8ec2020a2)


<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
