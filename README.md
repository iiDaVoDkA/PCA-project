# Principal Component Analysis: Environmental Impact of Fast Fashion

A comprehensive PCA analysis project examining the environmental sustainability metrics of the fast fashion industry.

**Course:** ST2DA-I2 | 2025-2026

## 📁 Project Structure

```
PCA-Fast-Fashion-Analysis/
├── src/                          # Source code
│   └── PCA_Fast_Fashion_Environmental_Analysis.ipynb
├── data/                         # Raw data
│   └── true_cost_fast_fashion.csv
├── figures/                      # Generated visualizations
│   ├── correlation_matrix.png
│   ├── scree_plot.png
│   ├── correlation_circle.png
│   ├── individuals_plot_brands.png
│   └── biplot.png
├── output/                       # Analysis outputs
│   ├── pca_transformed_data.csv
│   ├── pca_loadings.csv
│   └── pca_eigenvalues.csv
├── report/                       # LaTeX report
│   ├── PCA_Report.tex
│   └── PCA_Report.pdf
├── presentation/                 # Beamer slides
│   ├── PCA_Presentation.tex
│   └── PCA_Presentation.pdf
├── references/                   # Course materials
│   ├── Chapter 2- Principal Component Analysis.pdf
│   └── ST2DA-Chapter 1-2025-2026.pdf
└── README.md
```

## 📊 Dataset

**True Cost of Fast Fashion Dataset**
- **Observations:** 3,000 records
- **Variables:** 12 quantitative features
- **Brands:** Shein, Zara, H&M, Forever 21, Uniqlo
- **Countries:** 10 manufacturing countries
- **Period:** 2015-2024

### Variables Analyzed

| Category | Variables |
|----------|-----------|
| Production | Monthly Production (tonnes), Release Cycles/Year |
| Environmental | Carbon Emissions (tCO2e), Water Usage (M litres), Landfill Waste |
| Economic | Average Item Price (USD), GDP Contribution (M USD) |
| Sustainability | Env Cost Index, Sustainability Score, Transparency Index, Compliance Score, Ethical Rating |

## 🔬 Methodology

1. **Data Standardization** - Z-score normalization (mean=0, std=1)
2. **Correlation Matrix** - Using Pearson correlation (variables have different units)
3. **Eigendecomposition** - Extract eigenvalues and eigenvectors
4. **Component Selection** - Kaiser criterion (λ > 1)
5. **Factor Loadings** - Correlations between variables and PCs
6. **Visualization** - Scree plot, correlation circle, biplot

## 📈 Key Findings

- **6 principal components** retained (Kaiser criterion)
- **52.51%** cumulative variance explained
- Variables show **low intercorrelation** → each captures unique sustainability dimension
- **No significant brand differentiation** in environmental profile

## 🛠️ Requirements

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy
```

For LaTeX compilation:
```bash
brew install tectonic  # macOS
# or install TeX Live/MiKTeX
```

## 🚀 Usage

### Run the Analysis

```bash
cd src
jupyter notebook PCA_Fast_Fashion_Environmental_Analysis.ipynb
```

### Compile LaTeX Documents

```bash
cd report && tectonic PCA_Report.tex
cd presentation && tectonic PCA_Presentation.tex
```

## 📚 References

1. Jolliffe, I. T., & Cadima, J. (2016). Principal component analysis: a review and recent developments. *Phil. Trans. R. Soc. A*, 374(2065).
2. Abdi, H., & Williams, L. J. (2010). Principal component analysis. *WIREs Computational Statistics*, 2(4), 433-459.
3. Pearson, K. (1901). On lines and planes of closest fit to systems of points in space. *Philosophical Magazine*, 2(11), 559-572.

## 📄 License

This project is for educational purposes as part of the ST2DA-I2 course.

---
*December 2025*

