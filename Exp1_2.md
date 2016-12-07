# Example 2 Basic Operations ([Notebook](https://github.com/chenchen2015/TensorFlowLearning/blob/master/Notebooks/Exp1_2.ipynb))
In this example I tried to go through some of the basic operations in TensorFlow including:
- Defining variables and do some basic math with them
- Print results using Python 3 style print function
- Basic matrix operations
- Placeholder functions

Note that all the code are tested and meant for **Python 3.5.2**
```python
# Import TensorFlow Module
import tensorflow as tf

## Example #1
## Basic Constant Variable Definition and Print Function

# Define some constants
a = tf.constant(3)
b = tf.constant(5)

# Do some basic math and print the result using the with...as... statement
# Note that since I am using Python 3.5.2 not 2.7, the usage of the print function is slightly different
with tf.Session() as sess:
    print('Python version used', ver)
    print("a = {0:1d}, b = {1:1d}".format(sess.run(a), sess.run(b)))
    print("a + b = {0:2d}".format(sess.run(a+b)))
    print("a * b = {0:2d}".format(sess.run(a*b)))
    
## Example #2
## Basic Operations with Placeholder function

# Initialize a, b as two integer placeholders (i.e. variables)
a = tf.placeholder(tf.int32, name="var_a")
b = tf.placeholder(tf.int32, name="var_b")

# Now you can define some arbitrary operations
opAdd = tf.add(a, b)
opSub = tf.sub(a, b)
opMul = tf.mul(a, b)

# Print the result (Note the difference with example #1)
with tf.Session() as sess:
    print(
        "a = {0}, b = {1}".format(
            sess.run(a, feed_dict={a: 3}), 
            sess.run(b, feed_dict={b: 5})))
    print("a + b = {0}".format(sess.run(opAdd, feed_dict={a: 3, b: 5})))
    print("a - b = {0}".format(sess.run(opSub, feed_dict={a: 3, b: 5})))
    print("a * b = {0}".format(sess.run(opMul, feed_dict={a: 3, b: 5})))

## Example #3
## Simple Matrix Operations

# Create two constant matrix with a dimension of 3x3
mat1 = tf.constant([[1., 2., 3.],
                    [4., 5., 6.],
                    [7., 8., 9.]])
mat2 = tf.constant([[9., 8., 7.],
                    [6., 5., 4.],
                    [3., 2., 1.]])

# Run some simple matrix operation
opAdd = mat1 + mat2;
opSub = mat1 - mat2;
opMul = tf.matmul(mat1, mat2)

# Print the results
with tf.Session() as sess:
    print("Addition: \n", sess.run(opAdd),"\n")
    print("Subtraction : \n", sess.run(opSub),"\n")
    print("Multiplication: \n", sess.run(opMul),"\n")
```
