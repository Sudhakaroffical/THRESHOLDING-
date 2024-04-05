# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding, and Otsu's thresholding using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Import necessary packages

### Step2:
Read the image

### Step3:
If the read image is a color image, convert it into a grayscale image

### Step4:
perform the threshold operation you want to do(global thresholding or adaptive thresholding or otsu's 
thresholding)

### Step5:
Display the Results


## Program
```
Developed By: SUDHAKAR K
Register No: 212222240107
```
```python
# Load the necessary packages

import cv2



# Read the Image and convert it to grayscale

img = cv2.imread('DIPT-8.jpeg',-1)
cv2.imshow('original_image',img)
cv2.waitKey(0)
cv2.destroyAllWindows
gray =cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('gray_image',gray)
cv2.waitKey(0)
cv2.destroyAllWindows


# Use Global thresholding to segment the image

ret,thresh_img1=cv2.threshold(gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(gray,100,255,cv2.THRESH_TRUNC)


# Use Adaptive thresholding to segment the image

thresh_img6=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img7=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)


# Use Otsu's method to segment the image 

ret,thresh_img8=cv2.threshold(gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)



# Display the results

image =[thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
for i in range(0,8):
    cv2.imshow('threshold_image',image[i])
    cv2.waitKey(0)
    cv2.destroyAllWindows



```
## Output

### Original Image
![Screenshot 2024-04-05 142940](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/82e3a131-6b6f-4a38-9b9b-005e7d5cda97)



### Global Thresholding
![Screenshot 2024-04-05 143010](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/3555b1ca-b2d1-4f46-a0ce-0727b612c8b7)
![Screenshot 2024-04-05 143035](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/6eb12d44-1bc7-46ab-b26d-8d6de3f8f251)

![Screenshot 2024-04-05 143053](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/10d518e8-fa1f-4955-98b0-4ecc0d84626d)
![Screenshot 2024-04-05 143140](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/dc678138-dd08-4cf3-ab5d-1172b10ef865)


![Screenshot 2024-04-05 143205](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/4df8fc3c-01b4-410e-9099-d647a9c04645)

![Screenshot 2024-04-05 143218](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/696e00ec-67ee-43db-8a11-aad444f060e3)




### Adaptive Thresholding
![Screenshot 2024-04-05 143234](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/8c4cba13-bcbf-4e2d-8533-b03f7510d905)

![Screenshot 2024-04-05 143251](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/b60df8f8-1792-43d4-92fe-8f29c04cf95f)




### Optimum Global Thresholding using Otsu's Method
![Screenshot 2024-04-05 143305](https://github.com/Sudhakaroffical/THRESHOLDING-/assets/118622513/bc3160fc-04d2-4fb1-93b3-0abfa5d260f0)



## Result
Thus the images are segmented using global thresholding, adaptive thresholding, and optimum global thresholding using Python and OpenCV.

