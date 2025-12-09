# 🏫 Multi-Agent School Evacuation Simulation

A multi-agent systems project simulating emergency evacuation scenarios in realistic school environments. Developed for Multi-Agent Systems to demonstrate how building layout and obstacle placement impact evacuation effectiveness.

> 📊 **Key Finding:** Strategic obstacle placement resulted in ~30% of agents becoming trapped with no viable exit paths, highlighting critical design flaws in evacuation routes.

---

## 📘 Abstract

Emergency evacuations in complex buildings like schools present significant challenges due to obstacles, bottlenecks, and congested pathways. This project simulates evacuation scenarios using:

- **Realistic school layouts** with multiple room types
- **Strategic obstacle placement** mimicking real-world environments
- **BFS-based pathfinding** to calculate evacuation distances and accessibility
- **Visualization tools** for analyzing evacuation effectiveness

---

## 🏗️ Architecture Overview

The simulation consists of three main components:

| Component | Description |
|-----------|-------------|
| **SchoolGrid** | Generates realistic school layouts with 7 room types and appropriate obstacles |
| **EvacuationSimulator** | Uses BFS algorithms to calculate distances, identify bottlenecks, and predict evacuation timing |
| **Visualization Engine** | Produces color-coded maps with legends for clear result interpretation |

---

## 🏫 School Layout Design

The simulation creates a complex 7-room school environment:

```
┌─────────────┬─────────────┬─────────────┐
│  Classroom  │   Hallway   │  Classroom  │
│    (1)      │             │    (2)      │
├─────────────┤             ├─────────────┤
│  Classroom  │             │  Classroom  │
│    (3)      │             │    (4)      │
├─────────────┴─────────────┴─────────────┤
│              Cafeteria                  │
├──────────────────┬──────────────────────┤
│       Gym        │       Library        │
└──────────────────┴──────────────────────┘
```

### 🪑 Obstacle Types

| Room Type | Obstacles | Pattern |
|-----------|-----------|---------|
| Classrooms | Desks, chairs | Grid arrangement |
| Hallways | Lockers | Lining walls |
| Cafeteria | Tables, benches | Maze-like paths |
| Gym | Equipment | Scattered placement |
| Library | Bookshelves | Barrier formations |

---

## ⚙️ Implementation Details

- **🔧 Language:** Python 3.x
- **📊 Visualization:** Matplotlib
- **🧭 Pathfinding:** Breadth-First Search (BFS)
- **📐 Grid System:** 2D numpy arrays

### Key Algorithms

| Algorithm | Purpose |
|-----------|---------|
| BFS Pathfinding | Calculate shortest paths to exits |
| Bottleneck Detection | Identify congestion points |
| Accessibility Analysis | Determine trapped agent locations |
| Evacuation Time Estimation | Predict clearing time based on distance + congestion |

---

## 📈 Results & Findings

### Evacuation Metrics

| Metric | Value |
|--------|-------|
| Total Agents | ~100 |
| Successfully Evacuated | ~70% |
| Trapped (No Exit Path) | ~30% |
| Average Evacuation Distance | Varies by room |

### Key Insights

- ⚠️ **Library Area:** Bookshelves create complete barriers, trapping agents entirely
- 🚪 **Hallway Bottlenecks:** Lockers reduce effective corridor width
- 📍 **Classroom Accessibility:** Desk arrangements can block direct exit routes
- ⏱️ **Evacuation Time:** Highly dependent on initial agent position and obstacle density

---

## 🎨 Visualization Features

The simulation generates professional visualizations including:

- **Color-coded grid maps** showing room types and obstacles
- **Heatmaps** displaying evacuation distances
- **Agent position overlays** with path indicators
- **Legend and annotations** for clear interpretation

---

## 🛠️ Tech Stack

- Python 3.x
- NumPy (grid operations)
- Matplotlib (visualization)
- Collections (BFS queue implementation)

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
   python evacuation_simulation.py
   ```

4. **View output**
   - ASCII grid printed to console
   - PNG visualization saved to working directory

---

## 📁 Project Structure

```
evacuation-simulation/
├── README.md
├── evacuation_simulation.py    # Main simulation code
├── school_grid.py              # SchoolGrid class
├── simulator.py                # EvacuationSimulator class
├── visualization.py            # Plotting utilities
└── report.pdf                  # Project report
```


---

📄 Reference

Crowd Evacuation Conflicts Simulation Based Cellular Automaton Integrating Game Theory

---

## 📜 License

This project is for educational purposes as coursework
