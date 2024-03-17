[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/wcamb/)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/wcambiuc)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@waldemircambiucci)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/waldemircambiucci/)

Author: Waldemir Cambiucci
Update: March 2024

# TOOLS - PYTHON-CIRCUITS-DIMENSIONS

Below is a Python code example using Qiskit to explore classical dimensions such as size, depth, and width of a quantum circuit. We'll also calculate the number of operations involved in the circuit:

```python
from qiskit import QuantumCircuit
from qiskit.visualization import plot_circuit_layout, plot_histogram
from qiskit.transpiler import PassManager
from qiskit.transpiler.passes import Unroller

def explore_classical_dimensions(circuit):
    # Size
    size = circuit.size()

    # Depth
    depth = circuit.depth()

    # Width
    width = circuit.width()

    # Number of Operations
    num_operations = len(circuit.data)

    return size, depth, width, num_operations

# Example: Creating a 3-qubit quantum circuit
qc = QuantumCircuit(3)

# Applying gates to create a simple circuit
qc.h(0)
qc.cx(0, 1)
qc.cx(1, 2)
qc.measure_all()

# Explore classical dimensions
size, depth, width, num_operations = explore_classical_dimensions(qc)

# Print the results
print("Size of the circuit:", size)
print("Depth of the circuit:", depth)
print("Width of the circuit:", width)
print("Number of operations in the circuit:", num_operations)

# Visualize the circuit
print("\nVisualizing the circuit:")
qc.draw('mpl')
```

This code creates a simple quantum circuit with three qubits and explores its classical dimensions using the `explore_classical_dimensions` function. We then print the results and visualize the circuit using Qiskit's `draw` function.

Make sure you have Qiskit installed (`pip install qiskit`). This code snippet provides a basic example of how to explore classical dimensions of a quantum circuit using Python and Qiskit. You can modify the circuit and explore other dimensions as needed for your application.
