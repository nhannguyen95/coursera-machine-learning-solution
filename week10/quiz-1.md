# Quiz: Large Scale Machine Learning

## Question 1
Suppose you are training a logistic regression classifier using stochastic gradient descent. You find that the cost (say, cost(θ,(x<sup>(i)</sup>,y<sup>(i)</sup>)), averaged over the last 500 examples), plotted as a function of the number of iterations, is slowly increasing over time. Which of the following changes are likely to help?

### Answer
* **Try halving (decreasing) the learning rate α, and see if that causes the cost to now consistently go down; and if not, keep halving it until it does.**

* Use fewer examples from your training set.

* This is not possible with stochastic gradient descent, as it is guaranteed to converge to the optimal parameters θ.

* Try averaging the cost over a smaller number of examples (say 250 examples instead of 500) in the plot.

---

## Question 2
Which of the following statements about stochastic gradient descent are true? Check all that apply.

### Answer
* In order to make sure stochastic gradient descent is converging, we typically compute J<sub>train</sub>(θ) after each iteration (and plot it) in order to make sure that the cost function is generally decreasing.

* Suppose you are using stochastic gradient descent to train a linear regression classifier. The cost function J(θ) is guaranteed to decrease after every iteration of the stochastic gradient descent algorithm.

* **Before running stochastic gradient descent, you should randomly shuffle (reorder) the training set.**

* **You can use the method of numerical gradient checking to verify that your stochastic gradient descent implementation is bug-free. (One step of stochastic gradient descent computes the partial derivative of cost(θ,(x<sup>(i)</sup>,y<sup>(i)</sup>)).)**

---

## Question 3
Which of the following statements about online learning are true? Check all that apply.

### Answer
* **One of the advantages of online learning is that if the function we're modeling changes over time (such as if we are modeling the probability of users clicking on different URLs, and user tastes/preferences are changing over time), the online learning algorithm will automatically adapt to these changes.**

* When using online learning, you must save every new training example you get, as you will need to reuse past examples to re-train the model even after you get new training examples in the future.

* **Online learning algorithms are usually best suited to problems were we have a continuous/non-stop stream of data that we want to learn from.**

* Online learning algorithms are most appropriate when we have a fixed training set of size m that we want to train on.

---

## Question 4
Assuming that you have a very large training set, which of the following algorithms do you think can be parallelized using map-reduce and splitting the training set across different machines? Check all that apply.

### Answer
* Logistic regression trained using stochastic gradient descent.

* **Logistic regression trained using batch gradient descent.**

* Linear regression trained using stochastic gradient descent.

* **Computing the average of all the features in your training set μ=1m∑mi=1x(i) (say in order to perform mean normalization).**

---
## Question 5
Which of the following statements about map-reduce are true? Check all that apply.

### Answer
* **When using map-reduce with gradient descent, we usually use a single machine that accumulates the gradients from each of the map-reduce machines, in order to compute the parameter update for that iteration.**

* **Because of network latency and other overhead associated with map-reduce, if we run map-reduce using N computers, we might get less than an N-fold speedup compared to using 1 computer.**

* **If you have only 1 computer with 1 computing core, then map-reduce is unlikely to help.**

* Linear regression and logistic regression can be parallelized using map-reduce, but not neural network training.
