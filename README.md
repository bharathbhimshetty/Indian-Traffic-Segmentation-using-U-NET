# Indian-Traffic-Segmentation-using-U-NET

* The dataset is partially based on https://idd.insaan.iiit.ac.in/
* The dataset we have used has around 4008 images of HD resolution (1080 * 1980)
which are the pictures taken on various kinds of places mostly Traffic on roads in and around Hyderabad and Bengaluru.
* We have the coordinates and through which we have created polygons wherein these polygons are drawn onto a RGB image canvas but in 0 axis and hence we get a channels of 40, as we have 40 different classes.
* After the polygons are drawn we get y labelled images which are masked images of original and we use these in training to predict.
* As the classes are 40 and we need to color code them between 0-255 and we squeeze these classes further to 21 so that results during prediction shall be better.
* We havent normalized the images and also we havent used any image augumentation techniques too as the predictions are not good but we have resized the images t0 (512, 512) and we can  resize in multiples of 32 also as the U-NET accepts these image shapes only.
* We have used U-NET architechture as the shape of input image is same as shape of the output image.
* In U-NET we have used "resnet-34" as base model, as this gives us good results among other base models such as "resnet-50" or "VGG-16".
* We have used dice loss as loss and Adam as optimizer with default learning rates as the results are pretty good.
* This dice loss is a cce loss which is categorical cross entropy loss as this is multiclass classification.
* We train the model with two metrics such as F1 score and as well as IOU score, which is intersection over union also called as jaccared similarity.
* We ran for 30 epochs in all and the model was saved.
* The predictions are better as the loss is around 0.26 and val iou score is around 61.5 and train iou score is around 68.5.
* The model seems slightly overfit, but nonetheless the results are good as can viszualize.
