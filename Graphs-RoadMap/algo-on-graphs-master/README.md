# Advanced Shortest Path Algorithms  
**Duration:** July 2024  
**Type:** Self-Project  
**Tech Stack:** C++ / Python / Graph Algorithms / Data Structures  

## 🚀 Project Overview  
This project implements advanced shortest path algorithms on large-scale road and social networks, optimizing query response time for finding the shortest path between nodes. It significantly reduces computational costs compared to standard Dijkstra’s algorithm through hybrid approaches.  

## 🧠 Key Features & Contributions  
- **🔁 Bi-directional Dijkstra**: Achieved >1000× speedup over standard Dijkstra by searching simultaneously from source/target nodes.  
- **🌟 A* Pathfinding + Bi-directional Dijkstra**: Combined heuristics with bi-directional search for road network optimization.  
- **🏗️ Contraction Hierarchies (CH)**: Preprocessed graph nodes to create shortcut edges, enabling near-instantaneous queries.  
- **⚡ Performance**: Handled 1000+ real-world queries with <2s average response time on large graphs.  

## 📁 Project Structure  
advanced-shortest-path
├── data/ # Sample input graphs (road & social networks)
├── src/ # Source code
│ ├── dijkstra.cpp
│ ├── bidirectional_dijkstra.cpp
│ ├── astar.cpp
│ └── contraction_hierarchy.cpp
├── benchmarks/ # Performance analysis
├── README.md
└── requirements.txt # Dependencies


## 🧪 Algorithms Implemented  
| Algorithm               | Description                          | Use Case          |
|-------------------------|--------------------------------------|-------------------|
| Dijkstra                | Classic shortest path                | Baseline          |
| Bi-directional Dijkstra | Forward/backward simultaneous search | Speed optimization|
| A* (A-star)             | Heuristic-based pathfinding          | Geospatial networks|
| Contraction Hierarchies | Preprocessing + fast queries         | Road networks     |

## 📊 Results  
| Network Type          | Queries Tested | Avg. Query Time | Method               |
|-----------------------|----------------|-----------------|----------------------|
| Road Network (Real)   | 1000           | <2s             | CH + A*             |
| Social Network        | 500            | ~1.5s           | Bi-Directional Dijkstra|

## 📚 References  
1. Contraction Hierarchies – Geisberger et al.  
2. Stanford CS Lecture on A* Search  
3. OpenStreetMap real-world road datasets  

## 📬 Contact  
For questions/suggestions:  
- Open a GitHub issue  
- Email: [s.nikunj@iitg.ac.in]  

