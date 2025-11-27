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
The size of a margin is equal to $\frac{2}{\lvert \lvert w \rvert \rvert}$, which means to optimize hyperplane we need to minimize $\lvert \lvert w \rvert \rvert$ while keeping concistencies with the data.

**Vector Direction**
![[Pasted image 20251127150502.png|600]]

# SVM for Linearly Separable Data
## Support Vectors
Two classes can be separated by a pair of linear separator. **Support Vectors** are Vectors in training data that *supports* the separators.

More specifically, support vectors are *data points* that lie closest to the decision surface (or hyperplane). They are the data points that are most difficult to classify, and have direct bearing on the optimum position of the separator.

Larger margins has better generalization, data close to the separator represents uncertainty in classification.

**Support Vectors** Satisfies $$\vert\vec{w}\cdot \vec{x_{i}} +b\vert=1$$ where $x_{i}$ is the i-th  support vector
And all data points in training data with labels "+" and "-" satisfies 
$$y_{i}(\vec{w}\cdot \vec{x_{i}} +b)\geq1$$
As stated in [[Support Vector Machine#What & Why|Hyperplane Classifier]], we need to minimize:
$$V(\vec{w}, b)=\frac{1}{2}\vec{w}\cdot \vec{w}$$
## Lagrangian Formula
An easier way to calculate the search for the optimal hyperplane.
![[Pasted image 20251127164837.png|500]]

>[!important]
>The magnitude of $\alpha_{i}$ indicates weight, or inflience of the data point $x_{i}$

But why do we only take non-zero alphas?
![[Pasted image 20251127172412.png]]

**Lagrangian Dual Problem**
![[Pasted image 20251127165357.png|400]]

To further simplify it (removed the dependence on $w$ and $b$)
![[Pasted image 20251127170243.png |400]]

## Quadratic Optimization Problem
![[Pasted image 20251127170820.png|400]]

**Quadratic Programming**
QP is the problem of optimizing a quadratic objective funciton and is one of the simplests form of non-linear programming.
![[Pasted image 20251127172639.png|300]]

The objective function can contain bilinear or up to second order polynomial terms, and the constraints are linear and can be both equalities and inequalities.

