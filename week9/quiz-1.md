# Quiz: Anomaly Detection

## Question 1:
For which of the following problems would anomaly detection be a suitable algorithm?

### Answer
* **From a large set of primary care patient records, identify individuals who might have unusual health conditions.**

* From a large set of hospital patient records, predict which patients have a particular disease (say, the flu).

* **In a computer chip fabrication plant, identify microchips that might be defective.**

* Given data from credit card transactions, classify each transaction according to type of purchase (for example: food, transportation, clothing).

---

## Question 2:
Suppose you have trained an anomaly detection system for fraud detection, and your system that flags anomalies when p(x) is less than ε, and you find on the cross-validation set that it is missing many fradulent transactions (i.e., failing to flag them as anomalies). What should you do?

### Answer
* Decrease ε

* **Increase ε**

---

## Question 3:
Suppose you are developing an anomaly detection system to catch manufacturing defects in airplane engines. You model uses

<a href="https://www.codecogs.com/eqnedit.php?latex=p(x)&space;=&space;\prod_{j=1}^n&space;p(x_j&space;;&space;\mu_j,&space;\sigma^2_j)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p(x)&space;=&space;\prod_{j=1}^n&space;p(x_j&space;;&space;\mu_j,&space;\sigma^2_j)" title="p(x) = \prod_{j=1}^n p(x_j ; \mu_j, \sigma^2_j)" /></a>

You have two features x1 = vibration intensity, and x2 = heat generated. Both x1 and x2 take on values between 0 and 1 (and are strictly greater than 0), and for most "normal" engines you expect that x1≈x2. One of the suspected anomalies is that a flawed engine may vibrate very intensely even without generating much heat (large x1, small x2), even though the particular values of x1 and x2 may not fall outside their typical ranges of values. What additional feature x3 should you create to capture these types of anomalies:

### Answer
* x<sub>3</sub>=(x<sub>1</sub>+x<sub>2</sub>)<sup>2</sup>

* x<sub>3</sub>=x<sub>1</sub>×x<sub>2</sub><sup>2</sup>

* x<sub>3</sub>=x<sub>1</sub>/x<sub>2</sub>

* x<sub>3</sub>=x<sub>1</sub><sup>2</sup>×x<sub>2</sub><sup>2</sup>.

---

## Question 4:
Which of the following are true? Check all that apply.

### Answer
* If you are developing an anomaly detection system, there is no way to make use of labeled data to improve your system.

* If you have a large labeled training set with many positive examples and many negative examples, the anomaly detection algorithm will likely perform just as well as a supervised learning algorithm such as an SVM.

* **If you do not have any labeled data (or if all your data has label y=0), then is is still possible to learn p(x), but it may be harder to evaluate the system or choose a good value of ϵ.**

* **When choosing features for an anomaly detection system, it is a good idea to look for features that take on unusually large or small values for (mainly the) anomalous examples.**

---
## Question 5:
You have a 1-D dataset {x<sup>(1)</sup>,…,x<sup>(m)</sup>} and you want to detect outliers in the dataset. You first plot the dataset and it looks like this:

<img src="https://i.imgur.com/SrHZV0u.png"/>

Suppose you fit the gaussian distribution parameters μ<sub>1</sub> and σ<sub>1</sub><sup>2</sup> to this dataset. Which of the following values for μ<sub>1</sub> and σ<sub>1</sub><sup>2</sup> might you get?

---

* μ<sub>1</sub> = -3,  σ<sub>1</sub><sup>2</sup> = 4
* μ<sub>1</sub> = -6,  σ<sub>1</sub><sup>2</sup> = 4
* **μ<sub>1</sub> = -3,  σ<sub>1</sub><sup>2</sup> = 2**
* μ<sub>1</sub> = -6,  σ<sub>1</sub><sup>2</sup> = 2
