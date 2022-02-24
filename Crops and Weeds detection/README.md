
In this repository, crops and weeds are recognized and localized using [YOLOv5](https://github.com/ultralytics/yolov5) and [Faster-RCNN](https://arxiv.org/abs/1506.01497). The Faster-RCNN model was slow to run on my computer so I ran it for less epochs than YOLOv5. YOLOv5 is a single stage detector, while Faster-RCNN is heavy and requires more computational budget to train. In this project, I collected a labeled dataset from [Kaggle](https://www.kaggle.com/ravirajsinh45/crop-and-weed-detection-data-with-bounding-boxes).
The dataset has been reviewed to see for any missing information or for removing undesired images.

The dataset has been uploaded to [Roboflow](https://www.kaggle.com/ravirajsinh45/crop-and-weed-detection-data-with-bounding-boxes) annoatation tool to convert it to YOLOV5 format for YOLO and TF record format for Faster RCNN, and to preprocess and augment the dataset. The following images demonstrates labeled iamges.

![gtruth](https://user-images.githubusercontent.com/61932757/154662096-a08c3ca8-474c-4516-bf59-8602565bd022.png)

After converting to YoloV5 format and TF record format for Faster-RCNN the model has been trained for 70 epochs. Following are some of the images I obtained on the test set after training YOLOV5 on the dataset.

![d2](https://user-images.githubusercontent.com/61932757/154662430-1f96ed36-0e21-435c-975f-f3efab364a02.png) ![d11](https://user-images.githubusercontent.com/61932757/154662503-b03731e0-df5c-4a89-915e-5395343c2775.png)

results can be seen in the following plot.

![result](https://user-images.githubusercontent.com/61932757/154662724-73e69e16-986d-4b92-937b-8f8f98515d8f.png)

As far Faster-RCNN, it was computationally heavy, and takes more time to train. I had limited computational budget, so I trained it for 30 epochs. The detect results can be seen in the following images.

![detection5](https://user-images.githubusercontent.com/61932757/154663047-e6a28300-a03c-4bda-b2d4-3bb65ebc30a9.jpg) ![detection2](https://user-images.githubusercontent.com/61932757/154663084-148a8500-39d6-4e8d-aace-b0d5608256c6.jpg)

In the future, I would like to acquire maize crops and weeds dataset for real-time detection on raspberry pi.
