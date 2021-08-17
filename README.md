# SPSGP-4521-Rice-Crop-Disease-Detection-using-YoLO
Rice Crop Disease Detection using YoLO

In this i am using yolov3 model.

YoLO (you only look once), an algorithm that is used for object detection in real time. It predicts classes and bounding boxes for the testing images in one run of the algorithm.

YOLO-based Convolutional Neural Network family of models for object detection and the most recent variation called YOLOv3.

YoLOv3 has a deeper architecture of feature extractor called Darknet-53. A 53-layer trained on Imagenet and for the task of detection 53 more layers has been stacked onto it, which gives us a 106 layer fully convolutional underlying architecture for yolov3.

Pre-Requisites:
i.   Anaconda (python IDE)
ii.  Microsoft's Visual Object Tagging Tool (VoTT)
iii. Python packages

Python Packages:
1. Tensorflow
2. keras
3. opencv
4. Pillow

VoTT is used for annotating and labelling the images.
Create a project name as "Annotations". Give the Source Images/Training Images path as source for the images and as the destination path. A new folder will be created with a given name at the export settings. Export it as CSV

After creating the dataset

Steps:
1. Open your anaconda command prompt and run "python Convert_to_YOLO_format.py" - this will create the data_classes.txt and data_train.txt files
2. Next run "python Download_and_Convert_YOLO_weights.py" 
3. Now train your yolo model "python Train_YOLO.py" - this process may take few hours based on how many images you have given in the dataset
4. After Training, test your model "python Detector.py" - the output will be displayed and there will be a folder with "Test_Image_Detection_Results" which consists of output images with bounding boxes over the disease detected with its name and tag color.
