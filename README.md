show all kinds of AI demo

1.fit-2d-data.html
https://www.tensorflow.org/js/tutorials/training/linear_regression

2.model.save('model_py/model.h5')
This saves our model as a HDF5 file — ready to be translated into the TensorFlow.js web format.
To convert the model, we first need to pip install tensorflowjs. Once installed, we run the tensorflowjs_converter from the command line (Command Prompt, Terminal, Bash, etc.).
Open the command line and navigate to our project folder (cd <directory_path> on Windows). Then run the converter by typing:
tensorflowjs_converter \
     --input_format=keras \
     model_py/model.h5 \
     model_js
     Here, we are telling tensorflowjs_converter to expect the keras model format. We then specify the model path model_py/model.h5. Lastly, we tell the converter to save the converted model in the model_js directory.
If we navigate to model_js we will find the following:
That .json file is our web-enabled model, ready for use in JavaScript.
