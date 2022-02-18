Object detection is very important for many applications, where recognizing and localizing an object is necessary. In this repository, sign language detection has been implemented using [MobileNet](http://download.tensorflow.org/models/object_detection/tf2/20200711/ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8.tar.gz). The purpose of this repository to detect four classes mainly ThumbsUp, ThumbsDown, ThankYou, and LiveLong, and depoly it in an android device like a Mobile Phone in this case [OPPOA1K](https://www.gsmarena.com/oppo_a1k-9673.php). The dataset has been acquired using webcam and labeld using [Labelimg](https://github.com/tzutalin/labelImg). Annotations were in xml format, therefore, to train MobileNet, it should be converted to TF record format. The dataset has been converted in TF record format and confiuration file of MobileNet has been edited to add 4 classes, to add paths of our dataset, and to edit some hyperparameters. TensorFlow's object detection API has been in this project.

The model has been trained for 2000 iterations. Some results images are shown below.

![thankyou_detection](https://user-images.githubusercontent.com/61932757/154614060-d8e9b802-5213-432c-b38a-fcd404af6091.png) ![Thumbs_down](https://user-images.githubusercontent.com/61932757/154614100-ffba6a59-0024-4d51-a623-b879b4f4428f.png)

However, The model confuses LiveLong with ThumbsUp because of Thumb position.

![LiveLong](https://user-images.githubusercontent.com/61932757/154614197-d25608ec-4e99-4bbe-bb23-37a2393e7755.png)

And Model incorrectly labeled an image, when there was no object in it.

![Thumbs_up](https://user-images.githubusercontent.com/61932757/154614267-1168da32-4a4c-4c28-be41-754d57294228.png)

From the above results, it is clear that, more diverse data needs to be acquired and to train the model for longer. Some data augmentation options could helpful. This model could be customized to your own projects, please follow the steps to train an object detection model for your own applications.



