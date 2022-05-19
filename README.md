### EX NO: 04
### DATE: 11-04-2022
# <p align="center"> BACK PROPAGATION IN A SINGLE NEURON</p>

## AIM:  
To write a python program to perform back propagation in single neuron.  

## Equipment’s Required:   

1.	Hardware – PCs   

2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab  
	  
## Concept:  
Backpropagation in neural network is a short form for “backward propagation of errors.” It is a standard method of training artificial neural networks. This method helps calculate the gradient of a loss function with respect to all the weights in the network. The Back propagation algorithm in neural network computes the gradient of the loss function for a single weight by the chain rule. It efficiently computes one layer at a time, unlike a native direct computation. It computes the gradient, but it does not define how the gradient is used. It generalizes the computation in the delta rule.

Consider the following Back propagation neural network example diagram to understand:

 ![image](https://user-images.githubusercontent.com/63917883/166474966-060f82a7-fa8f-451f-8355-663d3fa24fef.png)

## Libraries Used in the Program:

## NUMPY   
NumPy is a library for the Python programming language, adding support for large, multidimensional arrays and matrices, along with a large collection of highlevel mathematical functions to operate on these arrays.  

  
### Algorithm:  

1.	Start the program.  

2.	Import libraries required as per requirement.  

3.	Define neuron weight, eeta, i, y.  

4.	summarize observations by class label  

5.	summarize first few examples  	 use for loop for range.  

6.	stop the program.  
  
### Program:  
```
/* Program to implement back-Propagation in a single neuron
Developed by: U. VIVEK KRISHNA
Register Number: 212219040180
*/
```
```python3
import numpy as np

i=1.5

w_o=0.0

y=0.5

r=0.01

def dc_dw(a,y,i):

 dc_da=2*(a-y)
 
 da_dw=i
 
 return dc_da*da_dw

w=[w_o]

a=[w_o*i]

for j in range(0,100):

  a.append(w[-1]*i)
  
  w.append(w[-1]-r*dc_dw(a[-1],y,i))
  
  if(a[-1]-y)**2<0.001:
  
    break
    
print(a)

print(" ")

print(w)
```
  
## Output:  

![WhatsApp Image 2022-05-03 at 8 19 13 PM](https://user-images.githubusercontent.com/63917883/166477063-a1daaa73-2d58-416b-9801-23bbef1085bd.jpeg)

## Result:

Thus, the python program performed back propagation in single neuron.  
