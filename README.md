# statistics_detect_outliers_dataset

This repository contains datasets and example code for detecting outliers in statistical data. It is intended as a simple resource for learning and experimenting with outlier detection techniques.

## Contents
- data/ — (expected) directory for datasets (CSV/Excel files)
- notebooks/ — Jupyter notebooks demonstrating analysis and detection
  - notebooks/detect_outliers(statistics).ipynb — example notebook showing IQR and Z-score methods
- src/ — (optional) scripts for preprocessing and models

> If these directories or files are missing, please add your datasets and code in the appropriate folders.

## Included notebook
A new notebook has been added at `notebooks/detect_outliers(statistics).ipynb`. It demonstrates:

- Loading a small example dataset
- Sorting and inspecting the data
- Detecting outliers using the Interquartile Range (IQR) method
- Detecting outliers using the Z-score (standard deviation) method
- Visualizing the data with a boxplot (seaborn)

The notebook identifies the outliers [102, 107, 108] for the example dataset.

## Getting started
1. Clone the repository:

   git clone https://github.com/Kumarrohit99/statistics_detect_outliers_dataset.git

2. Install dependencies (example using Python and pip):

   python -m venv .venv
   source .venv/bin/activate  # macOS / Linux
   .venv\Scripts\activate     # Windows (PowerShell)
   pip install -r requirements.txt

   If you don't have a requirements.txt, the notebook requires at least:

   pip install numpy matplotlib seaborn

3. Open the notebook:

   jupyter notebook notebooks/detect_outliers(statistics).ipynb

4. Run the cells to reproduce the outlier detection steps and the boxplot visualization.

## Example approaches
- Z-score method
- Interquartile Range (IQR)
- DBSCAN clustering
- Isolation Forest

## Contributing
Contributions are welcome. Please open an issue or submit a pull request with proposed changes.

## License
Add a license file (e.g., `LICENSE`) to state the repository license. If you don't have one yet, consider adding an open license such as MIT.

## Contact
Created by @Kumarrohit99. For questions or suggestions, open an issue or reach out on GitHub.
