# Gun_Object_detection-Using-Yolov5

![68b0fbc4-6b2b-4d92-bbc9-b2e50514950c](https://user-images.githubusercontent.com/97952352/150191855-95ceb615-71f2-47a8-ac09-a77242b13cbe.jpg)


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
   
   ## Training instructions 

  1.Change directory to dev/yolov5/
  
  2.install dependencies using !pip install -r requirments.txt
  
  3.Create data.yaml file which containes train,val and test training images and labels  
  
      train : data/data/train/images
      
      val : data/data/val/images
      
      test : data/data/test/images
      
      nc : 1
      
      names: ["Gun"] 
   
  4.Check defaults parameters in train.py and specify any parameters you want to it be different.

  5.Run $ !python detect.py --weights runs/train/exp/weights/best.pt --img 416 --conf 0.12 --source /content/gun_test3.jpg
  


