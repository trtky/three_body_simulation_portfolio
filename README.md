# Information

- This project computes the positions, velocities, and accelerations of three bodies interacting through Newtonian gravity.  
- The **Velocity–Verlet** integration method is used for stable and accurate time evolution.  
- After the simulation, the trajectories of the bodies are animated, including their motion trails.

---

# Run

- Execute the file `three_body_sim.py`.  
- After the simulation finishes, an animation showing the motion of all bodies will appear.

---

# Results

The following image shows an example result of the simulation:

![result](results/results.png)




# Process of Computation

## Nomenclature

- \( i, j \): indices for the bodies  
- \( t \): current time step  
- \( t+1 \): next time step  

---

## 1. Dynamics

### 1.1 Initial Time Step

- The initial positions and velocities are given.  
- The accelerations are computed using Newton’s law of gravitation.

**Acceleration formula**

![acceleration_formula](formula/acceleration_0.png)

---

### 1.2 Subsequent Time Steps

- Using the current acceleration, compute the new positions at time \( t+1 \).  
- The **Velocity–Verlet** method is used for time integration.

**New position**

![new_position](formula/new_position.png)

- After updating the positions, compute the new accelerations.

![acceleration_formula_2](formula/acceleration_1.png)

- Finally, compute the new velocities at time \( t+1 \).

![new_velocity](formula/new_velocity.png)

---

## 2. Energies

For every time step, the total energy of the system can be computed.

### 2.1 Kinetic Energy

Each body contributes a kinetic energy term:

![kinetic_energies](formula/kinentic_energy.png)

### 2.2 Potential Energy

Each pair of bodies contributes a gravitational potential energy term:

![potential_energies](formula/potential_energy.png)

### 2.3 Total Energy

The total energy is the sum of kinetic and potential energy:

![total_energy](formula/total_energy.png)
