# Quantum Error Correction Using Code Concatenation

## Problem Statement

Quantum error correction protocols play a central role in the realisation of quantum computing as quantum systems are prone to errors due to noise and decoherence. However the Threshold Theorem provides a theoretical background for quantum error correction, it states that it is possible to create a quantum computer to perform an arbitrary quantum computation provided the error rate per physical gate or time step is below some constant threshold value.

This project focuses on implementing a Steane code, which is a form of QEC code based on the 7-qubit code. The challenge lies in concatenating the Steane code with itself multiple times, as this involves managing a large number of qubits. The goal is to compile the quantum circuits after concatenation, draw circuit diagrams for the resulting schemes, and evaluate the error rates for both the single-layer and multi-layer concatenated codes.

## Methods

1. **Implementation of the Steane Code**:
   The Steane code, a 7-qubit quantum error-correcting code, will be implemented using Google Qualtran. This step will involve creating a circuit that encodes logical qubits using the Steane code.

2. **Concatenation of the Steane Code**:
   The Steane code will be concatenated with itself. In this process, logical qubits from one Steane code will be treated as physical qubits for another Steane code, thereby creating a two-level concatenated scheme.

3. **Circuit Diagram Generation and Comparison**:
   Using visualization tools, drawing the circuit diagrams for the original Steane code and the two-level concatenated Steane code will be generated. The diagrams will be compared to analyze how the number of qubits and gates scale with concatenation.

4. **Plotting Logical Error Rates**:
   Calculate logical error rates for the Steane code (without concatenation) by simulating the circuit under various physical error rates. A plot the results to show how the logical error rate depends on the physical error rate for the single-level code.

5. **Analysis of the Concatenated Code Error Rates**:
   For the two-level concatenated Steane code, plot the error rate. This data will then be compared to the Threshold Theorem predictions. If the concatenated scheme suppresses errors as predicted by the theorem, the logical error rate should decrease more rapidly than the physical error rate, given that the physical error rate is below the threshold.

## Expected Results

1. **Implementation of the Steane Code**:
   Successful implementation of the Steane code, leading to a quantum circuit that encodes a logical qubit and protects against single-qubit errors. The circuit should correctly perform logical operations and detect errors.

2. **Concatenation of the Steane Code**:
   The concatenated Steane code is expected to result in a larger circuit with more qubits and gates due to the additional layer of encoding.

3. **Error Rate Behavior**:
   The logical error rate of the single-level Steane code is expected to show a reduction in error rate compared to the physical qubits. When concatenated, the two-level scheme should exhibit even lower logical error rates.

4. **Threshold Theorem Validation**:
   The logical error rates for the two-level concatenated scheme should align with the Threshold Theorem, demonstrating that concatenation of QEC codes effectively reduces error rates when the physical error rate is sufficiently low.

## References

1. A. M. Steane. (1996). Error Correcting Codes in Quantum Theory
2. Google Qualtran Documentation and Tutorials.
3. Andrew Steane. (1996). Multiple Particle Interference and Quantum Error Correction
4. Simon J. Devitt, Kae Nemoto, William J. Munro. (2013). Quantum Error Correction for Beginners
