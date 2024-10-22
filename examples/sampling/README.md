## Sampling the final states of a Quantum Circuit

**Problem:** How would you sample from the final states in the state vector or tensor representations?

### Instructions to run

The `sampling.py` file has the following two parameters:

1. `--num_samples <sample> (-n)`: Specifies the number of samples to be drawn. Default: 10
2. `--tensor_simulation`: Enables the use of Tensor simulation to simulate the quantum circuit

Run the program using:

```sh
python examples/sampling/sampling.py
```

### Explaination

In a vector simulation of a n-qubit system, each element describes a possible combination of the state of qubit. For n-qubits, the state vector will have 2^n states.

Any qubit can be represented as a weighted combination of |0> and |1> computational basis states.

> q = α |0> + β |1>

For a multi-qubit system, the state vector is calculated through the Kronecker product of all qubits within the system.

> q<sub>n</sub> = q<sub>1</sub> ⊗ q<sub>2</sub> ⊗ ... ⊗ q<sub>n</sub>

We can calulate the probability of each state by using the amplitude of each state |q<sub>i</sub>|<sup>2</sup>.

For sampling, we draw randomly from a set of states (0 to 2^n - 1) with probabilies calculated from the
state vector.

### Tensor simulations

In case of tensor simulations, each row in the tensor is the matrix representation of the corresponding qubit. [q<sub>1</sub>, q<sub>2</sub>, q<sub>3</sub>].

This can simply be converted to a vector state by calculating the Kronecker product of all qubits. Once we get the vector state, we can sample the final states similar to vector state sampling.
