# Modeling Lorenz Dynamics with VAEs and GANs

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Topic](https://img.shields.io/badge/Topic-Applied%20Mathematics-orange)
![Framework](https://img.shields.io/badge/Framework-Deep%20Learning-red)

This repository documents a research and computational modeling project focused on the simulation and analysis of the chaotic Lorenz system using deep generative machine learning architectures. It explores the intersection of chaos theory and deep learning by training networks to learn, reconstruct, and generate complex continuous phase-space trajectories.

---

## 📌 Project Overview
* **Mentee:** Bismah Zafar
* **Mentor:** Su Hyeong Lee
* **Program:** Twoples Mentorship Programme

The goal of this project is to evaluate how effectively generative models can capture the underlying physical laws and geometric structures of a chaotic mathematical system without relying on explicit differential equation solvers during inference.

---

## 🪐 Mathematical Background: The Lorenz System
The Lorenz system is a system of three coupled, non-linear ordinary differential equations (ODEs) developed by Edward Lorenz in 1963 to model atmospheric convection. It defines how the state variables evolve over time:

$$\frac{dx}{dt} = \sigma (y - x)$$
$$\frac{dy}{dt} = x (\rho - z) - y$$
$$\frac{dz}{dt} = xy - \beta z$$

### System Parameters & Chaos:
To induce classic chaotic behavior, the standard system parameters are defined as:
* **$\sigma$** (Prandtl number) = $10$
* **$\rho$** (Rayleigh number) = $28$
* **$\beta$** (Geometric factor) = $8/3$

These parameters yield a fractal structure known as a **strange attractor** (the famous butterfly shape) where trajectories converge, illustrating an extreme sensitivity to initial conditions (the butterfly effect).

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


<p align="center">
  <img width="576" height="581" alt="image" src="https://github.com/user-attachments/assets/763b4ef4-5be5-4afb-ae7a-cbfd8d09cf63" />

  <img width="968" height="470" alt="image" src="https://github.com/user-attachments/assets/445118cc-624b-43ab-9b37-daa1a8ed79c2" />

  <img width="644" height="658" alt="image" src="https://github.com/user-attachments/assets/f5c92271-cab2-4e9b-8db0-6bd25f77d071" />

  <img width="1432" height="460" alt="image" src="https://github.com/user-attachments/assets/9fb3ce45-a9fa-43f8-99ce-6498f1fcae51" />

  <img width="1486" height="547" alt="image" src="https://github.com/user-attachments/assets/4b5dea56-d97c-4202-8cb7-1221aa4503ba" />
  
</p>
