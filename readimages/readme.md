# Read an image from the Dataiku managed folder

We need some libraries in order to be available to access to an image from Dataiku managed folder.

```python
  %pylab inline

  import dataiku
  from dataiku import pandasutils as pdu
  import pandas as pd
  import numpy as np
  import cv2
  import matplotlib.pyplot as plt

  %matplotlib inline
```

Define a Folder structure 

```python
mydataset = dataiku.Folder("ImagesTest")
```

Finally, go through all the images inside the folder and plot each one

```python
i = 321
for img in [item["fullPath"] for item in mydataset.get_path_details()["children"]]:
    print(img)
    with mydataset.get_download_stream(path=img) as stream:
        nparr = np.fromstring(stream.read(), np.uint8)
        img_np = cv2.imdecode(nparr, cv2.IMREAD_COLOR)
        plt.subplot(i),plt.imshow(img_np, cmap='gray')
        i = i + 1
        stream.close()
        if i == 327:
            break
 
plt.show()
```

<img src="images/dataiku-opencv-framework1.png?raw=true" width="600" height="360" alt="Dataset section"/>
