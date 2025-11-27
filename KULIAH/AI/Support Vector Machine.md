# Keywords
- Binary Classification
- Linear Separability
- Linear Classifier
- Hyperplane Classifier

# What & Why
Good performance in various applications like bioinformatics, text classification, etc.

**Binary Classification**
Given a training data ($x_{i},y_{i}$), with $x\in \mathbb{R}^d$ and $y\in{-1,1}$, learn a classifier function $f(x)$, such that if the value of $f(x) \geq{0}$, then $y=+1$, and other wise $y=-1$.

**Linear Separability**
A linearly separable data is a data in which when plotted, the values of two classes can be clearly and completely separated using a **straigt line**. The larger the margin of the line is, the better.

**Linear Classifier**
The line that separates linearly separable data. A linear classifier has the form:
$$f(x)=w^Tx+b$$
In 2D the discriminant is a line: 
- $w$ - a normal to the line (know as the weight vector)
- $b$ - bias
In 3D, the discriminant is a plane, and in nD it is a hyperplane.

For a k-NN classifier, it is necessary to carry the training data
For a linear classifier, the training data is used to learn $w$, and then discarded. Only $w$ is needed for classifying new data.

**Perceptron's Weakness**
Biggest weakness of perceptron is that it will not find the same hyperplane every time.

**SVM Objective**
Find the optimal separating hyperplane which maximizes the margin of the training data.
Uses *quadratic optimization* to avoid local minimum that is present in *Neural Networks*.

**Hyperplane Classifier**
The size of a margin is equal to $\frac{2}{\lvert \lvert w \rvert \rvert}$

**Vector Direction**
![[Pasted image 20251127150502.png|600]]

# SVM for Linearly Separable Data
Two classes can be separated by a pair of linear separator. **Support Vectors** are Vectors in training data that *supports* the separators.

Larger margins has better generalization, data close to the separator represents uncertainty in classification.