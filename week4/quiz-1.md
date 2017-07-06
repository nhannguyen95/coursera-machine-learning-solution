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

<img src="https://d3c33hcgiwev3.cloudfront.net/Kf1MZL5zEeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.24.00-AM.png?Expires=1499472000&amp;Signature=AO5zu~r4jFSjTBkSzOUivs8GhYyJKHo1uVxe~exlOr0J1Xobt7KDaFT5L3l~69eqXiyMJ5z2~2cXmN2utPZUVWbKbGzHFPZU9G0TMQ5sdrSTtjB9kkRttN6uBVpkud9HzTVcA9tBbBQ0cOjRswPy-4OsWxJk1ue8fQIlrDBtdwg_&amp;Key-Pair-Id=APKAJLTNE6QMUY6HBC5A">

### Answer
* **AND**
* NAND (meaning "NOT AND")
* OR
* XOR (exclusive OR)

---
## Question 3
Consider the neural network given below. Which of the following equations correctly computes the activation a<sub>1</sub><sup>(3)</sup>? Note: g(z) is the sigmoid activation function.

<img src="https://d3c33hcgiwev3.cloudfront.net/FflwP750EeSGOCIAC3iXdw_Screen-Shot-2015-02-27-at-3.28.08-AM.png?Expires=1499472000&amp;Signature=h1tqN55ObGFF9RCNkSLDAbo7igtXhFwZekKmfabfxzfqP1kcZVdha1TVIgQKP4P3u7SVNqmntafeUfLm81r176biPOyecIXtTd1nxS0l0Utqm1WM-fix3p3bejMe2eOMqUZ0KZ55hcW69Z1UdoiRsGi5KxBJUMHslPErAn45a7o_&amp;Key-Pair-Id=APKAJLTNE6QMUY6HBC5A">

### Answer
* **a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>1,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>1,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(2)</sup>)**
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(1)</sup>+Θ<sub>1,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(1)</sup>+Θ<sub>1,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(1)</sup>)
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>1,0</sub><sup>(1)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>1,1</sub><sup>(1)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>1,2</sub><sup>(1)</sup>a<sub>2</sub><sup>(2)</sup>)
* a<sub>1</sub><sup>(3)</sup>=g(Θ<sub>2,0</sub><sup>(2)</sup>a<sub>0</sub><sup>(2)</sup>+Θ<sub>2,1</sub><sup>(2)</sup>a<sub>1</sub><sup>(2)</sup>+Θ<sub>2,2</sub><sup>(2)</sup>a<sub>2</sub><sup>(2)</sup>)

---
## Question 4
You have the following neural network:

<img src="https://d3c33hcgiwev3.cloudfront.net/lvSx8L50EeSGOCIAC3iXdw_Screen-Shot-2015-02-27-at-3.32.25-AM.png?Expires=1499472000&amp;Signature=RC1ZeO6ZRFFs-XCbFFNPgH1CJaidN4Emmb64tEY9OYYCgibG2NekcOdokPxlMOE6Ohi3Ril8AockQbOPIn9w8NW78JAe6HKhSGJzyRnbjQ~bUuLdNKK6cnf5H3eRLUn~X-pjZP2Fs8dJotomeF1OPbNfftJ0z4mAAZHdtZxQVd8_&amp;Key-Pair-Id=APKAJLTNE6QMUY6HBC5A">

You'd like to compute the activations of the hidden layer a(2)∈ℝ3. One way to do so is the following Octave code:

<img src="https://d3c33hcgiwev3.cloudfront.net/uLXmWL50EeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.32.38-AM.png?Expires=1499472000&amp;Signature=JiSvBL~cTukT2sCQsuQFeqMOIdK8ppShv6Ix2zJjl4DFCv8ps7T69dfmDiG-Vl~PEK4krQEfxoFPFofCeOUEEw856GQgdtTaUdd54iQ0bRELuGMAYhNccehPrcvRA0EAFEB-bpghzuPJHzKEUnFdio20zRbE~n5V4rqPRPr9ZCE_&amp;Key-Pair-Id=APKAJLTNE6QMUY6HBC5A">

You want to have a vectorized implementation of this (i.e., one that does not use for loops). Which of the following implementations correctly compute a(2)? Check all that apply.

### Answer
* **a2 = sigmoid (Theta1 * x);**
* a2 = sigmoid (x * Theta1);
* a2 = sigmoid (Theta2 * x);
* z = sigmoid(x); a2 = Theta1 * z;

---

## Question 5
You are using the neural network pictured below and have learned the parameters <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;2.1&space;&&space;1.3&space;\\&space;1&space;&&space;0.6&space;&&space;-1.2\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;2.1&space;&&space;1.3&space;\\&space;1&space;&&space;0.6&space;&&space;-1.2\end{bmatrix}" title="\Theta^{(1)} = \begin{bmatrix} 1 & 2.1 & 1.3 \\ 1 & 0.6 & -1.2\end{bmatrix}" /></a> (used to compute a(2))) and <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;4.5&space;&&space;3.1&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;4.5&space;&&space;3.1&space;\end{bmatrix}" title="\Theta^{(2)} = \begin{bmatrix} 1 & 4.5 & 3.1 \end{bmatrix}" /></a> (used to compute a(3)} as a function of a(2)). Suppose you swap the parameters for the first hidden layer between its two units so <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;0.6&space;&&space;-1.2&space;\\&space;1&space;&&space;2.1&space;&&space;1.3&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(1)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;0.6&space;&&space;-1.2&space;\\&space;1&space;&&space;2.1&space;&&space;1.3&space;\end{bmatrix}" title="\Theta^{(1)} = \begin{bmatrix} 1 & 0.6 & -1.2 \\ 1 & 2.1 & 1.3 \end{bmatrix}" /></a> and also swap the output layer so <a href="https://www.codecogs.com/eqnedit.php?latex=\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;3.1&space;&&space;4.5&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Theta^{(2)}&space;=&space;\begin{bmatrix}&space;1&space;&&space;3.1&space;&&space;4.5&space;\end{bmatrix}" title="\Theta^{(2)} = \begin{bmatrix} 1 & 3.1 & 4.5 \end{bmatrix}" /></a> . How will this change the value of the output hΘ(x)?

<img src="https://d3c33hcgiwev3.cloudfront.net/DnZ0rb52EeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.42.00-AM.png?Expires=1499472000&amp;Signature=UZ6sVWVWUTC3GnJw0HVkINfsAfwMm4wP5tcGC3XYE-r6Kt3Jgqu90iZ1kAVJ60CcTQUsVI6FzCec9N40P4j~jcg~mlVQOGcRavnfgUZH-1xXHTmnMnO4JQUp5V6zHzsBR-qbQ57iu1mBswhk66J4i8oPvhTo2dkrch9LOd52BtM_&amp;Key-Pair-Id=APKAJLTNE6QMUY6HBC5A">

### Answer
* **It will stay the same.**
* It will increase.
* It will decrease
* Insufficient information to tell: it may increase or decrease.
