# Indian-Traffic-Segmentation-using-U-NET

The x label is 3 channel image and y labels have 40 classes segmented for each gray scale image.

The dataset is partially based on https://idd.insaan.iiit.ac.in/

We have used dice loss which is categorical cross entropy loss as this is multiclass classification.

We train the model with two metrics such as F1 score and as well as IOU score, which is intersection over union also called as jaccared similarity.
