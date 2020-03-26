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


 
