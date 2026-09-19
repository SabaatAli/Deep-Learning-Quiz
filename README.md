# Deep-Learning-Quiz
QUIZ REPORT
Image Separation and Border Addition Task

**Tool Used: Google Colab**

**1. Objective**
The objective of this quiz task is to process one image containing five separate receipt/picture regions using Computer Vision techniques. The input image is analyzed using OpenCV to identify and separate the required regions. Each separated region is cropped into an individual image, a 10-pixel black border is added around it, and the five processed images are saved separately.
________________________________________
**2. Task Description**
The input image is provided as /content/input_image.jpeg in Google Colab. The task is to separate five receipt regions using a Computer Vision-based image-processing approach rather than relying only on manually specified pixel coordinates.
The solution uses OpenCV for grayscale conversion, Gaussian blurring, adaptive thresholding, morphological processing, contour detection, and region analysis. When fewer than five separate regions are detected by contours, an additional projection/layout-based separation method is used to obtain the five required regions.
After separation, a 10-pixel black border is added to every output image. The five images are saved as individual JPG files and are also combined into a ZIP archive.
________________________________________
**3. Tools and Libraries**
Tool/Library	Purpose	Application
Google Colab 	Python execution environment	Run the complete Computer Vision task online
Python	Programming language	Image processing and file handling
OpenCV (cv2)	Computer Vision library	Grayscale conversion, filtering, thresholding, morphology, contours, and image processing
NumPy	Numerical processing	Projection and image-region analysis
Pillow (PIL)	Image processing	Add borders and save output images
OS	File management	Create the output directory
shutil	File management	Create the ZIP archive
________________________________________
**4. Methodology**
1.	Load the original image from /content/input_image.jpeg. 
2.	Read the image using OpenCV. 
3.	Convert the image from color to grayscale. 
4.	Apply Gaussian Blur to reduce noise. 
5.	Apply adaptive thresholding to highlight relevant image regions. 
6.	Apply morphological closing to improve connected regions. 
7.	Detect external contours using OpenCV. 
8.	Calculate bounding boxes for the detected regions. 
9.	Filter out very small or unsuitable regions. 
10.	Check whether five separate regions have been detected. 
11.	If fewer than five regions are detected, use projection/layout analysis to separate the five receipt areas. 
12.	Sort the detected regions from top-to-bottom and left-to-right. 
13.	Crop each of the five regions from the original image. 
14.	Add a 10-pixel black border around each cropped image. 
15.	Save the five images in /content/separated_cv_images. 
16.	Create separated_cv_images.zip containing all five output images. 
________________________________________
**5. Computer Vision Process**********
The complete image-processing process can be represented as:
Input Image → Grayscale Conversion → Gaussian Blur → Adaptive Thresholding → Morphological Processing → Contour Detection → Region Analysis → Five Image Regions → Cropping → Border Addition → Output Images
The main Computer Vision techniques used in this process are:
•	Grayscale conversion 
•	Gaussian filtering 
•	Adaptive thresholding 
•	Morphological closing 
•	Contour detection 
•	Bounding-box detection 
•	Projection/layout analysis 
•	Image cropping 
________________________________________
**6. Explanation of Important Components**
Function/Component	Purpose
Image Loading	Loads the input image into the program.
Grayscale Conversion	Converts the color image into grayscale for easier processing.
Gaussian Blur	Reduces noise and small unwanted details.
Adaptive Thresholding	Separates useful foreground information from the background.
Morphological Processing	Improves and connects useful image regions.
Contour Detection	Detects boundaries of possible receipt regions.
Bounding Boxes	Defines rectangular regions around detected objects.
Region Filtering	Removes regions that are too small or unsuitable.
Projection/Layout Analysis	Provides an additional separation method when contour detection finds fewer than five regions.
Cropping	Extracts each identified receipt region from the original image.
Border Addition	Places a black border around each separated image.
Image Saving	Stores each processed receipt as an individual JPG file.
ZIP Creation	Combines all five output images into one ZIP archive.
________________________________________
**7. Expected Output**
The program creates the following output folder:
/content/separated_cv_images/
The folder contains five separated images:
1.	receipt_1_bordered.jpg 
2.	receipt_2_bordered.jpg 
3.	receipt_3_bordered.jpg 
4.	receipt_4_bordered.jpg 
5.	receipt_5_bordered.jpg 
Each output image contains one separated receipt region with a 10-pixel black border.
________________________________________

