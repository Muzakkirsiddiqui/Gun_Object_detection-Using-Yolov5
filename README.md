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
       
   
       
  * Evaluation Metrics:

    ### Current performance metrics v0.0

 
Following are the results on test data with confidence score>0.4

| _Per class_ |precision    |recall  |map@0.5  |map@0.95 | total no of images |
| --- | --- | --- | --- | --- | ---
| 'Gun' | 0.79 | 0.75 | 0.76 |0.352 | 50 |
  
  ![Capture12](https://user-images.githubusercontent.com/97952352/150192992-a1318914-75ba-4a73-a683-ad3e2a87012e.JPG)
   
   
   
   
   
   
   
   
   
   
   
   
   ##DEMO:
     
   
https://user-images.githubusercontent.com/97952352/150192206-06057799-3752-439f-8861-04aed610382b.mp4
  


