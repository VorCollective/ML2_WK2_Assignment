# Palmer Penguins Clustering (K-Means)

**Lab / Course:** Machine Learning / Data Science – Unsupervised Learning  
**Dataset:** Palmer Penguins  
**Goal:** Use K-Means clustering on penguin measurements to see if it can naturally discover the three species.

## Quick Description

- 344 penguins from Antarctica
- Measurements: bill length/depth, flipper length, body mass
- Task: cluster penguins using only measurements (no species label used)
- Result: clusters usually match the real species very well (Adelie, Chinstrap, Gentoo)

## What the Notebook Does

1. Load and check data (`1penguins.csv`)
2. Clean: drop rows with missing values
3. One-hot encode categories (for later interpretation)
4. Scale the 4 main numeric features
5. Run K-Means with 3 clusters
6. Visualize clusters using PCA (2D scatter plot)
7. Show summary stats per cluster (means, count, dominant species, % male)
8. Save results to `cluster_stats.csv`

## Typical Cluster Summary

| Cluster | Bill Length | Bill Depth | Flipper | Mass   | Count | % of total | Main Species | % Male |
|---------|-------------|------------|---------|--------|-------|------------|--------------|--------|
| 0       | ~47.5 mm   | ~18.8 mm  | ~197 mm | ~3900 g| ~87   | ~25%      | Chinstrap   | ~66%  |
| 1       | ~47.5 mm   | ~15.0 mm  | ~217 mm | ~5080 g| ~123  | ~36%      | Gentoo      | ~50%  |
| 2       | ~38.2 mm   | ~18.1 mm  | ~188 mm | ~3580 g| ~132  | ~39%      | Adelie      | ~38%  |

→ The algorithm rediscovers the species almost perfectly!

## Files

- `Labs.ipynb`          → main notebook
- `penguins.csv`       → dataset (put it in the same folder)
- `cluster_stats.csv`   → generated summary table

## How to Run

1. Put `1penguins.csv` next to the notebook
2. Install packages (if needed):
   ```bash
   pip install pandas matplotlib seaborn numpy scikit-learn
