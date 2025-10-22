
# QOSF Mentorship Program - Task 2 Submission

**Name:** Kristian Koci
**Date:** October 21, 2025  
**Task:** Task 2 - Arbitrary Quantum State Preparation

----------

## My Approach

I'm submitting Task 2: Arbitrary State Preparation using the Möttönen decomposition. Rather than attempting multiple tasks, I chose to focus on understanding one algorithm deeply.

The QOSF guidelines mention that submitting more tasks doesn't improve selection chances, so I decided to prioritize depth over breadth. State preparation seemed like a good choice because it's fundamental - it comes up in quantum machine learning, simulation, and algorithm initialization.

----------

## What I Built

I implemented the Möttönen algorithm from scratch using only NumPy. The algorithm prepares arbitrary quantum states through a two-phase process:

1.  Magnitude preparation using RY rotations
2.  Phase preparation using RZ rotations

The implementation includes:

-   Basic quantum state representation and gates
-   Multi-qubit operations via tensor products
-   Circuit simulator
-   Multi-controlled gate decomposition
-   Fidelity calculations for testing

I tested it on several quantum states including Bell states, GHZ, W state, and random states with complex phases. All tests achieved fidelity above 0.9999.

----------

## Why From Scratch?

I chose to build everything from scratch (without Qiskit or other quantum libraries) because I wanted to understand the underlying mathematics. It's easier to use a library function, but working through tensor products and gate decomposition yourself forces you to really understand what's happening.

It took longer this way, but I learned more about how quantum circuits actually work at the matrix level.

----------

## What I Learned

**The binary tree structure is clever.** The way Möttönen processes qubits level by level, with control patterns coming from binary representations, makes the algorithm systematic and elegant.

**Complexity is inherent.** The O(n²·2ⁿ) gate count initially seemed concerning, but makes sense given that we're setting 2ⁿ complex amplitudes. The exponential part is unavoidable. The n² overhead comes from my multi-controlled gate decomposition approach.

**Implementation matters.** Small details like handling zero amplitudes, numerical precision, and proper normalization all matter when building from scratch.

----------

## Limitations

My multi-controlled gate decomposition works but isn't optimal - better decompositions exist that would reduce gate count. I also didn't implement sparse state optimizations, so the algorithm processes all 2ⁿ amplitudes even when many are zero.

The circuits would need transpilation and error mitigation for real quantum hardware.

----------

## Why QOSF?

I'm applying to QOSF because I want to work on quantum computing projects with guidance from experienced researchers. I'm particularly interested in quantum algorithms and would like to contribute to open-source quantum software.

I can commit 10-15 hours per week to the mentorship project and am comfortable with remote collaboration and version control.

----------

## Technical Summary

**Implementation:** Jupyter notebook, NumPy only  
**Testing:** 8+ quantum states, all with fidelity > 0.9999  
**Documentation:** Inline comments and markdown explanations  
**Verified on:** qBraid platform

I'm available for technical discussions about the implementation and happy to walk through any part of the code.

----------

## Submitted Files

-   `task2_state_preparation_mottonen.ipynb` - Main implementation
-   `README.md` - Technical documentation
-   `COVER_LETTER.md` - This letter

----------

Thank you for considering my application. I look forward to the opportunity to learn through the QOSF mentorship program.

Kristian 
