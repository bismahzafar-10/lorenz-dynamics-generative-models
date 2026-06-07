# Modeling Lorenz Dynamics with VAEs and GANs

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Topic](https://img.shields.io/badge/Topic-Applied%20Mathematics-orange)
![Framework](https://img.shields.io/badge/Framework-Deep%20Learning-red)

This repository documents a research and computational modeling project focused on the simulation and analysis of the chaotic Lorenz system using deep generative machine learning architectures. It explores the intersection of chaos theory and deep learning by training networks to learn, reconstruct, and generate complex continuous phase-space trajectories.

---

## 📌 Project Overview

**Objective:** Explore and determine which model more effectively captures the dynamics of the Lorenz system.

**Methodology:**
            ◉ Data Generation: Generated Lorenz system data numerically for model training.
            ◉ VAE Implementation: Developed a VAE model that encodes the Lorenz system in a compact latent space, optimized with reconstruction and KL divergence losses.
            ◉ GAN Implementation: Created a GAN with a generator producing Lorenz-like samples from random noise and a discriminator distinguishing between real and generated data.
            ◉ Comparative Analysis: Analyzed both models based on their fidelity to the Lorenz attractor and stability of generated outputs.

**Expected Outcome:** 
The goal of this project is to evaluate how effectively generative models can capture the underlying physical laws and geometric structures of a chaotic mathematical system without relying on explicit differential equation solvers during inference. This work reflects the exciting intersection of mathematics and AI, and it has been a deeply enriching experience under Su Hyeong Lee’s mentorship.

---

## 🪐 Mathematical Background: The Lorenz System

The Lorenz system is a set of three ordinary differential equations originally developed by Edward Lorenz in 1963 to model atmospheric convection. It is notable for its chaotic solutions and has become a classic example in the study of dynamical systems and chaos theory. The equations describe how the state of the system evolves over time and are given by:


$$\frac{dx}{dt} = \sigma (y - x)$$
$$\frac{dy}{dt} = x (\rho - z) - y$$
$$\frac{dz}{dt} = xy - \beta z$$

where:
- x, y, and z represent the state variables of the system.
- 𝜎 is the Prandtl number, which relates to the fluid properties (10).
- 𝜌 is the Rayleigh number, which represents the temperature difference driving convection (28).
- 𝛽 is a geometric factor (8/3).


 **Chaos**: The Lorenz system exhibits sensitive dependence on initial conditions, meaning that small changes in the initial state can lead to vastly different outcomes. This property is often illustrated by the "butterfly effect."

**Strange Attractors**: The system has a particular type of solution called a strange attractor, which is a fractal structure that the trajectories of the system converge to in the phase space.



---

## 🛠️ Project Pipeline

### 1. Data Generation & Preprocessing
* **Numerical Integration:** Generated continuous 3D coordinate trajectories $(x, y, z)$ by solving the non-linear ODEs using numerical integration methods (Runge-Kutta method) over time.
* **Normalization:** Scaled and normalized the sequential time-series data to ensure training stability for the neural networks.

### 2. Generative Modeling
The project implements two distinct classes of Deep Generative Models to capture the continuous chaotic trajectories:
* **Variational Autoencoders (VAEs):** Used to map continuous Lorenz sequences into a compressed, low-dimensional latent space, ensuring smooth latent distributions while reconstructing complex temporal trajectories.
* **Generative Adversarial Networks (GANs):** Employs an adversarial framework—training a generator network against a discriminator network—to synthesize entirely new, physically plausible chaotic phase-space paths that mimic the true system dynamics.

---

## 💻 Tech Stack & Tools
* **Language:** Python
* **Mathematical Tools:** Numerical ODE Integration (Runge-Kutta), Data Normalization
* **Architectures:** Variational Autoencoders (VAEs), Generative Adversarial Networks (GANs)

---

## 🚀 How to Run the Notebook

1. Clone this repository to your local machine:
```bash
git clone https://github.com/bismahzafar-10/lorenz-dynamics-generative-models.git

```
2. Open Jupyter Notebook or Google Colab and upload the .ipynb file.

3. Run the cells step-by-step to visualize the data generation and model training.

---

### 📊 Model Performance & Simulation Results

<p align="center">
  <img src="https://github.com/user-attachments/assets/763b4ef4-5be5-4afb-ae7a-cbfd8d09cf63" width="45%" alt="Lorenz Attractor Plot" />
</p>


VAE for Lorenz Dynamics

<p align="center">
  <img src="https://github.com/user-attachments/assets/445118cc-624b-43ab-9b37-daa1a8ed79c2" width="90%" alt="Trajectory Comparison" />
</p>

GAN for Lorenz Dynamics

<p align="center">
<img src="https://github.com/user-attachments/assets/f5c92271-cab2-4e9b-8db0-6bd25f77d071" width="45%" alt="Phase Space Reconstruction" />
</p>

Comparative Analysis


<p align="center">
  <img src="https://github.com/user-attachments/assets/9fb3ce45-a9fa-43f8-99ce-6498f1fcae51" width="90%" alt="VAE Loss Curves" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/4b5dea56-d97c-4202-8cb7-1221aa4503ba" width="90%" alt="GAN Generated Samples" />
</p>
