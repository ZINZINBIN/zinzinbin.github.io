---
title: "Computational Plasma Physics"
layout: single-portfolio
excerpt: "<img src='/images/research/PIC.gif' alt=''>"
collection: research
order_number: 50
header: 
  og_image: "research/PIC.gif"
---

## Introduction
This research implements the symplectic integration with the PIC method to simulate the kinetics of the plasma while preserving the Hamiltonian of the system. We cover a one-dimensional periodic system with an electrostatic plasma, where the effect of the induced magnetic field is ignored. This allows us to cover the one-dimensional Vlasov-Poisson equation, a simplified equation of the Vlasov-Maxwell equation. For small-scale simulations, we consider the electron motions only while the ions are assumed to be fixed. Our numerical experiments are a two-stream instability in which two electron beams in different directions are injected, and a bump-on-tail instability where the high-energy electron perturbation is added in the thermalized electron plasma. The external perturbation applied to the system induces the plasma-wave interaction and results in a shape of a separatrix in a phase-velocity space of the system and reaches a new equilibrium of the velocity distribution where the quasi-linear diffusion can be observed.

## Vlasov-Poisson Plasma System
Plasma can be treated as an electric fluid that contains particle interactions (collision) and field-particle interactions. The motion of the plasma induces a change in the distribution of charged particles, which generates electromagnetic fields and affects the motion again. The self-consistent behaviors of the fields and particles can be described by integrating the fluid and Maxwell’s equations, which allows us to understand the dynamics of a continuous medium interacting with fields. Below slide describes the governing equations of the plasma system.

<img src="/images/research/computational-plasma-physics/Plasma-system.png"  width="100%">

## Symplectic Particle In Cell Method
Particle-In-Cell method is a particle-mesh coupling method for solving equations of motion in kinetic systems. The main concept of this method is to separate the particle coordinate and mesh coordinate for electromagnetic fields. While a Lagrangian frame to track the particles in phase space is applied on the particle coordinate, the physical quantities like densities and fields are approximated on a coarse mesh coordinate, which allows the reduction of the computational cost for solving Maxwell’s equations. Below slide describes the concept of PIC. 

<img src="/images/research/computational-plasma-physics/PIC-1.png"  width="100%">

Note that there is an interpolation process that maps the field computed on the mesh coordinate to the particle coordinate. For each iteration, the field solver calculates E and B on a mesh grid, and the interpolated fields are applied to update the state of the particles. Although PIC is easy to implement and enables a low computational cost for field calculation, the dissipation of the Hamiltonian is a problem since a general explicit time integration method cannot preserve the Hamiltonian structure for a long timescale simulation. Thus, we utilize the symplectic integration known as a 2nd-order Verlet method (Leapfrog). The details for developing the symplectic PIC code are described as below.

<img src="/images/research/computational-plasma-physics/PIC-implementation.png"  width="100%">

## Numerical Result
The numerical simulation for the two-stream instability is represented as below and the attached file below. Our code can simulate not only the phase trajectory but also the time-evolving distribution of the particles. The formation of the separtrix with the energy preservation can be observed with different mode numbers. 

<img src="/images/research/computational-plasma-physics/PIC_simulation.gif"  width="100%">

You can see the details at the attached files.

## Article
Jinsu Kim. "Symplectic Particle-In-Cell Method for 1-Dimensional Vlasov-Poisson Plasma System" [Draft](/files/Symplectic-PIC.pdf).

## Presentation
<iframe src="/files/Symplectic-PIC-ppt.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>