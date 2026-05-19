# Image-Handling-and-Pixel-Transformations-Using-OpenCV
## Name: SRI HARI KRSISHNA DT 
## Register Number: 212224240160
## AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)
Algorithm:
## Step 1:
Load an image from your local directory and display it.

## Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

## Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

## Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

## Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels



## 1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```
import cv2

img = cv2.imread('Eagle_in_Flight.jpg', 0)

print("Image Loaded Successfully")
```
## 2. Print the image width, height & channel.
```
height, width = img.shape

print("Width :", width)
print("Height :", height)
print("Channels : Grayscale Image")
```
## 3. Display the image using Matplotlib imshow().
```
import matplotlib.pyplot as plt

plt.imshow(img, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
plt.show()
```
## 4. Save the image as a PNG file using OpenCV imwrite().
```
cv2.imwrite('Eagle_Output.png', img)

print("Image Saved Successfully")
```
## 5. Read the saved image above as a color image using cv2.cvtColor().
```
color_img = cv2.imread('Eagle_Output.png')

rgb_img = cv2.cvtColor(color_img, cv2.COLOR_BGR2RGB)

print("Color Image Converted Successfully")
```
## 6. Display the RGB image.
```
plt.imshow(rgb_img)
plt.title("RGB Image")
plt.axis('off')
plt.show()
```
## 7. Resize the image.
```
resized = cv2.resize(rgb_img, (300, 300))

plt.imshow(resized)
plt.title("Resized Image")
plt.axis('off')
plt.show()
```
## 8. Rotate the image.
```
rotated = cv2.rotate(rgb_img, cv2.ROTATE_90_CLOCKWISE)

plt.imshow(rotated)
plt.title("Rotated Image")
plt.axis('off')
plt.show()
```
## 9. Crop the image.
```
cropped = rgb_img[50:250, 50:250]

plt.imshow(cropped)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
## 10. Convert the image into binary format using thresholding.
```
_, binary = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)

plt.imshow(binary, cmap='gray')
plt.title("Binary Image")
plt.axis('off')
plt.show()
```
## 11. Detect edges using Canny Edge Detection.
```
edges = cv2.Canny(img, 100, 200)

plt.imshow(edges, cmap='gray')
plt.title("Edge Detection")
plt.axis('off')
plt.show()
```
## 12. Save the processed output images.
```
cv2.imwrite('Resized_Image.png', resized)
cv2.imwrite('Rotated_Image.png', rotated)
cv2.imwrite('Cropped_Image.png', cropped)
cv2.imwrite('Binary_Image.png', binary)
cv2.imwrite('Edges_Image.png', edges)

print("All Processed Images Saved")
```
## Output:
<img width="596" height="395" alt="image" src="https://github.com/user-attachments/assets/c3b0a959-fd8d-4aff-8959-ab5cb836e019" />
<img width="624" height="391" alt="image" src="https://github.com/user-attachments/assets/d6f9be8f-5317-42db-98f6-97ab6b38c51a" />
<img width="583" height="391" alt="image" src="https://github.com/user-attachments/assets/f7c828a1-6b08-47e4-8388-bd99bd94d36a" />
<img width="584" height="388" alt="image" src="https://github.com/user-attachments/assets/b40edccd-3c78-4156-8f1c-529a4a6c952c" />
<img width="600" height="390" alt="image" src="https://github.com/user-attachments/assets/6b3d2d62-baa6-439f-a55d-35980b866401" />
<img width="614" height="388" alt="image" src="https://github.com/user-attachments/assets/a6f6d426-0f60-4e5f-af40-f13c5ceba937" />
<img width="558" height="397" alt="image" src="https://github.com/user-attachments/assets/15ac3e79-d89a-4587-b72a-9c2496de2b29" />
<img width="584" height="398" alt="image" src="https://github.com/user-attachments/assets/d861c0d1-4483-4f31-ad22-4e412fda5852" />
<img width="575" height="395" alt="image" src="https://github.com/user-attachments/assets/404a80d0-6f58-4340-ab29-a1216673f045" />
<img width="566" height="390" alt="image" src="https://github.com/user-attachments/assets/96e5cb36-fe9d-4041-9858-4d445d36a3b0" />
<img width="560" height="398" alt="image" src="https://github.com/user-attachments/assets/511c5148-4bcb-4bd8-9c67-88eeb974e619" />
<img width="473" height="386" alt="image" src="https://github.com/user-attachments/assets/3e36c0a6-e2bc-4e02-bddf-06d7768ff191" />
<img width="521" height="289" alt="image" src="https://github.com/user-attachments/assets/e89a1c7c-84a5-40fc-b3c3-d9a92250a820" />
<img width="544" height="387" alt="image" src="https://github.com/user-attachments/assets/6d81f003-5929-4f69-9298-022b46f452c4" />







## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program
