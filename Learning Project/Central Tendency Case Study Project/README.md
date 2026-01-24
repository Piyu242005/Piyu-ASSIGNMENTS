# 📊 Central Tendency Case Study — Wine Quality Dataset

**Author:** Piyush Ramteke

---

## Overview

This project analyzes the **Wine Quality Dataset** to understand how its chemical features behave using **measures of central tendency** (mean, median, mode). By examining distributions and computing representative values, the analysis provides a solid foundation for data exploration, statistical reasoning, and machine learning preprocessing.

---

## Table of Contents

- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Features Analyzed](#features-analyzed)
- [Methodology](#methodology)
- [Visualizations](#visualizations)
- [Outputs](#outputs)
- [How to Run](#how-to-run)
- [Requirements](#requirements)
- [Key Takeaways](#key-takeaways)

---

## Dataset

| Property         | Value                                   |
|------------------|-----------------------------------------|
| File             | `Wine Quality Dataset.csv`              |
| Observations     | ~4,898 white wine samples               |
| Features         | 12 numeric columns (chemical properties + quality rating) |

---

## Project Structure

```
Central Tendency Case Study Project/
│
├── Wine_Central_Tendency_Notebook.ipynb   # Main analysis notebook
├── Wine Quality Dataset.csv               # Source dataset
├── wine_central_tendency_summary.csv      # Mean, median, mode summary
├── wine_representative_series.csv         # Representative value per feature
├── ScreenShot/                            # Saved figures and screenshots
└── README.md                              # Project documentation
```

---

## Features Analyzed

| Feature                | Description                              |
|------------------------|------------------------------------------|
| fixed acidity          | Tartaric acid content (g/L)              |
| volatile acidity       | Acetic acid content (g/L)                |
| citric acid            | Citric acid content (g/L)                |
| residual sugar         | Remaining sugar after fermentation (g/L) |
| chlorides              | Salt content (g/L)                       |
| free sulfur dioxide    | Free SO₂ (mg/L)                          |
| total sulfur dioxide   | Total SO₂ (mg/L)                         |
| density                | Density of wine (g/cm³)                  |
| pH                     | Acidity level                            |
| sulphates              | Potassium sulphate content (g/L)         |
| alcohol                | Alcohol percentage (% vol)               |
| quality                | Sensory quality score (3–9)              |

---

## Methodology

1. **Load the dataset** into a pandas DataFrame.
2. **Compute central tendency measures** for each numeric column:
   - **Mean** — arithmetic average.
   - **Median** — middle value when sorted.
   - **Mode** — most frequently occurring value.
3. **Select a representative value** per feature using a simple rule:
   - If |skewness| > 0.5 → use **median** (data is skewed).
   - Else → use **mean** (data is roughly symmetric).
4. **Visualize distributions** with histograms for every numeric feature.
5. **Create a pie chart** showing the distribution of wine quality ratings.
6. **Export results** to CSV files for reuse.

---

## Visualizations

- **Histograms:** One histogram per numeric feature to visualize spread and skewness.
- **Pie Chart:** Donut-style chart displaying the percentage distribution of quality scores.

### Sample Visualizations

#### Distribution of Alcohol
![Distribution of Alcohol](ScreenShot/Distribution%20of%20alcohol.png)

#### Distribution of Quality
![Distribution of Quality](ScreenShot/distrabtion%20og%20quality.png)

#### Pie Chart - Quality Distribution
![Pie Chart](ScreenShot/Pie%20chart.png)

#### Notebook Overview
![Notebook Overview](ScreenShot/Screenshot%202026-01-24%20190149.png)

---

## Outputs

| File                              | Description                                      |
|-----------------------------------|--------------------------------------------------|
| `wine_central_tendency_summary.csv` | Mean, Median, Mode for all numeric features     |
| `wine_representative_series.csv`    | Single representative value per feature         |

### Sample Summary (excerpt)

| Feature            | Mean   | Median | Mode  |
|--------------------|--------|--------|-------|
| fixed acidity      | 6.85   | 6.8    | 6.8   |
| volatile acidity   | 0.28   | 0.26   | 0.28  |
| residual sugar     | 6.39   | 5.2    | 1.2   |
| alcohol            | 10.51  | 10.4   | 9.4   |
| quality            | 5.88   | 6.0    | 6.0   |

---

## How to Run

1. **Clone or download** this project folder.
2. Open **`Wine_Central_Tendency_Notebook.ipynb`** in VS Code or Jupyter.
3. Run all cells from top to bottom.
4. The summary CSVs will be generated automatically.

---

## Requirements

| Package      | Version (recommended) |
|--------------|-----------------------|
| Python       | 3.9+                  |
| pandas       | 1.5+                  |
| matplotlib   | 3.5+                  |

Install dependencies with:

```bash
pip install pandas matplotlib
```

---

## Key Takeaways

- Central tendency measures help summarize large datasets quickly.
- Choosing between mean and median depends on skewness—median is more robust to outliers.
- Visualizing distributions reveals patterns that summary statistics alone may miss.
- This workflow is a building block for deeper exploratory data analysis (EDA) and feature engineering.

---

## License

This project is for educational purposes.
