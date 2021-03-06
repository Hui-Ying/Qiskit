
# Quantum Teleportation

## Description: 
- Content includes the step-by-step math for the quantum teleportation tutorial on qiskit. 
- Original Code: https://qiskit.org/textbook/ch-algorithms/teleportation.html


## Video Link to the explanation
- Youtube link to the video for the explanation, please click [here](https://www.youtube.com/watch?v=cEhMuMWtThU&t=26s)  
Circuit Demo:  
<img src="/images/teleportation_circuit.png" width="800" height="300">  
Measurement Result: 
<img src="/images/teleportation_result.png" width="600" height="350">  


## Bell States Definition
Write down the Bell States for use:
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Psi^{%2B}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B \left|00\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Phi^{%2B}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|10\right\rangle %2B\left|01\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Psi^{-}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|11\right\rangle -\left|00\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|\Phi^{-}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|10\right\rangle -\left|01\right\rangle \right)">

## Process:

### Step 1. Generate a Bell state

Initialize |q1> and |q2>:

- <img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle =\left|0\right\rangle">
- <img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle =\left|0\right\rangle">

Create a Bell state |q1, q2> by applying a Hadamard gate on |q1> and a CNOT gate on |q2>:

Apply a Hadamard gate 
<img src="https://render.githubusercontent.com/render/math?math=H">
on |q1> and a CNOT gate on |q2>:

<img src="https://render.githubusercontent.com/render/math?math=H\left|q_{1}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|1\right\rangle %2B\left|0\right\rangle \right)">

Tensor product |q1>  and |q2>:

<img src="https://render.githubusercontent.com/render/math?math=\left|q_{1}\right\rangle \otimes\left|q_{2}\right\rangle =\frac{1}{\sqrt{2}}\left[\left(\left|1\right\rangle %2B\left|0\right\rangle \right)\otimes\left|0\right\rangle \right]=\frac{1}{\sqrt{2}}\left(\left|10\right\rangle %2B\left|00\right\rangle \right)">

Apply a CNOT gate on |q2>:


<img src="https://render.githubusercontent.com/render/math?math=\left|q\right\rangle =CNOT_{12}\left|q_{1}\right\rangle \otimes\left|q_{2}\right\rangle =\frac{1}{\sqrt{2}}\left(\left|00\right\rangle %2B\left|11\right\rangle \right) ">: Bell state created!
 
 
### Step 2. Represent q0, q1 and q2 as a state |q0, q1, q2>

|q0>  is a random state.


<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0}\right\rangle =\alpha\left|0\right\rangle %2B\beta\left|1\right\rangle ">

Write down |q0>,|q1> and |q2> as a state for a better understanding of how the teleportation works


<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1},q_{2}\right\rangle =\left|q_{0}\right\rangle \otimes\left|q_{1},q_{2}\right\rangle =\left(\alpha\left|0\right\rangle %2B \beta\left|1\right\rangle \right)\otimes\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B \left|00\right\rangle \right) ">


<img src="https://render.githubusercontent.com/render/math?math==\frac{1}{\sqrt{2}}\left(\alpha\left|011\right\rangle %2B\alpha\left|000\right\rangle %2B\beta\left|111\right\rangle %2B\beta\left|100\right\rangle \right)">

<img src="https://render.githubusercontent.com/render/math?math==\frac{\alpha}{\sqrt{2}}\left(\left|01\right\rangle \otimes\left|1\right\rangle \right)%2B\frac{\alpha}{\sqrt{2}}\left(\left|00\right\rangle \otimes\left|0\right\rangle \right)%2B\frac{\beta}{\sqrt{2}}\left(\left|11\right\rangle \otimes\left|1\right\rangle \right)%2B\frac{\beta}{\sqrt{2}}\left(\left|10\right\rangle \otimes\left|0\right\rangle \right)">


### Step 3. Represent states |00>, |01>, |10>, and |11> using the Bell states:


<img src="https://render.githubusercontent.com/render/math?math=\left|01\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Phi^{+}\right\rangle -\left|\Phi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|00\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Psi^{+}\right\rangle -\left|\Psi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|10\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Phi^{+}\right\rangle %2B\left|\Phi^{-}\right\rangle \right)">


