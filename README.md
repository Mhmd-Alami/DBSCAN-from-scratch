# DBSCAN-from-scratch

This repository contains educational Jupyter notebooks for understanding and experimenting with clustering algorithms, with a main focus on **DBSCAN** and a comparison to **K-Means**.  
The goal is to help you intuitively learn:

- How DBSCAN works (concepts and parameters)
- How it differs from K-Means
- How parameter choices affect the resulting clusters

---

## Project Structure

### `T3-3.ipynb` — DBSCAN from Scratch (Concept & Experiments)

This notebook focuses on the **DBSCAN** clustering algorithm.  
You will:

- Review the intuition behind DBSCAN:
  - Density-based clustering
  - Core points, border points, and noise
- Experiment with different parameters:
  - `epsilon` / `eps` (neighborhood radius)
  - `minimum neighbors` / `min_samples` (minimum points to form a dense region)
- Analyze how these parameters change:
  - Number of clusters
  - Shape and distribution of clusters
  - Number of noise points (outliers)

Example excerpts from the notebook:

- “Regarding to plots below the best parameters are **0.2** for epsilon and **3** for minimum neighbors!”
- “Epsilon : 0.1”
- “Minimum neighbors : 1”
- “Clusters : 30”

The notebook helps you **visually** understand how sensitive DBSCAN is to the choice of `eps` and `min_samples` and how to search for “good” parameters.

> Note: The actual implementation and plots are inside the notebook.  
> Open it in Jupyter to see the full code, visualizations, and explanations.

---

### `T3-4.ipynb` — Finding the Best K for K-Means

This notebook is about **K-Means** and focuses on finding the **best number of clusters** \(k\).

You will:

- Apply K-Means with different values of `k`
- Use visual or quantitative methods (e.g. elbow method) to identify a suitable `k`
- Compare the behavior of K-Means to DBSCAN

Example excerpt from the notebook:

- “Find the best number of clusters for kmeans :”

This notebook is meant to highlight an important contrast:

- **K-Means** requires you to choose `k` (number of clusters) in advance.
- **DBSCAN** does **not** require `k` but instead depends on density parameters (`eps`, `min_samples`).

---

## What You Will Learn

By working through these notebooks, you will learn:

### DBSCAN Concepts

- What “density-based” clustering means
- Types of points:
  - **Core points:** have at least `min_samples` neighbors within distance `eps`
  - **Border points:** not core themselves but reachable from a core point
  - **Noise points:** neither core nor border (outliers)
- How DBSCAN can:
  - Discover clusters of **arbitrary shape**
  - **Automatically** determine the number of clusters based on density
  - Detect **outliers** naturally

### Comparing DBSCAN and K-Means

- **K-Means:**
  - You must choose `k` (number of clusters)
  - Favors spherical clusters
  - Sensitive to initialization and scale of features

- **DBSCAN:**
  - No need to predefine `k`
  - Works well with irregular-shaped clusters
  - Sensitive to `eps` and `min_samples`
  - Can mark points as noise (outliers)

This makes the repository a compact educational resource for understanding **two different philosophies** of clustering.

---

## Requirements

To run the notebooks, you need:

- **Python** (3.x)
- Recommended libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scikit-learn`
  - `jupyter` (or JupyterLab)

### Installation

You can install the dependencies using `pip`:

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

(Optionally, you can manage them inside a virtual environment.)

---

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Mhmd-Alami/DBSCAN-from-scratch.git
   cd DBSCAN-from-scratch
   ```

2. **(Optional) Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # macOS / Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```
   or manually:
   ```bash
   pip install numpy pandas matplotlib scikit-learn jupyter
   ```

4. **Launch Jupyter Notebook:**

   ```bash
   jupyter notebook
   ```

5. **Open the notebooks:**

   - `T3-3.ipynb` for DBSCAN experiments
   - `T3-4.ipynb` for K-Means and best `k`

---

## Educational Use

This repository is well-suited for:

- University / college courses on:
  - Machine Learning
  - Data Mining
  - Pattern Recognition
- Self-study to understand:
  - Clustering algorithms
  - Parameter tuning
  - Visual analysis of clustering results

Instructors can use it as:

- A lab assignment
- An in-class demo
- A starting point for student projects

---

## Possible Extensions

If you want to extend this project, here are some ideas:

- Implement **DBSCAN fully from scratch** (without using `sklearn.cluster.DBSCAN`)
- Test DBSCAN and K-Means on **real-world datasets**
- Add other clustering algorithms:
  - Hierarchical clustering
  - OPTICS
  - Spectral clustering
- Add **evaluation metrics**:
  - Silhouette score
  - Davies-Bouldin index
  - Adjusted Rand index
- Compare:
  - Performance
  - Robustness to noise
  - Ability to detect complex cluster shapes

---

## Contributing

Contributions are welcome!

You can:

- Fix bugs or improve code clarity
- Add comments and explanations
- Add new notebooks or examples
- Improve visualizations and plots
- Extend the documentation

To contribute:

1. Fork the repository
2. Create a new branch
3. Commit your changes and push the branch
4. Open a Pull Request

---

## License

This project is for educational and personal use. Feel free to fork and improve it!

---

## Acknowledgements

This repository was created as a learning exercise to better understand clustering, DBSCAN, and K-Means, and to explore how parameter choices influence clustering outcomes.
