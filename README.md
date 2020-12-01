
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


<img src="https://render.githubusercontent.com/render/math?math=\left|q\right\rangle =CNOT_{12}\left|q_{1}\right\rangle \otimes\left|q_{2}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|00\right\rangle +\left|11\right\rangle \right) ">
 
 
### Step 3. Represent q0, q1 and q2 as a state 

<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0}\right\rangle"> is a random state.


<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0}\right\rangle =\alpha\left|0\right\rangle +\beta\left|1\right\rangle ">

Write down <img src="https://render.githubusercontent.com/render/math?math=\left|q_{0}\right\rangle">, <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle"> and <img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle"> as a state for the purpose of a better understanding how the teleportation works


<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1},q_{2}\right\rangle =\left|q_{0}\right\rangle \otimes\left|q_{1},q_{2}\right\rangle =\left(\alpha\left|0\right\rangle %2B \beta\left|1\right\rangle \right)\otimes\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B \left|00\right\rangle \right) ">


<img src="https://render.githubusercontent.com/render/math?math==\frac{1}{\sqrt{2}}\left(\alpha\left|011\right\rangle %2B\alpha\left|000\right\rangle %2B\beta\left|111\right\rangle %2B\beta\left|100\right\rangle \right)">

<img src="https://render.githubusercontent.com/render/math?math==\frac{\alpha}{\sqrt{2}}\left(\left|01\right\rangle \otimes\left|1\right\rangle \right)%2B\frac{\alpha}{\sqrt{2}}\left(\left|00\right\rangle \otimes\left|0\right\rangle \right)%2B\frac{\beta}{\sqrt{2}}\left(\left|11\right\rangle \otimes\left|1\right\rangle \right)%2B\frac{\beta}{\sqrt{2}}\left(\left|10\right\rangle \otimes\left|0\right\rangle \right)">

### Step 4. Represent <img src="https://render.githubusercontent.com/render/math?math=\left|q_{00}\right\rangle"> , <img src="https://render.githubusercontent.com/render/math?math=\left|q_{01}\right\rangle">, <img src="https://render.githubusercontent.com/render/math?math=\left|q_{10}\right\rangle"> , and <img src="https://render.githubusercontent.com/render/math?math=\left|q_{11}\right\rangle">  using the Bell states:


<img src="https://render.githubusercontent.com/render/math?math=\left|01\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Phi^{+}\right\rangle -\left|\Phi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|00\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Psi^{+}\right\rangle -\left|\Psi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|10\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Phi^{+}\right\rangle %2B\left|\Phi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|11\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Psi^{+}\right\rangle %2B\left|\Psi^{-}\right\rangle \right)">


So now <img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1}q_{2}\right\rangle  ">  can be represented as follows,


<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1}q_{2}\right\rangle ">

<img src="https://render.githubusercontent.com/render/math?math==\left\{ \left[\frac{\alpha}{2}\left(\left|\Phi^{%2B}\right\rangle -\left|\Phi^{-}\right\rangle \right)\otimes\left|1\right\rangle %2B\frac{\alpha}{2}\left(\left|\Psi^{%2B}\right\rangle -\left|\Psi^{-}\right\rangle \right)\otimes\left|0\right\rangle %2B\frac{\beta}{2}\left(\left|\Psi^{%2B}\right\rangle %2B\left|\Psi^{-}\right\rangle \right)\otimes\left|1\right\rangle +\frac{\beta}{2}\left(\left|\Phi^{%2B}\right\rangle %2B\left|\Phi^{-}\right\rangle \otimes\left|0\right\rangle \right)\right]\right\} ">


<img src="https://render.githubusercontent.com/render/math?math==\left[\left|\Phi^{+}\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|\Psi^{%2B}\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle %2B\frac{\beta}{2}\left|1\right\rangle \right)%2B\left|\Phi^{-}\right\rangle \otimes\left(\frac{-\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|\Psi^{-}\right\rangle \otimes\left(\frac{-\alpha}{2}\left|0\right\rangle %2B\frac{\beta}{2}\left|1\right\rangle \right)\right]">



### Step 4.  Transform the Bell states into <img src="https://render.githubusercontent.com/render/math?math=\left|q_{00}\right\rangle"> , <img src="https://render.githubusercontent.com/render/math?math=\left|q_{01}\right\rangle">, <img src="https://render.githubusercontent.com/render/math?math=\left|q_{10}\right\rangle"> , and <img src="https://render.githubusercontent.com/render/math?math=\left|q_{11}\right\rangle"> by applying <img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\right) "> on <img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1},q_{2}\right\rangle"> :


<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Phi^{%2B}\right\rangle \right)\right)=H_{0}\left(\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B\left|01\right\rangle \right)\right)=\frac{1}{2}\left[\left(\left|0\right\rangle -\left|1\right\rangle \right)\otimes\left|1\right\rangle %2B\left(\left|0\right\rangle %2B\left|1\right\rangle \right)\otimes\left|1\right\rangle \right]=\left|01\right\rangle">

Similarly,

<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Psi^{%2B}\right\rangle \right)\right)=\left|00\right\rangle">
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Phi^{-}\right\rangle \right)\right)=-\left|11\right\rangle">
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Psi^{-}\right\rangle \right)\right)=-\left|10\right\rangle">

Substituting the above equations to
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|q_{0},q_{1},q_{2}\right\rangle \right)\right)">,


<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|q_{0},q_{1},q_{2}\right\rangle \right)\right)">
<img src="https://render.githubusercontent.com/render/math?math==\left[\left|01\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|00\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle +\frac{\beta}{2}\left|1\right\rangle \right)%2B\left|11\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle -\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|10\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle -\frac{\beta}{2}\left|1\right\rangle \right)\right]">


By perfoming the measurement on <img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1}\right\rangle "> , the state will be collapsed to one of the following states:




