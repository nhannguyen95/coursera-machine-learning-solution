# Quiz: Unsupervised Learning

## Question 1
For which of the following tasks might K-means clustering be a suitable algorithm? Select all that apply.

### Answer
* Given historical weather records, predict if tomorrow's weather will be sunny or rainy.

* Given many emails, you want to determine if they are Spam or Non-Spam emails.

* **Given a set of news articles from many different news websites, find out what are the main topics covered.**

* **From the user usage patterns on a website, figure out what different groups of users exist.**

---

## Question 2
Suppose we have three cluster centroids μ<sub>1</sub>=[1 2]<sup>T</sup>, μ<sub>1</sub>2=[−3 0]<sup>T</sup> and μ<sub>3</sub>=[4 2]<sup>T</sup>. Furthermore, we have a training example x<sup>(i)</sup>=[−1 2]<sup>T</sup>. After a cluster assignment step, what will c<sup>(i)</sup> be?

### Answer
* c<sup>(i)</sup>=3

* c<sup>(i)</sup>=2

* c<sup>(i)</sup> is not assigned

* **c<sup>(i)</sup>=1**

---

## Question 3
K-means is an iterative algorithm, and two of the following steps are repeatedly carried out in its inner-loop. Which two?

### Answer
* Move each cluster centroid μ<sub>k</sub>, by setting it to be equal to the closest training example x<sup>(i)</sup>

* **Move the cluster centroids, where the centroids μ<sub>k</sub> are updated.**

* **The cluster assignment step, where the parameters c<sup>(i)</sup> are updated.**

* The cluster centroid assignment step, where each cluster centroid μ<sub>i</sub> is assigned (by setting c<sup>(i)</sup>) to the closest training example x<sup>(i)</sup>.

---
## Question 4
Suppose you have an unlabeled dataset {x<sup>(1)</sup>,…,x<sup>(m)</sup>}. You run K-means with 50 different random initializations, and obtain 50 different clusterings of the data. What is the recommended way for choosing which one of these 50 clusterings to use?

### Answer
* Always pick the final (50th) clustering found, since by that time it is more likely to have converged to a good solution.

* For each of the clusterings, compute cost function, and pick the one that minimizes this.

* The answer is ambiguous, and there is no good way of choosing.

* The only way to do so is if we also have labels y<sup>(i)</sup> for our data.

---
## Question 5
Which of the following statements are true? Select all that apply.

### Answer
* Once an example has been assigned to a particular centroid, it will never be reassigned to another different centroid

* **On every iteration of K-means, the cost function J (the distortion function) should either stay the same or decrease; in particular, it should not increase.**

* **A good way to initialize K-means is to select K (distinct) examples from the training set and set the cluster centroids equal to these selected examples.**

* K-Means will always give the same results regardless of the initialization of the centroids.
