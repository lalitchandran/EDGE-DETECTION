# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY: NISHA D
REGISTER NUMBER: 212223230143
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Load the image
```
image = cv2.imread('Fish.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
# Apply Sobel edge detector
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
```
# Apply Laplacian edge detector
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
```
# Apply Canny edge detector
```
canny_edges = cv2.Canny(gray_image, 50, 150)
```

# Display results using Matplotlib
```
plt.figure(figsize=(12, 12))
```

# Original Image
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
# Sobel Edge Detection
```
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
# Laplacian Edge Detection
```
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
# Canny Edge Detection
```
plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
# Show all results
```
plt.tight_layout()
plt.show()

```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/user-attachments/assets/ae58e868-9bcc-415d-8f88-381d8328a5b4)


### SOBEL EDGE DETECTOR:
![image](https://github.com/user-attachments/assets/cdfdcf36-831f-4162-b94f-484a9cae2fb9)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/62553140-4e46-476c-81c0-c8f12e52951b)


### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/cbed176f-439a-4bb2-be37-7c7476bcda94)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
