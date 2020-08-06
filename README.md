# Environment Set-Up

Make sure to run the code with TensorFlow 1.15 and Keras 2.3.1 to avoid any incompatible issues. 

The code was being runned using the Google Colab (GPU runtime). 

If you tend to run it in your own computer, make sure you have enough GPU and install the dependencies as shown in the documentation at my github link 
https://github.com/JJLim99/Implementation-of-TensorFlow-GPU-CUDA-in-Windows.git


# ObjectDetection-Keras_MaskRCNN

Please take note to the following changes to prevent errors. (Can refer to the uploaded mrcnn files)

For model.py
--> Change the code at line 2199 to self.keras_model.add_metric(loss, name) 

For utils.py
--> Change the code at line 866 to shift = np.array([0, 0, 1., 1.])

For config.py
--> Try to lower the value for both of the DETECTION_MIN_CONFIDENCE and DETECTION_NMS_THRESHOLD if there is no bounding boxes at the ouput
