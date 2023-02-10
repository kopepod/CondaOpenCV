# CondaOpenCV

This repository is meant to run opencv using the conda envirorment

## Conda

Create the envirorment. Alternatively a _yml_ file can be used.

```bash
conda create --name opencvenv
```

Activate the environment

```bash
conda activate opencvenv
```

## PIP

Install packages. 

```bash
pip install opencv-python
```

## Python

```python
import numpy as np
import cv2 as cv
img = cv.imread('home.jpg')
gray= cv.cvtColor(img,cv.COLOR_BGR2GRAY)
sift = cv.SIFT_create()
kp = sift.detect(gray,None)
img=cv.drawKeypoints(gray,kp,img)
cv.imwrite('sift_keypoints.jpg',img)
```


