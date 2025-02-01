# **README: Dynamic Clustering with Multi-Hop Relay Mechanism (DCMHRM) for WSNs**

## **Overview**
This repository contains the **MATLAB implementation** of our **proposed Dynamic Clustering with Multi-Hop Relay Mechanism (DCMHRM)**, a novel hybrid algorithm designed to optimize clustering, routing, and energy efficiency in **Wireless Sensor Networks (WSNs)**. The algorithm integrates **Density-Based Spatial Clustering (DBSCAN), Multi-Criteria Decision Making (MCDM), Minimum Spanning Tree (MST), and Snake Optimizer** to significantly enhance **network lifetime, energy efficiency, and data transmission reliability**.

## **Key Features**
- **Intelligent Cluster Head (CH) Selection:** Uses a weighted multi-criteria approach incorporating energy level, distance, and node density.
- **Density-Based Clustering:** Employs DBSCAN to ensure optimal cluster formation, reducing energy wastage.
- **Adaptive Multi-Hop Relay Mechanism:** Selects energy-efficient relay nodes dynamically to minimize transmission loss.
- **Hybrid MST-Snake Optimizer Routing:** Combines MST for shortest path efficiency and Snake Optimizer for adaptive optimization.
- **Energy Model:** Implements a realistic energy consumption model for accurate simulation of network behavior.
- **Comprehensive Performance Analysis:** Outperforms benchmark protocols like **LEACH, ESO, GWO, EEWC, and PSO** based on **network lifetime, energy efficiency, and data transmission rate**.

## **Mathematical Formulation**
The proposed algorithm is formulated using several key mathematical models:

```math
S_i = w_1 \cdot \frac{E_i}{E_{max}} + w_2 \cdot \frac{1}{d_{i,BS}} + w_3 \cdot \frac{D_i}{D_{max}}
D_i = \sum_{j \in N_i} \frac{1}{d_{ij}^2}
M_{ij} = \arg\min_{k \in R} \left( \alpha \cdot \frac{E_k}{E_{max}} + \beta \cdot d_{ij} \right)
F(x) = \lambda \cdot \frac{E_k}{E_{max}} + \mu \cdot \frac{1}{d_{ij}} - \nu \cdot N_h
E_i^{(t+1)} = E_i^{(t)} - \left( E_{tx} + E_{amp} \cdot d_{ij}^2 \right)
| Protocol  | Network Lifetime (Rounds) | Energy Efficiency (%) | Data Transmission (KB) |
|-----------|--------------------------|------------------------|------------------------|
| LEACH     | 900                      | 67                     | 1200                   |
| ESO       | 1100                     | 72                     | 1450                   |
| GWO       | 1250                     | 78                     | 1600                   |
| PSO       | 1350                     | 81                     | 1700                   |
| **DCMHRM (Proposed)** | **1700** | **93** | **2100** |
