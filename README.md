# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import all the required packages.

## Step2:
Load the image to operate on.

## Step3:
Convert the image to grayscale image.

## Step4:
Use Sobel operator along x,y and xy directions.

## Step5:
Operate the image using Laplacian operator.

## Step6:
Operate the image using Canny Edge operator.

## Step7:
Show all the operated images output.

## Step8:
End the program.

 
## Program:

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
image = cv2.imread("car.jpeg")
grayImage = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("OriginalImage",image)
cv2.imshow("GrayscaleImage",grayImage)
smoothImage = cv2.GaussianBlur(grayImage,(3,3),0)


# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(smoothImage,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(smoothImage,cv2.CV_64F,0,1,ksize=5)
sobelxy = cv2.Sobel(smoothImage,cv2.CV_64F,1,1,ksize=5)



# LAPLACIAN EDGE DETECTOR

laplacian = cv2.Laplacian(smoothImage,cv2.CV_64F)



# CANNY EDGE DETECTOR

cannyEdges = cv2.Canny(smoothImage,120,150)

plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(smoothImage,cmap = 'gray')
cv2.imshow("sobelx",sobelx)
cv2.imshow("sobely",sobely)
cv2.imshow("sobelxy",sobelxy)
cv2.imshow("Laplacian",laplacian)
cv2.imshow("Canny Edges",cannyEdges)
plt.title("Original")
plt.xticks([])
plt.yticks([])
plt.show()

```
## Output:
## Importing

![java 1](https://user-images.githubusercontent.com/93427224/168482889-c13e0d6f-424c-479f-a5c9-0f37023eca40.png)
![java 2](https://user-images.githubusercontent.com/93427224/168482896-9009![java 3](https://user-images.githubusercontent.com/93427224/168482900-64c36cc1-4d08-4663-883c-4fc17e5c7e27.png)
9bfb-076a-4d8e-90f2-947417ae18ca.png)

### SOBEL EDGE DETECTOR

![java 4](https://user-images.githubusercontent.com/93427224/168482970-c7009920-b741-4eca-bc11-83d2777bb253.png)
![java 5](https://user-images.githubusercontent.com/93427224/168482973-a1212a5f-f490-4dfd-a165-236952be4c6f.png)
![java 6](https://user-images.githubusercontent.com/93427224/168482976-ca2904b6-a6fe-4a42-ba9d-3b1caa820188.png)


### LAPLACIAN EDGE DETECTOR

![java 7](https://user-images.githubusercontent.com/93427224/168482961-a1d171f6-baa1-4dfb-9de4-3df9b347c08e.png)


### CANNY EDGE DETECTOR

![java 8](https://user-images.githubusercontent.com/93427224/168482934-561db23e-e40e-4a1b-a8eb-de5858348704.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
