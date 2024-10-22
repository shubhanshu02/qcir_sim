# qcir_sim

Quantum circuit simulation using Vector and Tensor simulations

**Note:** Examples for using are provided in the `examples/` folder. Examples include:

1. Benchmarking how many qubits can we simulate using Vector and Tensor simulation
2. Sampling the Qubits from a Quantum simulation
3. Calculating the expectation values of `<Ψ| Op |Ψ>`

## Setting up

### Using uv ([Installation](https://docs.astral.sh/uv/getting-started/installation/))

1. Create a virtual environment

```sh
uv venv .venv
```

2. Activate the virtual environment

```sh
source .venv/bin/activate
```

3. Install the dependencies

```sh
uv sync
uv pip install pandas # required in benchmark.py
```

### Legacy virtual environments

1. Create virtual environment

```sh
python3 -m venv .venv
```

2. Activate the virtual environment

```sh
source .venv/bin/activate
```

3. Install dependencies

```sh
pip install -e . # -e to develop while using
```
