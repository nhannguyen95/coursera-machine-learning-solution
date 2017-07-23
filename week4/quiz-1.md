# Quiz: Neural Networks: Representation

## Question 1
Which of the following statements are true? Check all that apply.

### Answer
* **Any logical function over binary-valued (0 or 1) inputs x1 and x2 can be (approximately) represented using some neural network.**
* A two layer (one input layer, one output layer; no hidden layer) neural network can represent the XOR function.
* **The activation values of the hidden units in a neural network, with the sigmoid activation function applied at every layer, are always in the range (0, 1).**
* Suppose you have a multi-class classification problem with three classes, trained with a 3 layer network. Let a<sub>1</sub><sup>(3)</sup>=(hΘ(x))<sub>1</sub> be the activation of the first output unit, and similarly a<sub>2</sub><sup>(3)</sup>=(hΘ(x))<sub>2</sub> and a<sub>3</sub><sup>(3)</sup>=(hΘ(x))<sub>3</sub>. Then for any input x, it must be the case that a<sub>1</sub><sup>(3)</sup>+a<sub>2</sub><sup>(3)</sup>+a<sub>3</sub><sup>(3)</sup>=1.

---
## Question 2
Consider the following neural network which takes two binary-valued inputs x1,x2∈{0,1} and outputs hΘ(x). Which of the following logical functions does it (approximately) compute?

<img src="">

### Answer
* **AND**
* NAND (meaning "NOT AND")
* OR
* XOR (exclusive OR)

---
## Question 3
Consider the neural network given below. Which of the following equations correctly computes the activation a<sub>1</sub><sup>(3)</sup>? Note: g(z) is the sigmoid activation function.

<img src="">

### Answer
* **a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>1,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>1,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(2)</sup>)**
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(1)</sup>+Θ<sub>1,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(1)</sup>+Θ<sub>1,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(1)</sup>)
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(1)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>1,1</sub><sup>(1)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>1,2</sub><sup>(1)</sup>a<sub>2</sub><sup>(2)</sup>)
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>2,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>2,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>2,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(2)</sup>)

---
## Question 4
You have the following neural network:

<img src="">

You'd like to compute the activations of the hidden layer a(2)∈ℝ3. One way to do so is the following Octave code:

<img src="">

You want to have a vectorized implementation of this (i.e., one that does not use for loops). Which of the following implementations correctly compute a(2)? Check all that apply.

### Answer
* **a2 = sigmoid (Theta1 * x);**
* a2 = sigmoid (x * Theta1);
* a2 = sigmoid (Theta2 * x);
* z = sigmoid(x); a2 = Theta1 * z;

---

## Question 5
You are using the neural network pictured below and have learned the parameters <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;2.1&space;&&space;1.3&space;\\&space;1&space;&&space;0.6&space;&&space;-1.2\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;2.1&space;&&space;1.3&space;\\&space;1&space;&&space;0.6&space;&&space;-1.2\end{bmatrix}" title="\Theta^{(1)} = \begin{bmatrix} 1 & 2.1 & 1.3 \\ 1 & 0.6 & -1.2\end{bmatrix}" /></a> (used to compute a(2))) and <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;4.5&space;&&space;3.1&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;4.5&space;&&space;3.1&space;\end{bmatrix}" title="\Theta^{(2)} = \begin{bmatrix} 1 & 4.5 & 3.1 \end{bmatrix}" /></a> (used to compute a(3)} as a function of a(2)). Suppose you swap the parameters for the first hidden layer between its two units so <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;0.6&space;&&space;-1.2&space;\\&space;1&space;&&space;2.1&space;&&space;1.3&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;0.6&space;&&space;-1.2&space;\\&space;1&space;&&space;2.1&space;&&space;1.3&space;\end{bmatrix}" title="\Theta^{(1)} = \begin{bmatrix} 1 & 0.6 & -1.2 \\ 1 & 2.1 & 1.3 \end{bmatrix}" /></a> and also swap the output layer so <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;3.1&space;&&space;4.5&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;3.1&space;&&space;4.5&space;\end{bmatrix}" title="\Theta^{(2)} = \begin{bmatrix} 1 & 3.1 & 4.5 \end{bmatrix}" /></a> . How will this change the value of the output hΘ(x)?

<img src="">

### Answer
* **It will stay the same.**
* It will increase.
* It will decrease
* Insufficient information to tell: it may increase or decrease.
