# Italian Justice System Workload (2003-2024)

**22 years of Italian judicial workload data - exploring how civil and criminal case backlogs, population-adjusted pressure, and the composition of civil litigation have changed over time.**

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](italian-justice-system-workload-2003-2024.ipynb)
[![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)](https://matplotlib.org/)
[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/lucalullo/italy-justice-system-workload-2003-2024)

**[Explore the notebook](italian-justice-system-workload-2003-2024.ipynb) · [View the dataset on Kaggle](https://www.kaggle.com/datasets/lucalullo/italy-justice-system-workload-2003-2024) · [Author's GitHub](https://github.com/lucalullo)**

## At a glance

| | |
|---|---|
| **Period** | 2003-2024 |
| **Geographic scope** | Italy, national level |
| **Focus** | Pending civil and criminal proceedings; judicial pressure; civil case composition |
| **Sources** | Italian Ministry of Justice (case statistics), ISTAT (resident population), as described in the notebook |
| **Data** | Three CSV files published in the linked Kaggle dataset |
| **Methods** | Exploratory data analysis, time-series visualizations, population-adjusted indicators |
| **Stack** | Python, pandas, Matplotlib, Jupyter |

## Key observations

The original notebook highlights four long-term patterns:

1. **Civil workload:** pending civil cases rise toward a peak around 2009, then decline for much of the remaining period, with a slight increase in the final year.
2. **Criminal workload:** pending criminal cases grow until around the mid-2010s and subsequently decline, especially in the later years.
3. **Judicial pressure:** pending civil proceedings per 100,000 residents remain above the corresponding criminal indicator throughout the observed period; both decrease over time.
4. **Civil case composition:** ordinary civil litigation remains the larger share, while enforcement and insolvency proceedings represent a smaller, relatively stable component.

These are descriptive findings from the notebook, not causal claims about judicial efficiency or the effects of specific reforms.

## Analysis workflow

```text
Ministry of Justice + ISTAT data
              |
              v
       Three CSV tables
              |
              v
     pandas inspection
              |
              v
  National workload trends
   (civil and criminal)
              |
              v
 Population-adjusted pressure
              |
              v
  Civil litigation composition
              |
              v
 Interpretation and limitations
```

### What the notebook visualizes

- **Pending civil proceedings (2003-2024):** national total over time.
- **Pending criminal proceedings (2003-2024):** national total including Justice of the Peace cases.
- **Judicial pressure:** civil and criminal pending cases per 100,000 residents.
- **Civil litigation composition:** ordinary litigation and enforcement/insolvency shares.

## Dataset

The analysis uses **[Italy Justice System Workload (2003-2024)](https://www.kaggle.com/datasets/lucalullo/italy-justice-system-workload-2003-2024)**, published on Kaggle. The original notebook describes its sources as the Italian Ministry of Justice and ISTAT.

| File | Contents |
|---|---|
| `civile.csv` | Pending civil proceedings, including breakdowns by judicial level |
| `penale.csv` | Pending criminal proceedings, with totals including and excluding Justice of the Peace cases |
| `indicatori.csv` | Derived judicial pressure and litigation composition indicators |

The dataset files are not redistributed in this repository. Refer to Kaggle for the dataset and its terms of use.

## Repository contents

```text
italian-justice-system-analysis/
├── README.md
├── italian-justice-system-workload-2003-2024.ipynb
├── requirements.txt
└── .gitignore
```

The notebook is the **original Kaggle analysis**, kept unchanged. The repository adds documentation and dependency information without rewriting the analysis.

## Run the notebook

The original notebook was written for Kaggle and loads files from:

```text
/kaggle/input/datasets/lucalullo/italy-justice-system-workload-2003-2024/
```

To run it locally:

1. Download the three CSV files from the linked Kaggle dataset.
2. Install dependencies: `python -m pip install -r requirements.txt`.
3. Open `italian-justice-system-workload-2003-2024.ipynb` in Jupyter.
4. Adjust the three `pd.read_csv(...)` paths to your local dataset location.

Those path changes are only necessary for local execution; the archived notebook itself is unchanged.

## Scope and limitations

- The work is **descriptive exploratory analysis**, not a predictive or causal study.
- The indicators describe pending proceedings and case composition; by themselves they do **not** establish judicial efficiency, case duration, or the impact of specific reforms.
- The analysis uses national aggregates. Local differences and changes in reporting practices are not evaluated in the notebook.
- The notebook presents charts and qualitative trend interpretations rather than statistical hypothesis tests or uncertainty estimates.
- The data cover **2003-2024**, not the current judicial workload.

## Related work

This analysis complements my work on tabular machine learning, from-scratch algorithms, and reproducible Python projects.

**[GitHub profile](https://github.com/lucalullo) · [Kaggle profile](https://www.kaggle.com/lucalullo)**

**Author:** Luca Lullo
