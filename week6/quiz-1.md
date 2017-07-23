# Quiz: Advice for Applying Machine Learning

## Question 1
You train a learning algorithm, and find that it has unacceptably high error on the test set. You plot the learning curve, and obtain the figure below. Is the algorithm suffering from high bias, high variance, or neither?

<img width="400" src="http://i.imgur.com/FZpJL1X.png">

### Answer
* Neither
* **High bias**
* High variance

---

## Question 2
Suppose you have implemented regularized logistic regression to classify what object is in an image (i.e., to do object recognition). However, when you test your hypothesis on a new set of images, you find that it makes unacceptably large errors with its predictions on the new images. However, your hypothesis performs well (has low error) on the training set. Which of the following are promising steps to take? Check all that apply.

### Answer
*The algorithm is suffering from high variance.*

* Try decreasing the regularization parameter λ.
* **Try using a smaller set of features.**
* **Try increasing the regularization parameter λ.**
* Try evaluating the hypothesis on a cross validation set rather than the test set.

---

## Question 3
Suppose you have implemented regularized logistic regression to predict what items customers will purchase on a web shopping site. However, when you test your hypothesis on a new set of customers, you find that it makes unacceptably large errors in its predictions. Furthermore, the hypothesis performs poorly on the training set. Which of the following might be promising steps to take? Check all that apply.

### Answer
*The algorithm is suffering from high bias.*

* **Try adding polynomial features.**
* **Try decreasing the regularization parameter λ.**
* Try evaluating the hypothesis on a cross validation set rather than the test set.
* Use fewer training examples.
---

## Question 4
Which of the following statements are true? Check all that apply.

### Answer
* **Suppose you are training a regularized linear regression model. The recommended way to choose what value of regularization parameter λ to use is to choose the value of λ which gives the lowest cross validation error.**

* Suppose you are training a regularized linear regression model. The recommended way to choose what value of regularization parameter λ to use is to choose the value of λ which gives the lowest test set error.

* **The performance of a learning algorithm on the training set will typically be better than its performance on the test set.**

* Suppose you are training a regularized linear regression model.The recommended way to choose what value of regularization parameter λ to use is to choose the value of λ which gives the lowest training set error.

---
## Question 5
Which of the following statements are true? Check all that apply.

### Answer
* **A model with more parameters is more prone to overfitting and typically has higher variance.**

* If the training and test errors are about the same, adding more features will not help improve the results.

* **If a learning algorithm is suffering from high bias, only adding more training examples may not improve the test error significantly.**

* **If a learning algorithm is suffering from high variance, adding more training examples is likely to improve the test error.**
