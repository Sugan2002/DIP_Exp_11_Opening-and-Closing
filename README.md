# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Plot the images using plt.imshow.

 
## Program:

```
Developed by : P.Suganya
Registeration Number:212220230049
```

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

text_image = np.zeros((100,200),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"AMMA",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))



# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```



## Output:

### Display the input image
![1](https://user-images.githubusercontent.com/77089743/172055089-0fa39f28-c530-4636-9cff-e1a84f4f1afa.PNG)


### Display the result of Opening
![2](https://user-images.githubusercontent.com/77089743/172055114-51d8d3cd-5a0d-4965-80a9-b1ba004d5857.PNG)



### Display the result of Closing
![3](https://user-images.githubusercontent.com/77089743/172055126-75c2bd20-d230-493f-84b5-1d05f05dc6d4.PNG)
 

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
