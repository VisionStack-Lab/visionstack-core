# VisionStack Core

### Robotics & Intelligent Systems Foundations Lab

VisionStack Core is the foundational computational backbone of **VisionStack Lab** — a long-term robotics and intelligent systems initiative focused on building efficient, effective and reliable autonomous systems.

This repository is a structured, simulation-driven robotics laboratory designed to develop deep foundations in:

* Physical system modelling
* Feedback control
* State estimation
* Planning and decision systems
* Learning-based adaptation

The architecture is intentionally modular and reproducible, preparing systems for eventual deployment into UAVs, UUVs, autonomous vehicles and miniaturised embedded platforms.

---

## Philosophy

Robotics is not hardware first. It is:

* Dynamics
* Feedback
* Estimation under uncertainty
* Structured decision-making
* Intelligent adaptation

Hardware validates. Simulation explains.

VisionStack Core reflects a layered robotic architecture:

1. Physical modelling (plant dynamics)
2. Control systems
3. State estimation
4. Planning and navigation
5. Learning systems
6. Hardware abstraction

Each layer is modular, testable and independently verifiable.

---

## Repository Structure

```
visionstack-core/
├── docs/
│   ├── theory-notes/          # Mathematical foundations and conceptual explanations
│   └── project-reports/       # Technical documentation for each major project
│
├── configs/                   # Configuration files for reproducible experiments
│
├── models/                    # Saved trained models and serialised artefacts
│
├── src/
│   ├── main.py                # System orchestration and execution entry point
│   │
│   ├── common/                # Shared utilities (plotting, constants, helpers)
│   │
│   ├── dynamics/              # Physical system models (plants)
│   │
│   ├── control/               # Controllers (PID, LQR, state feedback, etc.)
│   │
│   ├── estimation/            # Filtering and localisation algorithms
│   │
│   ├── planning/              # Path planning and decision algorithms
│   │
│   ├── rl/                    # Reinforcement learning modules and environments
│   │
│   └── hardware/              # Hardware abstraction and deployment interfaces
│
├── experiments/               # Exploratory scripts and parameter tuning
│
├── results/
│   ├── plots/                 # Simulation visualisations
│   └── logs/                  # Experiment logs and outputs
│
├── tests/                     # Unit tests and validation scripts
│
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Architectural Principles

### Configuration-Driven Execution

All experiments should be parameterised via files in `configs/`.

System parameters, noise matrices, controller gains, and simulation durations must not be hardcoded. This ensures:

* Reproducibility
* Experiment traceability
* Clear separation of logic and configuration

---

### Modular Layer Separation

* `dynamics/` defines physical systems only.
* `control/` interacts with plants but does not alter their internal structure.
* `estimation/` operates under measurement uncertainty and does not access ground truth directly.
* `planning/` makes decisions based on estimated state.
* `rl/` implements learning-based policies.
* `hardware/` provides a clean interface between software and real-world devices.

No cross-layer shortcuts are permitted.

---

### Orchestration via `main.py`

`main.py` is responsible for:

* Loading configuration files
* Initialising system components
* Running simulations or training sessions
* Managing output storage

It coordinates modules but does not contain core logic.

---

## Directory Overview

### docs/

Contains structured written material.

* `theory-notes/` — mathematical derivations and conceptual foundations
* `project-reports/` — experiment results, system analysis and conclusions

Clear documentation is treated as part of engineering discipline.

---

### configs/

Configuration files (YAML or JSON) defining:

* Physical parameters
* Noise characteristics
* Controller gains
* Simulation time horizons
* Training hyperparameters

This enables controlled experimentation.

---

### models/

Stores:

* Trained neural network weights
* Learned policies
* Serialised estimators
* Saved parameter sets

This directory contains artefacts, not definitions.

---

### experiments/

Exploratory scripts for:

* Parameter sweeps
* Controller comparisons
* Behaviour analysis

Code here may be temporary but should remain structured.

---

### results/

Generated outputs only.

* `plots/` — simulation figures
* `logs/` — experiment output data

Source code and generated artefacts remain strictly separated.

---

### tests/

Validation scripts for:

* Controller stability
* Estimator correctness
* Algorithm behaviour

Verification is mandatory, even in simulation.

---

## Cloud Architecture

VisionStack Core operates on a distributed development model.

### Oracle Cloud — Primary Research Node

Used for:

* Structured simulations
* Larger experiments
* Learning-based training
* Long-running processes

### Azure VM — Development Node

Used for:

* Rapid prototyping
* Algorithm iteration
* Lightweight testing

GitHub serves as the central coordination backbone across environments.

---

## 12-Week Foundational Roadmap

### Phase 1 — Dynamics & Feedback

* DC motor modelling
* PID control design
* Mass-spring-damper simulation

### Phase 2 — State-Space & Estimation

* Inverted pendulum modelling
* State feedback and LQR
* Kalman filtering
* 2D localisation under noise

### Phase 3 — Planning & Learning

* A* path planning
* Grid-based navigation
* Reinforcement learning fundamentals

Each project must include:

* Clean modular implementation
* Configuration-driven execution
* Mathematical documentation
* Simulation visualisation
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

Designed for efficient execution on lightweight cloud infrastructure.

---

## Long-Term Direction

VisionStack Core is built to evolve toward:

* Sensor fusion
* SLAM
* Autonomous navigation systems
* Embedded deployment
* UAV, UUV and ground vehicle integration
* Reliability-focused intelligent control architectures

The architecture is intentionally scalable from simulation to field deployment.

---

## Engineering Commitments

* Separate plant and controller
* Separate model and artefact
* Separate configuration and logic
* Separate source and output
* Validate behaviour before optimisation
* Design for reliability, not demonstration

VisionStack Core is not a collection of scripts.

It is the computational foundation of a long-term robotics and intelligent systems programme.