<img src="https://render.githubusercontent.com/render/math?math=\left|11\right\rangle =\frac{1}{\sqrt{2}}\left(\left|\Psi^{+}\right\rangle %2B\left|\Psi^{-}\right\rangle \right)">


Now |q0, q1, q2>  can be represented as follows,

<img src="https://render.githubusercontent.com/render/math?math=\left|q_{0},q_{1},q_{2}\right\rangle ">

<img src="https://render.githubusercontent.com/render/math?math==\left\{ \left[\frac{\alpha}{2}\left(\left|\Phi^{%2B}\right\rangle -\left|\Phi^{-}\right\rangle \right)\otimes\left|1\right\rangle %2B\frac{\alpha}{2}\left(\left|\Psi^{%2B}\right\rangle -\left|\Psi^{-}\right\rangle \right)\otimes\left|0\right\rangle %2B\frac{\beta}{2}\left(\left|\Psi^{%2B}\right\rangle %2B\left|\Psi^{-}\right\rangle \right)\otimes\left|1\right\rangle +\frac{\beta}{2}\left(\left|\Phi^{%2B}\right\rangle %2B\left|\Phi^{-}\right\rangle \otimes\left|0\right\rangle \right)\right]\right\} ">


<img src="https://render.githubusercontent.com/render/math?math==\left[\left|\Phi^{+}\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|\Psi^{%2B}\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle %2B\frac{\beta}{2}\left|1\right\rangle \right)%2B\left|\Phi^{-}\right\rangle \otimes\left(\frac{-\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|\Psi^{-}\right\rangle \otimes\left(\frac{-\alpha}{2}\left|0\right\rangle %2B\frac{\beta}{2}\left|1\right\rangle \right)\right]">




### Step 4.  Transform the Bell states into states |00>, |01>, |10>, and |11>  by applying CNOT gate and Hadamard gate on |q0, q1, q2>:


<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Phi^{%2B}\right\rangle \right)\right)=H_{0}\left(\frac{1}{\sqrt{2}}\left(\left|11\right\rangle %2B\left|01\right\rangle \right)\right)=\frac{1}{2}\left[\left(\left|0\right\rangle -\left|1\right\rangle \right)\otimes\left|1\right\rangle %2B\left(\left|0\right\rangle %2B\left|1\right\rangle \right)\otimes\left|1\right\rangle \right]=\left|01\right\rangle">

Similarly,

<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Psi^{%2B}\right\rangle \right)\right)=\left|00\right\rangle">
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Phi^{-}\right\rangle \right)\right)=-\left|11\right\rangle">
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|\Psi^{-}\right\rangle \right)\right)=-\left|10\right\rangle">

Plug the above equations into
<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|q_{0},q_{1},q_{2}\right\rangle \right)\right)">,


<img src="https://render.githubusercontent.com/render/math?math=H_{0}\left(CNOT_{01}\left(\left|q_{0},q_{1},q_{2}\right\rangle \right)\right)">
<img src="https://render.githubusercontent.com/render/math?math==\left[\left|01\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle %2B\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|00\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle +\frac{\beta}{2}\left|1\right\rangle \right)%2B\left|11\right\rangle \otimes\left(\frac{\alpha}{2}\left|1\right\rangle -\frac{\beta}{2}\left|0\right\rangle \right)%2B\left|10\right\rangle \otimes\left(\frac{\alpha}{2}\left|0\right\rangle -\frac{\beta}{2}\left|1\right\rangle \right)\right]">



### Step 5.Perform the measurement on states |q0> and |q1>:
By perfoming the measurement on |q0, q1>, the state will be collapsed to one of the following states:

