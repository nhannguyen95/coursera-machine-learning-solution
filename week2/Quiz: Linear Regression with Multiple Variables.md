# Quiz: Linear Regression with Multiple Variables

## Question 1
Suppose m=4 students have taken some class, and the class had a midterm exam and a final exam. You have collected a dataset of their scores on the two exams, which is as follows:

| midterm exam | (midterm exam)^2 | final exam |
|--------------|------------------|------------|
|89|7921|96|
|72|5184|74|
|94|8836|87|
|69|4761|78|

You'd like to use polynomial regression to predict a student's final exam score from their midterm exam score. Concretely, suppose you want to fit a model of the form hθ(x)=θ0+θ1x1+θ2x2, where x1 is the midterm score and x2 is (midterm score)2. Further, you plan to use both feature scaling (dividing by the "max-min", or range, of a feature) and mean normalization.

What is the normalized feature x<sub>1</sub><sup>(1)</sup>? (Hint: midterm = 89, final = 96 is training example 1.) Please round off your answer to two decimal places and enter in the text box below.

### Answer

Mean of x1 = (89 + 72 + 94 + 69) / 4 = 81

Range of x1 = Max of x1 - Min of x1 = 94 - 69 = 25

So x<sub>1</sub><sup>(1)</sup> = (89 - 81) / 25 = 0.32

### Octave code
```octave
data = [89, 7921, 96; 72, 5184, 74; 94, 8836, 87; 69, 4761, 78]

row = 1
col = 1

mean = mean(data)(col)
min = min(data)(col)
max = max(data)(col)
current = data(row)(col)

normalizedValue = (current - mean) / (max - min)
```
---
## Question 2

You run gradient descent for 15 iterations with α=0.3 and compute J(θ) after each iteration. You find that the value of J(θ) increases over time. Based on this, which of the following conclusions seems most plausible ?

### Answer
* α=0.3 is an effective choice of learning rate.
* Rather than use the current value of α, it'd be more promising to try a larger value of α (say α=1.0).
* **Rather than use the current value of α, it'd be more promising to try a smaller value of α (say α=0.1).**
---

## Question 3

Suppose you have m=28 training examples with n=4 features (excluding the additional all-ones feature for the intercept term, which you should add). The normal equation is θ=(X<sup>T</sup>X)<sup>-1</sup>X<sup>T</sup>y. For the given values of m and n, what are the dimensions of θ, X, and y in this equation?

### Answer
* X is 28×5, y is 28×5, θ is 5×5
* **X is 28×5, y is 28×1, θ is 5×1**
* X is 28×4, y is 28×1, θ is 4×4
* X is 28×4, y is 28×1, θ is4×1

---

## Question 4

Suppose you have a dataset with m=50 examples and n=200000 features for each example. You want to use multivariate linear regression to fit the parameters θ to our data. Should you prefer gradient descent or the normal equation ?

### Answer
* Gradient descent, since it will always converge to the optimal θ.
* The normal equation, since gradient descent might be unable to find the optimal θ.
* **Gradient descent, since (X<sup>T</sup>X)<sup>-1</sup> will be very slow to compute in the normal equation.**
* The normal equation, since it provides an efficient way to directly find the solution.

---

## Question 5

Which of the following are reasons for using feature scaling?

### Answer
* It prevents the matrix (X<sup>T</sup>X) (used in the normal equation) from being non-invertable (singular/degenerate).
* It is necessary to prevent the normal equation from getting stuck in local optima.
* **It speeds up gradient descent by making it require fewer iterations to get to a good solution.**
* It speeds up gradient descent by making each iteration of gradient descent less expensive to compute.
