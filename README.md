# Escher Maps for BiGG Models

This repository hosts a comprehensive collection of metabolic maps generated for models in the [BiGG Models database](http://bigg.ucsd.edu/). These maps are formatted for [Escher](https://escher.github.io/) and are designed to provide clear, orthogonal visualizations of complex metabolic networks.

## 🚀 How to Use
You can view and interact with these maps directly using the custom Escher viewer:

### **[👉 Open Escher Viewer](https://forxhunter.github.io/escher/)**

1.  **Select a Model**: Browse the folders in this repository to find the organism/model of interest (e.g., `e_coli_core`).
2.  **Choose a View**:
    *   **Combined Map** (`*_Combined.json`): View the entire network tiled by subsystem.
    *   **Subsystem Map** (`*_Glycolysis.json`): View a focused, individual pathway.
3.  **Load in Escher**: Use the "Load Map" feature on the website to import the JSON file.

## 🛠️ How it is Generated
These maps were created using an advanced **AutoLayout AI** pipeline developed by Tianyu Wu. The generation process prioritizes biological clarity and geometric precision:

1.  **Biological Decomposition**: 
    *   The full network is broken down into meaningful functional units.
    *   Priority is given to **KEGG Pathways** and explicit subsystems.
    *   Large clusters are recursively partitioned to ensure readability.

2.  **Algorithmic Layout**:
    *   **Simulated Annealing**: Optimizes node positions to minimize energy (edge crossings, stress).
    *   **Manhattan Geometry**: Enforces strict horizontal and vertical alignment for all edges.
    *   **Collision Resolution**: Active algorithms ensure nodes do not overlap.

3.  **Smart Labeling**:
    *   **Dynamic collision detection** ensures text labels never obscure the network structure.
    *   Labels shift adaptively to avoid crossing edges or nodes.

## 📂 Repository Structure
*   `{Model_ID}/` - Folder for a specific BiGG model.
    *   `{Model_ID}_Combined.json` - The master map containing all subsystems tiled together.
    *   `{Model_ID}_{Subsystem}.json` - Individual maps for each specific subsystem.

---
*Created by Tianyu Wu (GitHub: [forxhunter](https://github.com/forxhunter))*
