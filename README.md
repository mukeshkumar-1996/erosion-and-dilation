# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

**Name:** Mukeshkumar V

**Register No:** 212225230193

## Output

### Original Image

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image.png")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="683" height="467" alt="Screenshot 2026-09-16 164731" src="https://github.com/user-attachments/assets/b4b7fba0-00ef-4593-853c-82b84906e379" />



### Erosion

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
<img width="681" height="465" alt="Screenshot 2026-09-16 164738" src="https://github.com/user-attachments/assets/0bf38df0-4309-4d71-8d73-648c69f18e6b" />


### Dilation

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
<img width="687" height="464" alt="Screenshot 2026-09-16 164745" src="https://github.com/user-attachments/assets/c159f50d-c319-4a3a-b68e-924e03e91f40" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
