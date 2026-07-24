# EXP 01 Image Handling and Pixel Transformations Using OpenCV

## Overview

This project demonstrates basic image processing techniques using **OpenCV** in Python. It covers reading and displaying images, adjusting brightness and contrast, cropping, resizing, flipping, drawing shapes, adding text, splitting and merging color channels, converting color spaces, and performing bitwise operations.

---

## Aim

To develop a Python program using OpenCV that performs the following operations:

- Read and display an image.
- Print image dimensions and channels.
- Save an image in another format.
- Convert grayscale images to color.
- Crop, resize, and flip images.
- Add text and draw rectangles.
- Adjust image brightness.
- Modify image contrast.
- Split and merge RGB channels.
- Split and merge HSV channels.
- Perform bitwise image operations.

---

## Software Requirements

- Python 3.7+
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib



## Algorithm

### Step 1
Read the input images (`c.jpg`) using OpenCV and display them using Matplotlib.

### Step 2
Obtain and print the image properties such as width, height, and number of channels. Save the grayscale image as a PNG file and read it again as a color image.

### Step 3
Perform basic image transformations by cropping the required object, resizing the image by a factor of 2, and flipping it horizontally.

### Step 4
Annotate the image by adding text and drawing a magenta rectangle around the required object using OpenCV drawing functions.

### Step 5
Adjust the image brightness by creating brighter and darker images, then modify the image contrast using suitable scaling factors.

### Step 6
Split the image into RGB and HSV color channels, display each channel separately, and merge them back to reconstruct the original image.

### Step 7
Apply bitwise image operations to generate a transformed image and display all the final output images.


## Program Developed By

**Name:** K. Ligneshwar

**Register Number:** 212223230113

---



## Python Code

### 1. Read an image using OpenCV.

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("C:/Users/admin/Downloads/c.jpg", cv2.IMREAD_COLOR)
```

---

### 2. Convert BGR image into RGB.

```python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

---

### 3. Display the image.

```python
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis("off")
plt.show()
```

---

### 4. Print image dimensions.

```python
img_rgb.shape
```

---

### 5. Draw Green Diagonal Lines.

```python
line_img = cv2.line(
    img_rgb,
    (0, 0),
    (736, 1308),
    (0, 255, 0),
    2
)

line_img = cv2.line(
    line_img,
    (736, 0),
    (0, 1308),
    (0, 255, 0),
    2
)

plt.imshow(line_img)
plt.title("Image with Green Diagonal Lines")
plt.axis("off")
plt.show()
```

---

### 6. Draw a Circle.

```python
circle_img = cv2.circle(
    img_rgb,
    (400,300),
    150,
    (255,0,0),
    10
)

plt.imshow(circle_img)
plt.title("Image with Circle")
plt.axis("off")
plt.show()
```

---

### 7. Draw a Green Square.

```python
square_img = cv2.rectangle(
    img_rgb,
    (250,150),
    (550,450),
    (0,255,0),
    10
)

plt.imshow(square_img)
plt.title("Image with Green Square")
plt.axis("off")
plt.show()
```

---

### 8. Add Text.

```python
text_img = cv2.putText(
    img_rgb,
    "OpenCV Drawing",
    (10,30),
    cv2.FONT_HERSHEY_SIMPLEX,
    1,
    (255,255,255),
    3
)

plt.imshow(text_img)
plt.title("Image with Text")
plt.axis("off")
plt.show()
```

---

### 9. Convert RGB to HSV.

```python
image_hsv = cv2.cvtColor(
    img_rgb,
    cv2.COLOR_RGB2HSV
)
```

---

### 10. Convert RGB to Gray.

```python
image_gray = cv2.cvtColor(
    img_rgb,
    cv2.COLOR_RGB2GRAY
)
```

---

### 11. Convert RGB to YCrCb.

```python
image_ycrcb = cv2.cvtColor(
    img_rgb,
    cv2.COLOR_RGB2YCrCb
)
```

---

### 12. Convert HSV back to RGB.

```python
image_hsv_to_rgb = cv2.cvtColor(
    image_hsv,
    cv2.COLOR_HSV2RGB
)
```

---

### 13. Replace white block with a New Image.

