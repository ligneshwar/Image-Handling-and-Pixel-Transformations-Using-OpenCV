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

---

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
---

## Program Developed By

**Name:** K. Ligneshwar

**Register Number:** 212223230113

---


---

## Python Libraries

```python
## Experiment

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

### 5. Draw a line.

```python
line_img = cv2.line(
    img_rgb,
    (0,0),
    (768,600),
    (255,0,0),
    2
)
```

---

### 6. Draw a circle.

```python
circle_img = cv2.circle(
    img_rgb,
    (400,300),
    150,
    (255,0,0),
    10
)
```

---

### 7. Draw a rectangle.

```python
rectangle_img = cv2.rectangle(
    img_rgb,
    (0,0),
    (736,1308),
    (0,0,255),
    10
)
```

---

### 8. Add text.

```python
text_img = cv2.putText(
    img_rgb,
    "OpenCV Drawing",
    (10,30),
    cv2.FONT_HERSHEY_SIMPLEX,
    1,
    (255,255,255),
    10
)
```

---

### 9. Convert RGB to HSV.

```python
image_hsv = cv2.cvtColor(
    image_rgb,
    cv2.COLOR_RGB2HSV
)
```

---

### 10. Convert RGB to Gray.

```python
image_gray = cv2.cvtColor(
    image_rgb,
    cv2.COLOR_RGB2GRAY
)
```

---

### 11. Convert RGB to YCrCb.

```python
image_ycrcb = cv2.cvtColor(
    image_rgb,
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

### 13. Modify a 300×300 block.

```python
image[200:500,200:500] = [255,255,255]
```

---

### 14. Resize the image.

```python
resized_image = cv2.resize(
    image,
    (768//2,600//2)
)
```

---

### 15. Crop the image.

```python
roi = image[50:350,50:350]
```

---

### 16. Flip horizontally.

```python
flipped_horizontally = cv2.flip(
    image,
    1
)
```

---

### 17. Flip vertically.

```python
flipped_vertically = cv2.flip(
    image,
    0
)
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
<img width="285" height="508" alt="image" src="https://github.com/user-attachments/assets/e541a78e-4f4d-4139-9c14-58bb3300223a" />
<img width="280" height="502" alt="image" src="https://github.com/user-attachments/assets/511cc206-5a7c-4459-980e-8498f2e140c2" />
<img width="282" height="507" alt="image" src="https://github.com/user-attachments/assets/5dc7257c-ff94-4434-98f0-29c00be7746d" />
<img width="282" height="506" alt="image" src="https://github.com/user-attachments/assets/50f5ac2e-b7a5-434a-8d80-a81bdcefe2ea" />
<img width="278" height="506" alt="image" src="https://github.com/user-attachments/assets/8b442362-e8a6-422d-a93e-961fbc7d47a1" />
<img width="282" height="510" alt="image" src="https://github.com/user-attachments/assets/67597159-bf32-45d8-a15e-c95baf432c55" />
<img width="277" height="505" alt="image" src="https://github.com/user-attachments/assets/298f54d1-2c51-428c-9852-de2de36f031c" />
<img width="276" height="505" alt="image" src="https://github.com/user-attachments/assets/18253c3f-c01a-4dc3-90eb-900e98b144f6" />
<img width="280" height="502" alt="image" src="https://github.com/user-attachments/assets/10440196-19af-4172-b328-46ca0fcebb72" />
<img width="277" height="507" alt="image" src="https://github.com/user-attachments/assets/f610de95-2e7f-4592-9983-6320af722fbf" />
<img width="363" height="506" alt="image" src="https://github.com/user-attachments/assets/4d868cd0-5106-48a4-ab5b-6f836a8cbcb1" />
<img width="612" height="503" alt="image" src="https://github.com/user-attachments/assets/a1664f47-3970-4a38-90fc-6177355a0146" />
<img width="483" height="505" alt="image" src="https://github.com/user-attachments/assets/f81654ed-08a7-4f5b-9f1c-faa2d810ab33" />
<img width="281" height="502" alt="image" src="https://github.com/user-attachments/assets/367011d8-6032-4114-8d7b-b341f56473d1" />
<img width="281" height="508" alt="image" src="https://github.com/user-attachments/assets/15a524b8-ce18-4834-a5a4-eaeb56ffa98e" />


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

