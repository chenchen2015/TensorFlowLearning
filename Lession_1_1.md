# TensorFlowLearning
Learning notes of TensorFlow package.

## TensorFlow Installation (Windows 10)
1. Install [Anaconda (v4.20 64bit, Python 3.5.2 used)](https://www.continuum.io/downloads)
2. Install [CUDA 8.0](https://developer.nvidia.com/cuda-downloads)
3. Install [cuDNN for CUDA 8.0](https://developer.nvidia.com/cudnn). After you downloaded the file, copy all the files to the CUDA installation directory (default is at *C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0*)
4. Install **TensorFlow** using *pip*
```bash
pip install tensorflow # CPU Version
```
```bash
pip install tensorflow-gpu # GPU Version
```
5. Once you successfully installed **TensorFlow** package, you can start testing it. If everything's fine, you should be able to run the HelloWorld script below:
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
