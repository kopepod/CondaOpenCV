# CondaOpenCV

This repository is meant to run opencv using the conda environment

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
import cv2
import os

os.system("wget https://raw.githubusercontent.com/kopepod/CondaOpenCV/main/church.jpg")

img = cv2.imread('church.jpg')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
sift = cv2.SIFT_create()
kp = sift.detect(gray, None)
img = cv2.drawKeypoints(gray, kp, img)
cv2.imwrite('output_sift_kp.jpg', img)

```

<img src="https://github.com/kopepod/DemographicFaceSynthesis/blob/main/FIGS/GFL.png" width="256" height="256" />

![Church](https://raw.githubusercontent.com/kopepod/CondaOpenCV/main/church.jpg)


