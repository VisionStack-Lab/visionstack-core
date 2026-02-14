# VisionStack Core

### Robotics & Intelligent Systems Foundations Lab

VisionStack Core is the foundational research repository for **VisionStack Lab** — a long-term robotics and intelligent systems initiative focused on dynamics, control, perception, planning and learning.

This repository is designed as a structured, simulation-driven robotics laboratory that runs entirely in the cloud. It emphasises mathematical modelling, system architecture and engineering discipline before hardware deployment.

The objective is to build deep computational foundations that scale from undergraduate study through to advanced research.

---

## Philosophy

Robotics is not hardware first. It is:

* Dynamics
* Feedback control
* State estimation
* Planning under constraints
* Learning in uncertain environments

Hardware validates. Simulation explains.

This repository is structured to reflect a real robotic system architecture:

* Physics layer
* Control layer
* Estimation layer
* Planning layer
* Learning layer

---

## Repository Structure

```
visionstack-core/
├── docs/
│   ├── theory-notes/
│   └── project-reports/
├── configs/            
├── models/             
├── src/
│   ├── main.py
│   ├── common/         
│   ├── dynamics/       
│   ├── control/        
│   ├── estimation/     
│   ├── planning/       
│   ├── rl/             
│   └── hardware/
├── experiments/
├── results/
│   ├── plots/
│   └── logs/
├── tests/
├── .gitignore          
├── requirements.txt
└── README.md

```

---

## Directory Overview

### docs/

Contains structured written material.

* `theory-notes/` — mathematical foundations and conceptual explanations
* `project-reports/` — technical documentation for each major system

This section develops research clarity and technical communication.

---

### src/

Core implementation code organised by system layer.

#### common/

Shared utilities such as plotting functions, constants and helper modules.

#### dynamics/

Mathematical models of physical systems:

* DC motor
* Mass-spring-damper
* Inverted pendulum

#### control/

Controllers separated from plant models:

* PID
* State feedback
* LQR

#### estimation/

State estimation and perception algorithms:

* Kalman filter
* 2D localisation

#### planning/

Decision and navigation algorithms:

* A*
* Grid world simulation

#### rl/

Reinforcement learning implementations:

* Custom CartPole environment
* Q-learning
* Policy gradient

---

### experiments/

Temporary experimental scripts used for:

* Parameter tuning
* Controller comparison
* Simulation demonstrations

Experimental code does not belong inside `src/`.

---

### results/

Generated outputs only.

* `plots/` — simulation graphs
* `logs/` — experiment logs

Source code must remain separate from output artefacts.

---

### tests/

Basic validation scripts for controllers and algorithms.

Engineering discipline requires verification, even in simulation.

---

## Cloud Architecture

VisionStack Core is designed to run on distributed cloud infrastructure.

### Oracle Cloud (Primary Research Node)

Used for:

* Full simulations
* Larger experiments
* Structured project execution
* Long-running processes

### Azure VM (Development Node)

Used for:

* Lightweight prototyping
* Algorithm testing
* Rapid iteration

GitHub serves as the central coordination layer between environments.

---

## Phase Roadmap (First 12 Weeks)

### Phase 1 — Dynamics & Feedback

* DC motor modelling
* PID control
* Mass-spring-damper simulation

### Phase 2 — State-Space & Estimation

* Inverted pendulum
* State feedback and LQR
* Kalman filtering
* 2D robot localisation

### Phase 3 — Planning & Learning

* A* path planning
* Grid-based navigation
* Reinforcement learning fundamentals

Each phase must include:

* Clean modular code
* Mathematical documentation
* Simulation plots
* Technical report

---

## Technical Stack

* Python 3
* NumPy
* SciPy
* Matplotlib
* control
* scikit-learn
* PyTorch (CPU only)

Designed to run on lightweight cloud instances (1–4 GB RAM).

---

## Long-Term Vision

VisionStack Core is the computational backbone of VisionStack Lab.

Future expansions may include:

* Sensor fusion
* SLAM
* Multi-robot systems
* Advanced perception models
* Embedded deployment
* Hardware validation

The structure is designed to scale from foundational simulation to advanced research.

---

## Engineering Principles

* Separate plant and controller
* Separate model and experiment
* Separate code and results
* Document assumptions
* Validate behaviour
* Optimise clarity over complexity

This repository is a research laboratory in development.
