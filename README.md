# Image Processing

This repository contains the source code for an image processing project demonstrating the fundamental concepts and techniques in image manipulation. This project is designed to help beginners understand how to process and transform images using Python and OpenCV.

<hr><br>

## Purpose of This Repository

To provide a foundational understanding of image processing and demonstrate how to apply various transformations and operations on images.

<hr><br>

## Demonstration

Below is a demonstration of a simple Python code structure for image processing:

```python
import cv2
import numpy as np

# Load an image
image = cv2.imread('sample.jpg')

# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Create a binary image using thresholding
_, binary_image = cv2.threshold(gray_image, 128, 255, cv2.THRESH_BINARY)

# Apply a translation
rows, cols = image.shape[:2]
translation_matrix = np.float32([[1, 0, 50], [0, 1, 50]])
translated_image = cv2.warpAffine(image, translation_matrix, (cols, rows))

# Display the results
cv2.imshow('Original Image', image)
cv2.imshow('Grayscale Image', gray_image)
cv2.imshow('Binary Image', binary_image)
cv2.imshow('Translated Image', translated_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

<hr><br>

## Features

- Image loading and displaying
- Grayscale conversion
- Binary thresholding
- Image translation

<hr><br>

## Technologies Used

- Python
- OpenCV

<hr><br>

## Project Setup

1. **Clone this Repository**

```bash
git clone https://github.com/n4vrl0s3/Image-Processing.git
```

2. **Install the required Python packages**

```bash
pip install opencv-python numpy matplotlib 
```

<hr><br>

## Steps to Run

1. **Ensure you have the required Python packages installed**
2. **Run the Python script in your preferred IDE or terminal**

<hr><br>

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

<hr><br>

<div align="center">
  <a href="https://www.x.com/n4vrl0s3/">
    <img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=100:49108B,20:F3F8FF&section=footer&reversal=false&textBg=false&fontAlignY=50&descAlign=48&descAlignY=59"/>
  </a>
</div>