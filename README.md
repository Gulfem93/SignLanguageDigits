# Sign Language Digits
![image](https://miro.medium.com/max/648/1*7YExRBgHMnJAFPEw-HYt_Q.png)

## Introduction

* Numbers 0 to 9 were classified by image processing from the fingers.
  * If the finger points to 0, the result is 0.
  * If the finger points to 1, the result is 1.
  * If the finger points to 2, the result is 2.
  * If the finger points to 3, the result is 3.
  * If the finger points to 4, the result is 4.
  * If the finger points to 5, the result is 5.
  * If the finger points to 6, the result is 6.
  * If the finger points to 7, the result is 7.
  * If the finger points to 8, the result is 8.
  * If the finger points to 9, the result is 9.

## Steps:

* We read data
* Only looked at the difference between 1 and 0.
* Train-Test Split 
* After we look Logistic Regression

## Logistic Regression Steps:
![image](http://preview.ibb.co/cxP63H/5.jpg)

1. Initialize Paramaters:
  * The determining parameters for Logistic Regression are weight and bias. These parameters are defined at first.
    * How do I determine the values of weight and bias parameters?
      * There are several methods for this. One of them is initially weight = 0.01 and bias = 0.0
2. Forward Propagation
  * Based on the graph, we get a predictive value.
  * z = px1 * w1 + px2 * w2 + px3 * w3 + .... + px4096 * w4096 + b
  * I insert the z value into the sigmoid function and it gives me a value between 0 and 1.
  * Prediction values (y_head) appear. From here we calculate the loss function
      * Loss Function:
      ![image](https://image.ibb.co/eC0JCK/duzeltme.jpg)
      * Cost function is the sum of loss functions.
      
3. Backward Propogation 
  * If the cost function found is large, we will return.
  * We apply backward propogation.
  * The goal is to minimize the cost function.
  * I use gradient descent for this.
  ![gradient](http://image.ibb.co/dAaYJH/7.jpg)
  
 * In the graph in the figure, slopes are slopes.
 * Slopes are taken into account for gradient descent.
 * Formula:
 ![gradient](http://image.ibb.co/hYTTJH/8.jpg)
  
  * ∂J / ∂w = (1 / m) * (x * (yhead − y)T)
  * ∂J / ∂b = (1 / m) * (m∑(yhead − y))
