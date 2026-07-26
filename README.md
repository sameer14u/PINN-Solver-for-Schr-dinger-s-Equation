# Physics-Informed Neural Networks

## Solving the Time-Independent Schrödinger Equation (TISE) in 1D

### Problem Statement

Developed a **Physics-Informed Neural Network (PINN)** to solve the 1D Time-Independent Schrödinger Equation for a particle in a box using boundary conditions and energy eigenvalues. The project also explores extending the network to estimate **unknown eigenvalues alongside wavefunctions**.

### Files

* `solve_PDE_NN.ipynb` demonstrates a neural network as a general PDE solver.
* `Pinns_Cp.ipynb` implements a PINN for solving TISE with known boundary conditions and energy eigenvalues.
* `Pinn_multiple_n.ipynb` extends the model to learn solutions across multiple eigenstates.
* `PINN_Presentation.pdf` presents the methodology, results, and eigenvalue-learning extension.

### Methodology

The neural network approximates the wavefunction while incorporating the **Schrödinger equation directly into the loss function**. Automatic differentiation computes the required derivatives, while physics and boundary-condition losses constrain the predicted solution.

### Utility

Once trained, the PINN provides a continuous approximation of the wavefunction and can perform inference at arbitrary spatial points. Unlike grid-dependent numerical approaches, the model can be trained at one spatial discretization and evaluated at different resolutions without retraining.

### Follow-up

For unknown energy eigenvalues, the architecture can be extended to **jointly learn the eigenvalue and wavefunction** by treating energy as a trainable parameter and introducing appropriate normalization, boundary, and physics-based loss constraints.

Contributors : Sameer Choudhary and Arpit.
