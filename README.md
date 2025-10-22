
# Task 2: Möttönen State Preparation - From Scratch

**QOSF Mentorship Program Screening Task**

## Overview

Complete implementation of the Möttönen decomposition algorithm for arbitrary quantum state preparation. Built entirely from scratch using only NumPy—no quantum computing libraries.

## What's Inside

-   **Complete Möttönen Algorithm**: Both magnitude and phase preparation
-   **Full Quantum Simulator**: States, gates, circuits built from first principles
-   **Comprehensive Testing**: 8+ quantum states including Bell, GHZ, and W states
-   **High Fidelity Results**: All tests achieve >99.99% fidelity
-   **Complexity Analysis**: Empirical verification of O(n²·2ⁿ) gate count
-   **Clear Visualizations**: Probability and phase distributions
-   **Well Documented**: Inline explanations and mathematical foundations

## Key Features

✅ Arbitrary n-qubit state preparation  
✅ Systematic binary tree decomposition  
✅ Multi-controlled gate synthesis  
✅ Tensor product operations from scratch  
✅ Tested and validated on qBraid

## Implementation Highlights

-   **NumPy only**: No Qiskit, Cirq, or other quantum libraries
-   **Reference**: Möttönen et al., PRL 93.13 (2004): 130502
-   **Test Coverage**: 1-qubit, 2-qubit, and 3-qubit states with complex phases
-   **Code Quality**: Clean, documented, and reproducible

## Quick Start

```python
# Define target state (e.g., Bell state)
amplitudes = [1/np.sqrt(2), 0, 0, 1/np.sqrt(2)]

# Prepare using Möttönen algorithm
prep = MottoneStatePreparation(amplitudes)
circuit = prep.prepare_state()

# Verify fidelity
prepared = circuit.get_quantum_state()
target = QuantumState(amplitudes)
fidelity = target.fidelity(prepared)  # > 0.9999

```

## Results

State

Qubits

Fidelity

Status

Bell |Φ+⟩

2

0.9999999999

✓ PASS

GHZ

3

0.9999999999

✓ PASS

W State

3

0.9999999998

✓ PASS

## Structure

```
task2_state_preparation_mottonen.ipynb  # Main implementation
├── Part 1: Quantum State Representation
├── Part 2: Quantum Gates (I, X, Z, H, RY, RZ)
├── Part 3: Quantum Circuit Simulator
├── Part 4: Möttönen Algorithm
├── Part 5: Comprehensive Testing
├── Part 6: Visualization
├── Part 7: Complexity Analysis
└── Part 8: Custom State Preparation

```

## Dependencies

```
numpy >= 1.20.0
matplotlib >= 3.3.0

```

## Running

Tested on:

-   Python 3.8+
-   qBraid quantum computing platform
-   Jupyter Notebook

Simply run all cells in order—fully reproducible with seed set.

## Author

Created for QOSF Mentorship Program application.

Demonstrates understanding of:

-   Quantum state manipulation
-   Algorithm implementation from research papers
-   Tensor products and unitary operations
-   Multi-qubit gate decomposition
-   Systematic testing and validation

----------

_Built from scratch to show foundational understanding rather than library familiarity._
