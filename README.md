# Gun_Object_detection-Using-Yolov5

![gun_test3](https://user-images.githubusercontent.com/97952352/150189058-bbffd6ad-6dc9-4178-bd5f-e60e4e6d87a0.jpg)

### Table of contents
* [Introduction](#introduction)
* [Problem Statement](#problem-statement)
* [Data Source](#data-source)
* [Technologies](#technologies)
* [Type of Data](#type-of-data)
* [Data Pre-processing](#data-pre-processing)
* [Algorithms Implemented](#algorithms-implemented)
* [Steps Involved](#steps-involved)
* [Evaluation Metrics](#evaluation-metrics)
* [Results and Conclusion](#results-and-conclusion)

* Introduction:

    Detect guns in photos and in videos using Yolov5

* Data Source:

   https://www.kaggle.com/issaisasank/guns-object-detection
 
 * Data Pre-processing:
   1) Removed the images which don't have annotations
   2) Converted annotations into standard yolo format
   Training data
   In current dataset contains 330 training images and trained with 512*512 dimensions 

 Train Dataset | Validation dataset| Test | Epochs|
| --- | --- |  --- |--- |
| 330| 30| 30 |50 |
   
  * Algorithms Implemented:
       yolov5
       https://github.com/ultralytics/yolov5
   
  


