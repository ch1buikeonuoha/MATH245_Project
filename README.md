# MATH245_Project
This project investigates the spread of COVID-19 using compartmental epidemic models. The work was completed as part of MATH245a/b/c (2025/26) – Final Project 1 and explores numerical and analytical solutions of infectious disease models using Python.

The project focuses on:

The Susceptible–Infectious–Removed (SIR) model
Numerical solution using Euler's method
Comparison with exact analytical solutions
Error analysis and convergence
Parameter sensitivity studies
Extension to an SIRV (Susceptible–Infectious–Removed–Vaccinated) model
Impact of vaccination on disease transmission
Mathematical Models
SIR Model
The classical SIR model is defined by

[ \frac{dx}{dt} = -\beta xy ]

[ \frac{dy}{dt} = \beta xy - \gamma y ]

where:

(x) = fraction of susceptible individuals
(y) = fraction of infectious individuals
(\beta) = infection transmission rate
(\gamma) = recovery/removal rate
The removed compartment is given by:

[ R = 1 - x - y ]

SIRV Model
The vaccination model extends SIR by adding a vaccinated compartment (v):

[ \frac{dx}{dt} = -\beta xy - \mu x ]

[ \frac{dy}{dt} = \beta xy - \gamma y ]

[ \frac{dv}{dt} = \mu x ]

where:

(v) = vaccinated population fraction
(\mu) = vaccination rate
Project Structure
Features
Question 1
Implements Euler's method for solving the SIR system.
Generates simulation results as a Pandas DataFrame.
Compares numerical results with known analytical solutions.
Question 2
Investigates numerical error.
Plots the difference between Euler approximations and exact solutions.
Studies the effect of timestep size.
Question 3
Explores model behaviour under varying transmission and recovery rates.
Visualizes epidemic trajectories.
Question 4
Implements an SIRV model with vaccination.
Solves the system using SciPy's odeint.
Compares Euler and ODE solver solutions.
Examines vaccination strategies and their effect on infection levels.
Technologies Used
Python
NumPy
Pandas
SciPy
Plotnine (ggplot-style visualization)
Quarto
Installation
Install the required packages:

pip install numpy pandas scipy plotnine quarto
