# Enhancing Road Safety with V2V Simulations using SUMO

This project explores the use of Vehicle-to-Vehicle (V2V) communication and reinforcement learning to actively enhance road safety. By leveraging shared information from nearby vehicles, our system aims to reduce collisions and traffic jams through intelligent decisions such as changing speed, lanes, and routes.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Environment](#environment)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Demo](#demo)
- [Reference](#reference)
- [License](#license)

## Overview

Modern transportation systems face challenges like congestion and accidents, often due to limited interaction between vehicles. This project demonstrates how V2V communication, combined with Deep Q-Network (DQN) reinforcement learning, can create safer and more efficient traffic environments. All simulations are conducted using [SUMO (Simulation of Urban MObility)](https://sumo.dlr.de/docs/index.html).

## Features

- **V2V Communication:** Vehicles share state information to collaboratively avoid collisions and traffic jams.
- **Reinforcement Learning:** Uses Deep Q-Network (DQN) to optimize driving decisions.
- **Dynamic Control:** Real-time actions for speed, lane changes, and rerouting.
- **Customizable Simulation:** Easily modify network, routes, and vehicle parameters.

## Environment

- **SUMO:** An open-source traffic simulation suite.
- **Python:** Main programming language for simulation and model training.
- **PyTorch:** For implementing the DQN model.

## Project Structure

```
├── run.py               # Controller: manages training episodes and replay memory batch size
├── Simulation.py        # Simulation logic: vehicle loading, state extraction, action execution, reward calculation
├── DQNModeltorch.py     # DQN model: neural network definition, learning rate, reward structure
├── demo2.net.xml        # Network file: defines edges (roads), junctions, and connections
├── demo2.rou.xml        # Route file: defines vehicle routes, numbers, and arrival lanes
├── demo2.sumocfg        # SUMO configuration: visualization and simulation settings
├── requirements.txt     # Python dependencies
├── demos/               # Demo outputs and visualizations
└── README.md            # Project documentation
```

## Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/DivyaSri973/V2VSimulationsUsingSumo.git
    cd V2VSimulationsUsingSumo
    ```

2. **Install Python dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Install SUMO**
    - Follow the [SUMO installation guide](https://sumo.dlr.de/docs/Installing/index.html) for your operating system.

## Usage

1. **Configure SUMO**
    - Open SUMO and load `demo2.sumocfg` to visualize the traffic network.
    - Set the delay to `100` and click Run to view vehicles as defined in `demo2.rou.xml`.

2. **Run the Simulation**
    ```bash
    python3 run.py
    ```
    - This starts training the model and runs the V2V simulation.

## Demo

- Demo files and outputs can be found in the `demos` folder.
- For a step-by-step walkthrough, please refer to the project report or watch the demo videos.

## Reference

- SUMO Documentation: https://sumo.dlr.de/docs/index.html
- Project Report: [Add link here if available]

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.

---

*For questions, suggestions, or contributions, feel free to open an issue or pull request!*
