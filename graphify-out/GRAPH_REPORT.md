# Graph Report - .  (2026-07-20)

## Corpus Check
- Corpus is ~1,214 words - fits in a single context window. You may not need a graph.

## Summary
- 24 nodes · 31 edges · 7 communities (6 shown, 1 thin omitted)
- Extraction: 84% EXTRACTED · 16% INFERRED · 0% AMBIGUOUS · INFERRED: 5 edges (avg confidence: 0.91)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Anomaly Detection Pipeline
- Dependencies & Libraries
- Investigator Dashboard
- Future Enhancements

## God Nodes (most connected - your core abstractions)
1. `requirements.txt` - 7 edges
2. `Mule Account Detection POC` - 6 edges
3. `Anomaly Detection Model` - 5 edges
4. `Network Analysis` - 5 edges
5. `train_model.py` - 5 edges
6. `Feature Engineering` - 4 edges
7. `Risk Scoring` - 4 edges
8. `Investigator Dashboard` - 4 edges
9. `Synthetic Data Generation` - 3 edges
10. `dashboard.py` - 2 edges

## Surprising Connections (you probably didn't know these)
- `joblib` --implements--> `train_model.py`  [INFERRED]
  requirement.txt → README.md
- `requirements.txt` --references--> `plotly`  [EXTRACTED]
  README.md → requirement.txt
- `requirements.txt` --references--> `streamlit`  [EXTRACTED]
  README.md → requirement.txt
- `plotly` --implements--> `Investigator Dashboard`  [INFERRED]
  requirement.txt → README.md
- `streamlit` --implements--> `dashboard.py`  [INFERRED]
  requirement.txt → README.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Mule Account Detection Pipeline** — readme_synthetic_data_generation, readme_feature_engineering, readme_anomaly_detection_model, readme_network_analysis, readme_risk_scoring, readme_investigator_dashboard [EXTRACTED 1.00]

## Communities (7 total, 1 thin omitted)

### Community 0 - "Anomaly Detection Pipeline"
Cohesion: 0.50
Nodes (8): Anomaly Detection Model, Feature Engineering, generate_data.py, Mule Account Detection POC, Network Analysis, Risk Scoring, Synthetic Data Generation, train_model.py

### Community 1 - "Dependencies & Libraries"
Cohesion: 0.25
Nodes (8): Isolation Forest Algorithm, NetworkX, requirements.txt, joblib, networkx, numpy, pandas, scikit-learn

### Community 2 - "Investigator Dashboard"
Cohesion: 0.50
Nodes (4): dashboard.py, Investigator Dashboard, plotly, streamlit

## Knowledge Gaps
- **4 isolated node(s):** `generate_data.py`, `Future Enhancements`, `pandas`, `numpy`
  These have ≤1 connection - possible missing edges or undocumented components.
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `requirements.txt` connect `Dependencies & Libraries` to `Investigator Dashboard`?**
  _High betweenness centrality (0.250) - this node is a cross-community bridge._
- **Why does `Mule Account Detection POC` connect `Anomaly Detection Pipeline` to `Investigator Dashboard`?**
  _High betweenness centrality (0.139) - this node is a cross-community bridge._
- **Why does `Investigator Dashboard` connect `Investigator Dashboard` to `Anomaly Detection Pipeline`?**
  _High betweenness centrality (0.121) - this node is a cross-community bridge._
- **What connects `generate_data.py`, `Future Enhancements`, `pandas` to the rest of the system?**
  _4 weakly-connected nodes found - possible documentation gaps or missing edges._