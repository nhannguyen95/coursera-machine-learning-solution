# Quiz: Support Vector Machines

## Question 1:
Suppose you have trained an SVM classifier with a Gaussian kernel, and it learned the following decision boundary on the training set:

<img src="https://i.imgur.com/QmNLX4Q.jpg"/>

When you measure the SVM's performance on a cross validation set, it does poorly. Should you try increasing or decreasing C? Increasing or decreasing σ<sup>2</sup>?

### Answer
* It would be reasonable to try increasing C. It would also be reasonable to try decreasing σ<sup>2</sup>.

* **It would be reasonable to try decreasing C. It would also be reasonable to try increasing σ<sup>2</sup>.**

* It would be reasonable to try increasing C. It would also be reasonable to try increasing σ<sup>2</sup>.

* It would be reasonable to try decreasing C. It would also be reasonable to try decreasing σ<sup>2</sup>.

_This algorithm is suffering from high variance_

---

## Question 2:
The formula for the Gaussian kernel is given by <a href="https://www.codecogs.com/eqnedit.php?latex=\text{similarity}(x,l^{(1)})&space;=&space;\exp{(-\frac{||x-l^{(1)}||^2}{2\sigma^2})}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\text{similarity}(x,l^{(1)})&space;=&space;\exp{(-\frac{||x-l^{(1)}||^2}{2\sigma^2})}" title="\text{similarity}(x,l^{(1)}) = \exp{(-\frac{||x-l^{(1)}||^2}{2\sigma^2})}" /></a>.

The figure below shows a plot of f<sub>1</sub>=similarity(x,l<sup>(1)</sup>) when σ<sup>2</sup>=1.

<img src="https://i.imgur.com/kYhvQ6s.jpg"/>

Which of the following is a plot of f<sub>1</sub> when σ<sup>2</sup>=0.25?

### Answer:

* A

<img src="https://i.imgur.com/cjgtw47.jpg"/>

* B

<img src="https://i.imgur.com/YJlnp8n.jpg"/>

* C

<img src="https://i.imgur.com/svLa7Il.jpg"/>

* **D**

<img src="https://i.imgur.com/xGnxYA6.jpg"/>

---

## Question 3:
The SVM solves

<a href="https://www.codecogs.com/eqnedit.php?latex=\min_\theta&space;\space&space;C&space;\sum_{i=1}^m&space;y^{(i)}&space;\text{cost}_1(\theta^Tx^{(i)})&space;&plus;&space;(1-y^{(i)})&space;\text{cost}_0(\theta^Tx^{(i)})&space;&plus;&space;\sum_{j=1}^n&space;\theta_j^2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\min_\theta&space;\space&space;C&space;\sum_{i=1}^m&space;y^{(i)}&space;\text{cost}_1(\theta^Tx^{(i)})&space;&plus;&space;(1-y^{(i)})&space;\text{cost}_0(\theta^Tx^{(i)})&space;&plus;&space;\sum_{j=1}^n&space;\theta_j^2" title="\min_\theta \space C \sum_{i=1}^m y^{(i)} \text{cost}_1(\theta^Tx^{(i)}) + (1-y^{(i)}) \text{cost}_0(\theta^Tx^{(i)}) + \sum_{j=1}^n \theta_j^2" /></a>

where the functions cost<sub>0</sub>(z) and cost<sub>1</sub>(z) look like this:

<img src="https://i.imgur.com/Mit9Ug3.jpg"/>

The first term in the objective is:

<a href="https://www.codecogs.com/eqnedit.php?latex=C&space;\sum_{i=1}^m&space;y^{(i)}&space;\text{cost}_1(\theta^Tx^{(i)})&space;&plus;&space;(1-y^{(i)})&space;\text{cost}_0(\theta^Tx^{(i)})." target="_blank"><img src="https://latex.codecogs.com/gif.latex?C&space;\sum_{i=1}^m&space;y^{(i)}&space;\text{cost}_1(\theta^Tx^{(i)})&space;&plus;&space;(1-y^{(i)})&space;\text{cost}_0(\theta^Tx^{(i)})." title="C \sum_{i=1}^m y^{(i)} \text{cost}_1(\theta^Tx^{(i)}) + (1-y^{(i)}) \text{cost}_0(\theta^Tx^{(i)})." /></a>

This first term will be zero if two of the following four conditions hold true. Which are the two conditions that would guarantee that this term equals zero?

### Answer
* **For every example with y<sup>(i)</sup>=1, we have that θ<sup>T</sup>x<sup>(i)</sup> ≥ 1.**

* **For every example with y<sup>(i)</sup>=0, we have that θ<sup>T</sup>x<sup>(i)</sup> ≤ −1.**

* For every example with y<sup>(i)</sup>=1, we have that θ<sup>T</sup>x<sup>(i)</sup> ≥ 0.

* For every example with y<sup>(i)</sup>=0, we have that θ<sup>T</sup>x<sup>(i)</sup> ≤ 0.

---

## Question 4:
Suppose you have a dataset with n = 10 features and m = 5000 examples.

After training your logistic regression classifier with gradient descent, you find that it has underfit the training set and does not achieve the desired performance on the training or cross validation sets.

Which of the following might be promising steps to take? Check all that apply.

### Answer:
* Increase the regularization parameter λ.

* **Use an SVM with a Gaussian Kernel.**

* Use an SVM with a linear kernel, without introducing new features.

* **Create / add new polynomial features.**

---

## Question 5:
Which of the following statements are true? Check all that apply.

### Answer:
* If the data are linearly separable, an SVM using a linear kernel will return the same parameters θ regardless of the chosen value of C (i.e., the resulting value of θ does not depend on C).**

* **The maximum value of the Gaussian kernel (i.e., sim(x,l(1))) is 1.**

* Suppose you are using SVMs to do multi-class classification and would like to use the one-vs-all approach. If you have K different classes, you will train K - 1 different SVMs.

* **It is important to perform feature normalization before using the Gaussian kernel.**