- <img src="https://render.githubusercontent.com/render/math?math=\left|00\right\rangle \otimes\left(\alpha\left|0\right\rangle %2B\beta\left|1\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|01\right\rangle \otimes\left(\alpha\left|1\right\rangle %2B\beta\left|0\right\rangle \right) ">
- <img src="https://render.githubusercontent.com/render/math?math=\left|11\right\rangle \otimes\left(\alpha\left|1\right\rangle -\beta\left|0\right\rangle \right)">
- <img src="https://render.githubusercontent.com/render/math?math=\left|10\right\rangle \otimes\left(\alpha\left|0\right\rangle -\beta\left|1\right\rangle \right)">


In other words,

- When <img src="https://render.githubusercontent.com/render/math?math=\left|00\right\rangle \longrightarrow"> Do nothing
- When <img src="https://render.githubusercontent.com/render/math?math=\left|01\right\rangle \longrightarrow"> Apply X gate
- When <img src="https://render.githubusercontent.com/render/math?math=\left|11\right\rangle \longrightarrow"> Apply Z gate
- When <img src="https://render.githubusercontent.com/render/math?math=\left|10\right\rangle \longrightarrow"> Apply XZ gate


After applying the gates depending on the state,
<img src="https://render.githubusercontent.com/render/math?math=\left|q_{2}\right\rangle =\alpha\left|0\right\rangle %2B\beta\left|1\right\rangle ">

# Quantum Error Correction
Quantum error correction is one of the challenges of quantum control with quantum bits. For more details also check out this [article](https://huiyingsiao-72694.medium.com/challenges-of-quantum-control-with-superconducting-qubits-63486b95659b).
## The bit flip code[[1]](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.32.3266)  
Quantum error correction is crucial for quantum computers, here we discuss about the bit-flip code with two different inputs and demonstrate the simulation results. YouTube Concept explanation please click [here](https://www.youtube.com/watch?v=eyd8g_hoLgg) for the concept and [here](https://www.youtube.com/watch?v=2m5uTqMna7k&t=4s) for the code explanation. 


The bit flip code contains two parts(A & B).  
- Part A: |0> state as input  
Circuit Demo:  
<img src="/images/bit_flip-circuitA.png" width="800" height="200">  
The result shows that the probability of |0> state measured at the output.
<img src="/images/bit-flip-resultA.png" width="500" height="300">


- Part B: superposition state as input  
Here we initialize the state as a random superposition state.  
<img src="/images/bit-flip-randomB.png" width="250" height="250">  
Circuit Demo:  
<img src="/images/bit_flip-circuitB.png" width="800" height="400">  
The result shows that the probability of |0> state measured at the output.
<img src="/images/bit-flip-resultB.png" width="500" height="300"> 


## The sign flip code
Circuit Demo:    

<img src="/images/sign-flip-ckt.png" width="800" height="200">  
The result shows that the probability of |+> state to remain the same state at the output is 1. If there weren't any encoder then the probability for the sign-flip depends on the p we set for the error simulation.  
The result shows that the probability of |+> state measured at the output:
<img src="/images/sign-flip-result.png" width="500" height="300">


## The Shor code
Quantum error correction is crucial for quantum computers, here we discuss about the Shor code and the errors simulated using the noise model and demonstrate the simulation results. The Shor code can be used to correct both the bit-flip and the sign-flip errors using one code.
In the following code, a custom noise model was built by adding QuantumError to circuit gate. We domonstrate the measurement result from cases with and without the Shor code.
For more details please check the qiskit [tutorial](https://qiskit.org/documentation/apidoc/aer_noise.html).     
- Full code please click [here](https://github.com/Hui-Ying/Qiskit/blob/main/The%20Shor%20Code.pdf).
- Circuit Demo:  
1. Shor Code circuit  
<img src="/images/shor_code.png" width="800" height="400">  

2. Circuit without the error correction (simply with the error simulator) 
<img src="/images/simple.png" width="300" height="220">  

- Simulation results:
1. Shor Code circuit   
<img src="/images/with_shor.png" width="500" height="300">   
2. Circuit without the error correction (simply with the error simulator)  
<img src="/images/without_shor.png" width="500" height="300">  


## Surface code


# References
[[1]Reversible logic and quantum computers](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.32.3266)  
[[2]Wikipedia page of quantum error correction](https://en.wikipedia.org/wiki/Quantum_error_correction)
