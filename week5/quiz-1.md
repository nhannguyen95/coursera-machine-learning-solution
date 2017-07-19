# Quiz: Neural Networks: Learning

## Question 1
You are training a three layer neural network and would like to use backpropagation to compute the gradient of the cost function. In the backpropagation algorithm, one of the steps is to update

<a href="https://www.codecogs.com/eqnedit.php?latex=\Delta^{(2)}_{ij}&space;:=&space;\Delta^{(2)}_{ij}&space;&plus;&space;\delta^{(3)}_i&space;*&space;(a^{(2)})_j" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Delta^{(2)}_{ij}&space;:=&space;\Delta^{(2)}_{ij}&space;&plus;&space;\delta^{(3)}_i&space;*&space;(a^{(2)})_j" title="\Delta^{(2)}_{ij} := \Delta^{(2)}_{ij} + \delta^{(3)}_i * (a^{(2)})_j" /></a>

for every i,j. Which of the following is a correct vectorization of this step?

### Answer
* <a href="https://www.codecogs.com/eqnedit.php?latex=\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;(a^{(3)})^T&space;*&space;\delta^{(3)}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;(a^{(3)})^T&space;*&space;\delta^{(3)}" title="\Delta^{(2)} := \Delta^{(2)} + (a^{(3)})^T * \delta^{(3)}" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(3)}&space;*&space;(a^{(3)})^T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(3)}&space;*&space;(a^{(3)})^T" title="\Delta^{(2)} := \Delta^{(2)} + \delta^{(3)} * (a^{(3)})^T" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(3)}&space;*&space;(a^{(2)})^T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(3)}&space;*&space;(a^{(2)})^T" title="\Delta^{(2)} := \Delta^{(2)} + \delta^{(3)} * (a^{(2)})^T" /></a>
* <a href="https://www.codecogs.com/eqnedit.php?latex=\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(2)}&space;*&space;(a^{(2)})^T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\Delta^{(2)}&space;:=&space;\Delta^{(2)}&space;&plus;&space;\delta^{(2)}&space;*&space;(a^{(2)})^T" title="\Delta^{(2)} := \Delta^{(2)} + \delta^{(2)} * (a^{(2)})^T" /></a>

C

---

## Question 2
Suppose 𝚃𝚑𝚎𝚝𝚊𝟷 is a 5x3 matrix, and 𝚃𝚑𝚎𝚝𝚊𝟸 is a 4x6 matrix. You set 𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌=[𝚃𝚑𝚎𝚝𝚊𝟷(:);𝚃𝚑𝚎𝚝𝚊𝟸(:)]. Which of the following correctly recovers 𝚃𝚑𝚎𝚝𝚊𝟸?

### Answer
* **𝚛𝚎𝚜𝚑𝚊𝚙𝚎(𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌(𝟷𝟼:𝟹𝟿),𝟺,𝟼)**
* 𝚛𝚎𝚜𝚑𝚊𝚙𝚎(𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌(𝟷𝟻:𝟹𝟾),𝟺,𝟼)
* 𝚛𝚎𝚜𝚑𝚊𝚙𝚎(𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌(𝟷𝟼:𝟸𝟺),𝟺,𝟼)
* 𝚛𝚎𝚜𝚑𝚊𝚙𝚎(𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌(𝟷𝟻:𝟹𝟿),𝟺,𝟼)
* 𝚛𝚎𝚜𝚑𝚊𝚙𝚎(𝚝𝚑𝚎𝚝𝚊𝚅𝚎𝚌(𝟷𝟼:𝟹𝟿),𝟼,𝟺)

A

---

## Question 3
Let J(θ)=2θ<sup>3</sup>+2. Let θ=1, and ϵ=0.01. Use the formula (J(θ+ϵ)−J(θ−ϵ))/2ϵ to numerically compute an approximation to the derivative at θ=1. What value do you get? (When θ=1, the true/exact derivative is dJ(θ)/dθ=6.)

### Answer
* 6
* 8
* **6.0002**
* 5.9998

---

## Question 4
Which of the following statements are true? Check all that apply.

### Answer
* Computing the gradient of the cost function in a neural network has the same efficiency when we use backpropagation or when we numerically compute it using the method of gradient checking.
* **Using gradient checking can help verify if one's implementation of backpropagation is bug-free.**
* Gradient checking is useful if we are using one of the advanced optimization methods (such as in fminunc) as our optimization algorithm. However, it serves little purpose if we are using gradient descent.
* **For computational efficiency, after we have performed gradient checking to verify that our backpropagation code is correct, we usually disable gradient checking before using backpropagation to train the network.**

---

## Question 5
Which of the following statements are true? Check all that apply.

### Answer
* If we initialize all the parameters of a neural network to ones instead of zeros, this will suffice for the purpose of "symmetry breaking" because the parameters are no longer symmetrically equal to zero.
* Suppose you have a three layer network with parameters Θ(1) (controlling the function mapping from the inputs to the hidden units) and Θ(2) (controlling the mapping from the hidden units to the outputs). If we set all the elements of Θ(1) to be 0, and all the elements of Θ(2) to be 1, then this suffices for symmetry breaking, since the neurons are no longer all computing the same function of the input.
* **If we are training a neural network using gradient descent, one reasonable "debugging" step to make sure it is working is to plot J(Θ) as a function of the number of iterations, and make sure it is decreasing (or at least non-increasing) after each iteration.**
* **Suppose you are training a neural network using gradient descent. Depending on your random initialization, your algorithm may converge to different local optima (i.e., if you run the algorithm twice with different random initializations, gradient descent may converge to two different solutions).**
