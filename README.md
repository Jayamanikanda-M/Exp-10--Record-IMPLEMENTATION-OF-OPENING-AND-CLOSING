# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING

# Aim
To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

Morphological Opening

Morphological Closing

# Software Used
. Anaconda – Python 3.7

. Jupyter Notebook / VS Code

. OpenCV (cv2)

. NumPy

. Matplotlib

# Algorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Create or load an input image containing foreground objects.

Step 3:
Display the original image.

Step 4:
Create a structuring element (kernel) of suitable size.

Step 5: Opening Operation
Apply the Opening operation using the structuring element. Opening consists of Erosion followed by Dilation. Remove small foreground noises while preserving the shape of larger objects. Display the opened image.

Step 6: Closing Operation
Apply the Closing operation using the structuring element. Closing consists of Dilation followed by Erosion. Fill small holes and gaps within foreground objects. Display the closed image.

Step 7:
Compare the original, opened, and closed images.

# Program
Developed By

# Name: JAYAMANIKANDA M
# REG NO.: 212225230113


ORIGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HEY BUDDY', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```

OPENING OPERATION
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```

CLOSING OPERATION
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  
plt.title("Closing Operation")
plt.axis('off')
```
# Output:
Original Image

<img width="557" height="447" alt="image" src="https://github.com/user-attachments/assets/80931fac-9820-4212-ad6f-987e7358e9ce" />


The input image is displayed. The image serves as the source for morphological processing.

Opening Operation
<img width="560" height="451" alt="image" src="https://github.com/user-attachments/assets/a64ad549-58d6-422a-bd63-1ee85e844179" />



Original image is displayed. Opened image is displayed. Small foreground noise is removed. Thin protrusions and isolated pixels are eliminated. Object boundaries become smoother.

Closing Operation

<img width="590" height="442" alt="image" src="https://github.com/user-attachments/assets/63311fbc-f00b-458c-899f-0a17477bba7e" />


Original image is displayed. Closed image is displayed. Small holes and gaps inside objects are filled. Broken regions are connected. Object boundaries become more continuous.

# Applications
Opening
. Noise removal in binary images.

. Separation of connected objects.

. Preprocessing for object detection.

Closing
. Filling small holes in objects.

. Connecting nearby components.

. Enhancing segmented regions.

Advantages
Opening
. Removes unwanted foreground noise.

. Preserves major object structures.

. Improves segmentation quality.

Closing
. Restores object continuity.

. Eliminates small background gaps.

. Improves object representation.


# Result:

Thus, the morphological operations Opening and Closing are successfully implemented using OpenCV.
