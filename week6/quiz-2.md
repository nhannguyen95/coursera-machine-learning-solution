# Quiz: Machine Learning System Design

## Question 1

You are working on a spam classification system using regularized logistic regression. "Spam" is a positive class (y = 1) and "not spam" is the negative class (y = 0). You have trained your classifier and there are m = 1000 examples in the cross-validation set. The chart of predicted class vs. actual class is:

||Actual Class: 1|Actual Class: 0|
|-|-|-|
|Predicted Class: 1|85|890|
|Predicted Class: 0|15|10|

What is the classifier's precision (as a value from 0 to 1)?

Enter your answer in the box below. If necessary, provide at least two values after the decimal point.

### Answer

Precision = 85 / (85 + 890) = 0.09

---

## Question 2

Suppose a massive dataset is available for training a learning algorithm. Training on a lot of data is likely to give good performance when two of the following conditions hold true.

### Answer
* We train a model that does not use regularization.
* **The features x contain sufficient information to predict y accurately. (For example, one way to verify this is if a human expert on the domain can confidently predict y when given only x).**
* We train a learning algorithm with a small number of parameters (that is thus unlikely to overfit).
* **We train a learning algorithm with a large number of parameters (that is able to learn/represent fairly complex functions).**

---

## Question 3

Suppose you have trained a logistic regression classifier which is outputing h<sub>θ</sub>(x).Currently, you predict 1 if h<sub>θ</sub>(x) ≥ threshold, and predict 0 if h<sub>θ</sub>(x) < threshold, where currently the threshold is set to 0.5.

Suppose you decrease the threshold to 0.3. Which of the following are true? Check all that apply.

### Answer

* The classifier is likely to now have higher precision.
* **The classifier is likely to now have higher recall.**
* The classifier is likely to have unchanged precision and recall, but higher accuracy.
* The classifier is likely to have unchanged precision and recall, but lower accuracy.

---
## Question 4

Suppose you are working on a spam classifier, where spam emails are positive examples (y=1) and non-spam emails are negative examples (y=0). You have a training set of emails in which 99% of the emails are non-spam and the other 1% is spam. Which of the following statements are true? Check all that apply.

### Answer

* **If you always predict non-spam (output y=0), your classifier will have an accuracy of 99%.**
* **If you always predict non-spam (output y=0), your classifier will have a recall of 0%.**
* **If you always predict spam (output y=1), your classifier will have a recall of 100% and precision of 1%.**
* If you always predict spam (output y=1), your classifier will have a recall of 0% and precision of 99%.

---

## Question 5

Which of the following statements are true? Check all that apply.

### Answer
* After training a logistic regression classifier, you must use 0.5 as your threshold for predicting whether an example is positive or negative.
* **The "error analysis" process of manually examining the examples which your algorithm got wrong can help suggest what are good steps to take (e.g., developing new features) to improve your algorithm's performance.**
* If your model is underfitting the training set, then obtaining more data is likely to help.
* It is a good idea to spend a lot of time collecting a large amount of data before building your first version of a learning algorithm.
* **Using a very large training set makes it unlikely for model to overfit the training data.**
