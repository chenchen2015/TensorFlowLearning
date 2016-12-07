# Example 2 Basic Operations ([Notebook](https://github.com/chenchen2015/TensorFlowLearning/blob/master/Notebooks/Exp1_1.ipynb))
In this example I tried to go through some of the basic operations in TensorFlow including:
- Defining variables and do some basic math with them
- Print the result using Python 3 style print function
Note that all the code are tested and meant for **Python 3.5.2**.:
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
