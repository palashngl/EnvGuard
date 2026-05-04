<p align="center">
  <img src="assets/envguard_banner.svg" alt="EnvGuard Banner" width="100%">
</p>

# EnvGuard: Environment-Centric Risk-Aware Robot Navigation

**Paper Title:** *Seeing Danger Before Moving: Learning Environment-Centric Risk for Safe Robot Navigation*  

**Repository:** https://github.com/palashngl/EnvGuard.git

---

## Status

This repository is currently being prepared for public release.

The paper description, project overview, and documentation are available now.  
The complete source code, trained models, configuration files, datasets, and experiment scripts will be uploaded soon after final cleanup, verification, and organization.

> **Note:** The implementation is under active preparation. Please check back for updates.

---

## Overview

EnvGuard is an **environment-centric risk-aware robot navigation framework** designed for autonomous robots operating in hazardous environments.

Traditional robot navigation systems mainly depend on onboard perception. This means the robot often detects danger only when it is already close to or inside a hazardous region. EnvGuard addresses this limitation by using the **environment itself** as the main source of hazard perception.

The system uses infrastructure-mounted cameras and distributed environmental sensors to estimate navigation risk before the robot enters unsafe areas. These risk observations are fused, filtered over time using a Bayesian latent risk belief, and converted into a risk-aware costmap for safe navigation planning.

---

## Key Idea

EnvGuard allows a robot to **see danger before moving into it**.

The main pipeline is:

```text
Environment-Mounted Cameras + Sensors
                |
                v
Multimodal Risk Encoder
                |
                v
Instantaneous Risk Observation
                |
                v
Bayesian Latent Risk Belief
                |
                v
Risk Costmap
                |
                v
Risk-Aware Planner
                |
                v
Safer Robot Navigation
```

The robot itself does not perform hazard perception.  
It uses onboard sensing only for localization and motion execution.

---

## Main Features

- Environment-centric hazard perception
- Infrastructure-mounted camera and sensor fusion
- Multimodal visual and sensory risk estimation
- Bayesian latent risk belief filtering
- Risk-aware costmap generation
- Proactive path replanning before hazard exposure
- Physical rover validation in a multi-hazard testbed
- Real-time navigation pipeline

---

## Sensor Modalities

EnvGuard can integrate environmental observations from:

- RGB-D cameras
- Smoke sensors
- Temperature sensors
- Flame sensors
- Water sensors
- Gas sensors
- Vibration sensors
- Tilt sensors

These observations are used to estimate the evolving risk state of the environment.

---



## Experimental Highlights

EnvGuard was evaluated using a real physical rover in a controlled multi-hazard testbed.

The testbed included:

- multiple candidate paths,
- dynamically activated hazards,
- distributed environmental sensors,
- environment-mounted cameras,
- physical rover traversal experiments,
- online replanning events.




---

## Repository Structure

The repository will be organized as follows:

```text
EnvGuard/
├── README.md
├── assets/
│   └── envguard_banner.svg
├── paper/
│   └── EnvGuard.pdf
├── figures/
│   ├── architecture/
│   ├── testbed/
│   └── results/
├── src/
│   ├── perception/
│   ├── belief_filter/
│   ├── planning/
│   └── utils/
├── scripts/
│   ├── run_perception.py
│   ├── run_bayesian_filter.py
│   └── run_planner.py
├── configs/
│   └── envguard.yaml
├── data/
│   ├── sensor_logs/
│   ├── risk_maps/
│   └── trajectories/
└── requirements.txt
```

---

## Code Release

The following files will be uploaded soon:

- complete source code,
- trained model weights,
- sensor log examples,
- risk map examples,
- trajectory data,
- configuration files,
- setup instructions,
- reproduction scripts,
- additional figures and videos.

---

## Installation

The full installation guide will be added after the code release.

Expected setup:

```bash
git clone https://github.com/palashngl/EnvGuard.git
cd EnvGuard
```

The requirements file and environment setup instructions will be provided soon.

---

## Usage

Usage instructions will be updated after the code is uploaded.

Expected execution format:

```bash
python scripts/run_perception.py --config configs/envguard.yaml
python scripts/run_bayesian_filter.py --config configs/envguard.yaml
python scripts/run_planner.py --config configs/envguard.yaml
```

---

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{ingle2025envguard,
  title     = {Seeing Danger Before Moving: Learning Environment-Centric Risk for Safe Robot Navigation},
  author    = {Ingle, Palash Yuvraj and Kim, Young-Gab},
  booktitle = {Robotics: Science and Systems},
  year      = {2025}
}
```

---


## License

The license will be updated soon.

Until the official release, please do not redistribute unpublished code, data, or models without permission.


