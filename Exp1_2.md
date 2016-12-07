# Example 2 Basic Operations

## Script ([Notebook](https://github.com/chenchen2015/TensorFlowLearning/blob/master/Notebooks/Exp1_1.ipynb))
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
