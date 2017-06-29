# Quiz: Logistic Regression

## Question 1
Suppose that you have trained a logistic regression classifier, and it outputs on a new example x a prediction hθ(x) = 0.7. This means (check all that apply):

### Answer
* Our estimate for P(y=1|x;θ) is 0.3.
* Our estimate for P(y=0|x;θ) is 0.7.
* **Our estimate for P(y=0|x;θ) is 0.3.**
* **Our estimate for P(y=1|x;θ) is 0.7.**

---

## Question 2
Suppose you have the following training set, and fit a logistic regression classifier hθ(x)=g(θ0+θ1x1+θ2x2).

|x1|x2|y|
|-|-|-|
|1|0.5|0|
|1|1.5|0|
|2|1|1|
|3|1|0|

Which of the following are true? Check all that apply.

### Answer
* **Adding polynomial features (e.g., instead using hθ(x)=g(θ0+θ1x1+θ2x2+θ3x21+θ4x1x2+θ5x22) ) could increase how well we can fit the training data.**
* **At the optimal value of θ (e.g., found by fminunc), we will have J(θ)≥0.**
* Adding polynomial features (e.g., instead using hθ(x)=g(θ0+θ1x1+θ2x2+θ3x21+θ4x1x2+θ5x22) ) would increase J(θ) because we are now summing over more terms.
* If we train gradient descent for enough iterations, for some examples x<sup>(i)</sup> in the training set it is possible to obtain hθ(x(i))>1.

---

## Question 3

For logistic regression, the gradient is given by <a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial}{\partial&space;\theta_j}&space;J(\theta)&space;=&space;\frac{1}{m}\sum_{i=1}^m{&space;(h_\theta(x^{(i)})&space;-&space;y^{(i)})&space;x_j^{(i)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial}{\partial&space;\theta_j}&space;J(\theta)&space;=&space;\frac{1}{m}\sum_{i=1}^m{&space;(h_\theta(x^{(i)})&space;-&space;y^{(i)})&space;x_j^{(i)}}" title="\frac{\partial}{\partial \theta_j} J(\theta) = \frac{1}{m}\sum_{i=1}^m{ (h_\theta(x^{(i)}) - y^{(i)}) x_j^{(i)}}" /></a>. Which of these is a correct gradient descent update for logistic regression with a learning rate of α? Check all that apply.

### Answer
A and B
* <a href="https://www.codecogs.com/eqnedit.php?latex=\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;(h_\theta(x^{(i)})&space;-&space;y^{(i)})&space;x^{(i)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;(h_\theta(x^{(i)})&space;-&space;y^{(i)})&space;x^{(i)}}" title="\theta := \theta - \alpha \frac{1}{m} \sum_{i=1}^m{ (h_\theta(x^{(i)}) - y^{(i)}) x^{(i)}}" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\frac{1}{1&space;&plus;&space;e^{-\theta^T&space;x^{(i)}}}&space;-&space;y^{(i)}\right)&space;x^{(i)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\frac{1}{1&space;&plus;&space;e^{-\theta^T&space;x^{(i)}}}&space;-&space;y^{(i)}\right)&space;x^{(i)}}" title="\theta := \theta - \alpha \frac{1}{m} \sum_{i=1}^m{ \left(\frac{1}{1 + e^{-\theta^T x^{(i)}}} - y^{(i)}\right) x^{(i)}}" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\theta^T&space;x&space;-&space;y^{(i)}\right)&space;x^{(i)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\theta&space;:=&space;\theta&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\theta^T&space;x&space;-&space;y^{(i)}\right)&space;x^{(i)}}" title="\theta := \theta - \alpha \frac{1}{m} \sum_{i=1}^m{ \left(\theta^T x - y^{(i)}\right) x^{(i)}}" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\theta_j&space;:=&space;\theta_j&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\theta^T&space;x&space;-&space;y^{(i)}\right)&space;x_j^{(i)}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\theta_j&space;:=&space;\theta_j&space;-&space;\alpha&space;\frac{1}{m}&space;\sum_{i=1}^m{&space;\left(\theta^T&space;x&space;-&space;y^{(i)}\right)&space;x_j^{(i)}}" title="\theta_j := \theta_j - \alpha \frac{1}{m} \sum_{i=1}^m{ \left(\theta^T x - y^{(i)}\right) x_j^{(i)}}" /></a>

---

## Question 4
Which of the following statements are true? Check all that apply.

### Answer
A and D
* The sigmoid function <a href="https://www.codecogs.com/eqnedit.php?latex=g(z)&space;=&space;\frac{1}{1&space;&plus;&space;e^{-z}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g(z)&space;=&space;\frac{1}{1&space;&plus;&space;e^{-z}}" title="g(z) = \frac{1}{1 + e^{-z}}" /></a> is never greater than one (>1).
* For logistic regression, sometimes gradient descent will converge to a local minimum (and fail to find the global minimum). This is the reason we prefer more advanced optimization algorithms such as fminunc (conjugate gradient/BFGS/L-BFGS/etc).
* Linear regression always works well for classification if you classify by using a threshold on the prediction made by linear regression.
* The cost function J(θ) for logistic regression trained with m≥1 examples is always greater than or equal to zero.

---

## Question 5
Suppose you train a logistic classifier hθ(x)=g(θ0+θ1x1+θ2x2). Suppose θ0=−6,θ1=0,θ2=1. Which of the following figures represents the decision boundary found by your classifier?

### Answer
Decision boundary:

-6 + x<sub>2</sub> = 0

=> x<sub>2</sub> = 6

=> It's a line which is parallel with Ox (x<sub>1</sub>) and intersects with Oy (x<sub>2</sub>) at (0, 6).

y = 1 if -6 + x<sub>2</sub> >= 0, so x<sub>2</sub> >= 6

y = 0 if -6 + x<sub>2</sub> < 0, so x<sub>2</sub> < 6
