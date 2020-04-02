# TensorPC

This documentation is created to run the tensorflwo obejct detection n otebook provided by tensorflow locally in a jupyter notebook. 

## Virtual environment 
Reccomended to use a virtual envronment for installation 
In our cases anaconda was used as package installation tool. 

To set up the virtual envrionment a guide by Jeff Heaton was follwed. 

https://www.youtube.com/watch?v=RgO8BBNGB8w&t=609s  

This tutorial provided the tensorflow.yml file to cover most required installations for the virual environment. The YML file used for our specific setup is included in the main repository. 


## Dependencies
- Protobuf 3.0.0
- Python-tk
- Pillow 1.0
- lxml
- tf Slim (which is included in the "tensorflow/models/research/" checkout)
- Jupyter notebook
- Matplotlib
- Tensorflow (>=1.12.0)
- Cython
- contextlib2
- cocoapi


## Additional Installations 
Running the jupyter notebook didnt work, regardless of all dependencies being isntalled correctly. 
Aditionally this post was helpful to install pycocotools: https://www.kaggle.com/c/tgs-salt-identification-challenge/discussion/62381

1. Install Visual C++ 2015 Build Tools from https://go.microsoft.com/fwlink/?LinkId=691126 with default selection.
2. Go to C:\Program Files (x86)\Microsoft Visual C++ Build Tools and run vcbuildtools_msbuild.bat
3. In Anaconda, run

        pip install git+https://github.com/philferriere/cocoapi.git#egg=pycocotools^&subdirectory=PythonAPI


## Trouble shooting error messages 
"object_detection module not found"

It was required to install the object-detection-api 

To do this run the following command in the venv: 
        
        pip install tensorflow-object-detection-api

## Experiment 31.03.2020
upload a defined set of test images 

### Models 
test different models on the same test images
- ssd_mobilenet_v1_coco_2018_01_28 - original model in code, although it was the 2017 version
- ssd_inception_v2_coco_2018_01_28
- faster_rcnn_nas_coco_2018_01_28 - performance slow, but detection is good.
- faster_rcnn_inception_resnet_v2_atrous_lowproposals_coco_2018_01_28 - detected people well and ps4 controller as remote 
- faster_rcnn_inception_resnet_v2_atrous_oid_2018_01_28 - good detection boxes but no classification at all (N/A) 
- faster_rcnn_inception_resnet_v2_atrous_oid_v4_2018_12_12 - only one detection box in one image, the rest of the images was completely empty 
- faster_rcnn_resnet101_fgvc_2018_07_19 - no detection at all 
### Additional Test Images 
Because the modelsdetected some categories surprisingly often, we decided to find some test images of those categories that still would make sense in the WeUse context. 
- TV
- Remote
- Scissors
- Books 
- Bike 
- Pot & Pan 
- Laptop
- Bikepump
- Toaster
- Hairdryer

        
 
