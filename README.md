# Gun_Object_detection-Using-Yolov5

![68b0fbc4-6b2b-4d92-bbc9-b2e50514950c](https://user-images.githubusercontent.com/97952352/150196541-69fe78bb-093c-4cad-8775-f4e79b98b92b.jpg)


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
   In current dataset contains 330 training images and trained with 416*416 dimensions 
   
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

  5.Run $ !python train.py --img 416 --batch 16 --epochs 500 --data {dataset.location}/data.yaml --weights yolov5s.pt --cache


 Train Dataset | Validation dataset| Test | Epochs|
  | --- | --- |  --- |--- |
  | 535| 50| 26 |150 |
  

   
  * Algorithms Implemented:
       yolov5
       
       https://github.com/ultralytics/yolov5
       
   
       
  * Evaluation Metrics:

### Current performance metrics:


Following are the results on test data with confidence score>0.4

| _Per class_ |precision    |recall  |map@0.5  |map@0.95 | total no of images |
| --- | --- | --- | --- | --- | ---
| 'Gun' | 0.79 | 0.75 | 0.76 |0.352 | 50 |
 
 ![Capture](https://user-images.githubusercontent.com/97952352/150194092-740f630e-5af0-430b-a20b-d4df38c822e3.JPG)
 
 
 ## Inference instructions 

  1.Change directory to dev/yolov5/
  
  2.Mention the required parameters in detect.py with following details along with best.pt params file which is there in model_params folder 
  
      weights='best.pt', source='images', img_size=416, conf_thres=0.12, iou_thres=0.2, device='', view_img=False, save_txt=False, save_conf=False,  classes=None,   agnostic_nms=False, augment=False, update=False, project='runs/detect', name='exp', exist_ok=False
      
  3.Run the following command 
  
      !python detect.py --weights runs/train/exp/weights/best.pt --img 416 --conf 0.12 --source /content/gun_test3.jpg
   
   
   
   
   
   
   
   
### Prediction results
_Sample result:_
     
   
https://user-images.githubusercontent.com/97952352/150192206-06057799-3752-439f-8861-04aed610382b.mp4

![download (3)](https://user-images.githubusercontent.com/97952352/150195170-74a8d76d-13c3-4653-8828-1443630ab98a.jpg)
  


