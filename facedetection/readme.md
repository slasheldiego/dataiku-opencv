# Face detection using CascadeClassifier

OpenCV is a set of tool where we can find efficient implementation facing common challenges inside computer vision area like face detection in images and videos.

Let's check how we can implement an easy face detector using a well-know CascadeClassifier in OpenCV. This classifier is based on Viola & Jones work which it is used a kind of vector feature called "Haar features" and a boosting algorithm called Adaboost which is a classifier composed by weak classifiers.

As we know now how load an image we can use it in a face detection classifier to try to detect some faces in the photo. To do that we need to import cv2 library and create a CascadeClassifier function from cv2 library.

```python
%pylab inline
 
import dataiku
from dataiku import pandasutils as pdu
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
import cv2
 
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + "haarcascade_frontalface_Default.xml")
```

As you can see CascadeClassifier function receive a parameter which is a file system path where a XML file  is located. We will talk about this XML in short but something you need to know is that this XML reside in the Dataiku server where we have our workspace. In this case we are in Dataiku Design Node where we can design, train and test our first model versions.

Now, turn back again in to the XML file. CascadeClassifier need a knowledge built training a Adaboost algorithm. However, there are previous pre-trained models available based on Haar Features. You can see more pre-trained models in this github project here. The pre-trained model are in XML format contained the output of the hyper-parameters and other metadata information that CascadeClassifier needs to create a classifier object. 

<img src="images/haar_features.png?raw=true" width="600" height="350" alt="Dataset section"/>