```python
# Read your new image
new_img = cv2.imread("C:/Users/admin/Downloads/L.jpeg")
new_img = cv2.cvtColor(new_img, cv2.COLOR_BGR2RGB)

# Resize to match the face region
new_img = cv2.resize(new_img, (270,350))

# Replace Ronaldo's face
img_rgb[120:470,250:520] = new_img

plt.imshow(img_rgb)
plt.title("Image Replaced with New Face")
plt.axis("off")
plt.show()
```

---

### 14. Resize the Image.

```python
resized_image = cv2.resize(
    img_rgb,
    (768//2,600//2)
)

plt.imshow(resized_image)
plt.title("Resized Image")
plt.axis("off")
plt.show()
```

---

### 15. Crop the Image.

```python
roi = img_rgb[50:350,50:350]

plt.imshow(roi)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

---

### 16. Flip Horizontally.

```python
flipped_horizontally = cv2.flip(
    img_rgb,
    1
)

plt.imshow(flipped_horizontally)
plt.title("Horizontally Flipped Image")
plt.axis("off")
plt.show()
```

---

### 17. Flip Vertically.

```python
flipped_vertically = cv2.flip(
    img_rgb,
    0
)

plt.imshow(flipped_vertically)
plt.title("Vertically Flipped Image")
plt.axis("off")
plt.show()
```


## Features

- Read grayscale and color images
- Display images using Matplotlib
- Save images in PNG format
- Crop objects
- Resize images
- Flip images horizontally
- Add text using `cv2.putText()`
- Draw rectangles using `cv2.rectangle()`
- Brightness adjustment
- Contrast enhancement
- RGB channel split and merge
- HSV channel split and merge
- Bitwise image operations

---

## Output
<img width="276" height="508" alt="image" src="https://github.com/user-attachments/assets/f530199d-7927-4c54-b0f0-7d7e07e9df21" />
<img width="280" height="508" alt="image" src="https://github.com/user-attachments/assets/a85da4d5-04ea-4c8e-8d51-449d2a5f4c04" />
<img width="282" height="507" alt="image" src="https://github.com/user-attachments/assets/8b560a15-e50b-429a-9ad5-d2356e4f55ae" />
<img width="280" height="512" alt="image" src="https://github.com/user-attachments/assets/ffcb8e05-c137-49e7-8bdf-70c42213b564" />
<img width="278" height="506" alt="image" src="https://github.com/user-attachments/assets/bd3a6134-5554-4968-865f-e17598f47977" />
<img width="282" height="507" alt="image" src="https://github.com/user-attachments/assets/9187db44-2f95-4a47-b121-f2618a5792b8" />
<img width="276" height="505" alt="image" src="https://github.com/user-attachments/assets/faad6e06-b6e3-4f05-b45b-79f20b41f17f" />
<img width="277" height="507" alt="image" src="https://github.com/user-attachments/assets/ff945793-cd8b-47f4-8a64-b648d2c5f259" />
<img width="276" height="507" alt="image" src="https://github.com/user-attachments/assets/a0894aba-22fd-45f0-b1ca-c62f63f5eb70" />
<img width="276" height="508" alt="image" src="https://github.com/user-attachments/assets/86e3eff6-1200-4de4-9596-df2dc31e4ed7" />
<img width="412" height="510" alt="image" src="https://github.com/user-attachments/assets/119365e7-7bb7-42f6-a9e3-87d271cbf2a2" />
<img width="612" height="510" alt="image" src="https://github.com/user-attachments/assets/f47da2fb-8eb1-426a-a118-27e9c4460b52" />
<img width="397" height="503" alt="image" src="https://github.com/user-attachments/assets/d65d23fa-8c3d-4a7d-8445-af6b4590fa46" />
<img width="277" height="506" alt="image" src="https://github.com/user-attachments/assets/eca6331b-1d6e-4961-a31a-36fa3b7d8f6c" />
<img width="280" height="501" alt="image" src="https://github.com/user-attachments/assets/6121f5a1-0393-4987-acef-e401f1844016" />



---

## Result

The objectives of the experiment were successfully achieved. Images were read, displayed, cropped, resized, flipped, annotated, and processed using OpenCV. Brightness and contrast adjustments, RGB and HSV channel operations, and bitwise transformations were successfully implemented using Python.

---

## Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

---

