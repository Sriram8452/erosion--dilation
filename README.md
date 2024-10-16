# EX 09 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
## Program:
```
NAME: Sriram G
REG.NO: 212222230149
```

### Import the necessary packages
``` 
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "Sriram G"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```
### Create the structuring element
``` 
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Erode the image
``` 
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")


```
### Dilate the image
``` 
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

```

## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/f2326d07-0026-4e0c-a83b-4b5a82c5ec8a)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/7f7a3d36-20c4-4600-b2e6-46abc9ff2c02)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/13841f9a-a2b3-4989-8fb2-43713cadc6af)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
