# Lesson 1 TensorFlow Setup and Basic Operations

## TensorFlow Installation (Windows 10)
1. Install [Anaconda (v4.20 64bit, Python 3.5.2 used)](https://www.continuum.io/downloads)
2. Install [CUDA 8.0](https://developer.nvidia.com/cuda-downloads)
3. Install [cuDNN for CUDA 8.0](https://developer.nvidia.com/cudnn). After you downloaded the file, copy all the files to the CUDA installation directory (default is at *C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0*, this will make sure that cuDNN library is under Windows's PATH variable and can be found by console)
4. Now, open a new console (CMD or PowerShell) and install **TensorFlow** using *pip*. Please install both the CPU **AND** GPU version.
```bash
pip install tensorflow # CPU Version

pip install tensorflow-gpu # GPU Version
```

## Hello World Script ([Notebook](https://github.com/chenchen2015/TensorFlowLearning/blob/master/Notebooks/Exp1_1.ipynb))
Once you successfully installed **TensorFlow** package, you can start testing it. If everything's fine, you should be able to run the HelloWorld script below:
```python
# Import TensorFlow Library
import tensorflow as tf

# Create a String Constant Named "helloworldVar"
helloworld = tf.constant('HelloWorld from Chen!!', name="helloworldVar") 

# Print the Type of the Variable
print(helloworld)

# Start a TensorFlow Session
sess = tf.Session()

# Run the Session and Print the Result
print(sess.run(helloworld))
```
