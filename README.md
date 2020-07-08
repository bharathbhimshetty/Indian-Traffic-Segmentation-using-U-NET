# Indian-Traffic-Segmentation-using-U-NE

This project is intended for autonomous navigation of car and the images are segmented manually using OpenCV polygons coordinates and the the images are 1 channel y labels and we use U-Net Resnet-34 as base model, to predict the masks and we have 40 classes.
The dataset is partially based on https://idd.insaan.iiit.ac.in/
We have used dice loss which is categorical cross entropy loss as this is multiclass classification.
We train the model with two metrics such as F1 score and as well as IOU score, which is intersection over
union also called as jaccared similarity.
