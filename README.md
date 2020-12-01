
# Quantum Teleportation

## Description:
This repository is used to explain the quantum teleportation qiskit code in a mathematical way. 


Original Code: https://qiskit.org/textbook/ch-algorithms/teleportation.html
Content includes the step-by-step math for the quantum teleportation. 


## Video Link to the explanation
- Youtube link to the video for the explanation
https://www.youtube.com/watch?v=cEhMuMWtThU&t=26s

## Process:
### Step 1. Bell States 
Write down the Bell States for use:
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Psi^{%2B}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B \left|00\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Phi^{%2B}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|10\right\rangle %2B\left|01\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Psi^{-}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|11\right\rangle -\left|00\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Phi^{-}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|10\right\rangle -\left|01\right\rangle \right)">


### Step 2. Generate a Bell state

Initialize <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle">
and <img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle">:

- <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle =\left|0\right\rangle">
- <img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle =\left|0\right\rangle">

Have <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1},q_{2}\right\rangle">  become a Bell state by applying a hadamard gate on <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle"> and a CNOT gate on <img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle">
:

Apply a Hadamard gate 
<img src="https://render.githubusercontent.com/render/math?math=H">
on 
<img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle ">
and a CNOT gate on
<img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle ">
:

<img src="https://render.githubusercontent.com/render/math?math=H\left|q_{1}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|1\right\rangle %2B\left|0\right\rangle \right)">

Tensor product <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle "> and
<img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle ">
:

<img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle \otimes\left|q_{2}\right\rangle =\frac{1}{\sqrt{2}}\left[\left(\left|1\right\rangle %2B\left|0\right\rangle \right)\otimes\left|0\right\rangle \right]=\frac{1}{\sqrt{2}}\left(\left|10\right\rangle %2B\left|00\right\rangle \right)">

Apply a CNOT gate on 
<img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle ">
:


<img src="https://render.githubusercontent.com/render/math?math=\left|q\right\rangle =CNOT_{12}\left|q_{1}\right\rangle \otimes\left|q_{2}\right\rangle ">
 




