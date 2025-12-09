# 🏫 Crowd Evacuation Simulation Based on Cellular Automaton Integrating Game Theory

A multi-agent evacuation simulation that combines **Cellular Automaton** modeling with **Game Theory** (Prisoner's Dilemma) to study how cooperative vs. competitive behaviors affect emergency evacuation outcomes. Developed for **CS5110 - Multi-Agent Systems**.

> 📊 **Key Finding:** Cooperative agents demonstrate higher evacuation success rates and lower wait times compared to defectors, validating that cooperation-promoting mechanisms improve overall evacuation efficiency.

---

## 📘 Abstract

Emergency evacuations involve complex interactions where individuals must decide whether to cooperate or compete for limited exit paths. This project simulates these dynamics by:

- Modeling agent behaviors using **Prisoner's Dilemma** game theory
- Implementing **Cellular Automaton** for spatial movement and collision detection
- Analyzing how **cooperation vs. defection** strategies affect evacuation outcomes
- Simulating realistic hazards including **fire zones** and **debris**

---

## 🏗️ Architecture Overview

| Component | Description |
|-----------|-------------|
| **SchoolGrid** | Generates complex school layout with classrooms, gym, library, auditorium, cafeteria, and hallways |
| **Agent** | Individual entities with strategies (Cooperate/Defect), reputation, panic levels, and movement tracking |
| **EvacuationSimulator** | Core simulation engine with BFS pathfinding, conflict resolution, and strategy evolution |
| **Visualization Engine** | Real-time grid visualization and statistical analysis plots |

---

## 🎮 Game Theory Model

### Prisoner's Dilemma Payoff Matrix

| Agent 1 / Agent 2 | Cooperate | Defect |
|-------------------|-----------|--------|
| **Cooperate** | (3, 3) | (0, 5) |
| **Defect** | (5, 0) | (1, 1) |

### Strategy Mechanics

- **Cooperators**: Gain reputation bonuses, receive priority in mutual cooperation scenarios
- **Defectors**: Short-term gains but face escalating penalties and reputation loss
- **Strategy Evolution**: Agents adapt strategies based on neighboring agents' success

---

## 🏫 School Environment

### Layout Components

| Area | Features |
|------|----------|
| **Classrooms (4)** | Desk obstacles in grid pattern |
| **Hallway** | Central corridor with debris and bottleneck points |
| **Gym** | Scattered equipment obstacles |
| **Library** | Bookshelf barriers |
| **Auditorium** | Row seating obstacles |
| **Cafeteria** | Table arrangements |

### Hazards

- 🔥 **Fire Zones**: Spreading fire that blocks paths
- 🪨 **Debris**: Random obstacles in hallways
- 🚧 **Bottlenecks**: Artificial chokepoints creating congestion

---

## ⚙️ Implementation Details

### Tech Stack

- **Language**: Python 3.x
- **Visualization**: Matplotlib, NumPy
- **Pathfinding**: Breadth-First Search (BFS)
- **Data Structures**: Collections (deque), Enum

### Key Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| Grid Size | 70 × 50 | School dimensions |
| Defector Penalty | 0.5 | Penalty multiplier for defectors |
| Strategy Update Prob | 0.25 | Chance of strategy adaptation |
| Max Steps | 400 | Simulation time limit |

### Agent Attributes

- **Strategy**: Cooperate or Defect
- **Reputation**: Accumulated trust score
- **Panic Level**: Affects decision-making
- **Inertia**: Resistance to strategy change

---

## 📈 Simulation Metrics

The simulation tracks:

- **Evacuation Success Rate**: Percentage of agents who escape
- **Cooperator vs. Defector Escape Counts**
- **Average Steps to Exit**: By strategy type
- **Average Wait Time**: Time spent blocked
- **Total Conflicts**: Movement collision events
- **Peak Congestion**: Maximum crowding near exits
- **Mutual Cooperation Events**: Successful cooperative interactions

---

## 🎨 Visualizations

### Grid Visualization
- 🔵 **Blue**: Cooperator agents
- 🔴 **Red**: Defector agents
- ⬛ **Dark Gray**: Walls
- 🟢 **Green**: Exits
- 🟤 **Brown**: Obstacles
- 🟠 **Orange**: Fire
- ⬜ **Gray**: Debris

### Analysis Plots
1. Strategy evolution over time
2. Cumulative evacuation progress
3. Congestion levels near exits
4. Conflicts per time step
5. Final results by strategy
6. Efficiency comparison (steps & wait time)

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/evacuation-simulation.git
   cd evacuation-simulation
   ```

2. **Install dependencies**
   ```bash
   pip install numpy matplotlib
   ```

3. **Run the simulation**
   ```bash
   jupyter notebook py__1_.ipynb
   ```
   Or convert to Python script:
   ```bash
   jupyter nbconvert --to script py__1_.ipynb
   python py__1_.py
   ```

---

## 📁 Project Structure

```
evacuation-simulation/
├── README.md
├── py__1_.ipynb          # Main simulation notebook
└── report.pdf            # Project report
```

---


## 📄 Reference

Xue J, Yang H-C, Zhang M, Wang Z, Shi L. Crowd Evacuation Conflicts Simulation Based Cellular Automaton Integrating Game Theory. Proceedings of the 18th ACM SIGGRAPH International Conference on Virtual-Reality Continuum and its Applications in Industry. 2022. https://dl.acm.org/doi/10.1145/3574131.3574445

---


## 📜 License

This project is for educational purposes as part of CS5110 coursework.
