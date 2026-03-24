# EX-09 Implementation-of-Erosion-and-Dilation
# Name: SHARAN G
# Register no: 212223230203

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:  
 import the neccesary packages


### Step2:  
create the text using cv2.put Text

### Step3:  
create the structuting element

### Step4:  
  Erodde the image

### Step5:  
 Dilate the image

 
## Program:

# Import the necessary packages
```python 
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

# Create the text using cv2.putText
```python
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'GOKUL', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

# Create the structuring element
```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
# Erode the image
```python
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```


# Dilate the image
```python
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```

## Output:

### Display the input Image
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/705a4a53-c19a-402a-8e7d-49202ec54062" />

### Display the Eroded Image
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/dde189ef-5c7d-4526-baf4-c9d779399382" />

### Display the Dilated Image
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/8b2cd6eb-af96-4b56-96ff-689d3c164c27" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
