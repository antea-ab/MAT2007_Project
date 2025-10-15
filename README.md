# Antibiotic Consumption and E. coli Resistance Analysis

**Author:** Antea Abilekaj  
**Course:** MAT2007  
**Date:** October 2025

## Overview

This project investigates the relationship between antibiotic consumption and *Escherichia coli* resistance patterns across countries. The analysis explores:

1. Which antibiotics show the strongest correlation between human consumption and resistance
2. How resistance varies across different antibiotics and countries  
3. The relationship between livestock antibiotic use and human bacterial resistance

## Key Findings

- **Top correlations:** Imipenem (r = 0.425) and Cefotaxime (r = 0.420) showed the strongest correlations between human consumption and resistance (both p < 0.01)
- **Resistance patterns:** Older antibiotics (Ampicillin, Co-trimoxazole) show high resistance (>60%), while last-resort antibiotics (carbapenems, Colistin) remain effective (<10% resistance)
- **Livestock connection:** No statistically significant correlations found between livestock antibiotic use and human E. coli resistance (all p > 0.05)

## Data Sources

1. **Human Antibiotic Consumption (2023)**  
   - Source: WHO Antimicrobial Consumption Database
   - File: `amu.csv`
   - 65 countries, measured in DID (Defined Daily Doses per 1,000 inhabitants per day)

2. **Antimicrobial Resistance Data**  
   - Source: WHO Global Antimicrobial Resistance and Use Surveillance System (GLASS)
   - File: `resistance.csv`
   - 879 records across 93 countries for *E. coli* bloodstream infections
   - 14 different antibiotics tested

3. **Livestock Antimicrobial Usage (2020)**  
   - Source: Mulchandani et al. (2023) via Our World in Data
   - File: `antibiotic-usage-in-livestock.csv`
   - 192 countries, measured in mg per population-corrected units (PCU)

## Repository Structure

```
project/
├── antibiotic_resistance_analysis.ipynb    # Main analysis notebook
├── data/                                   # Data files (see Data Sources)
├── outputs/                                # Generated figures
│   ├── 1_top2_antibiotics_with_countries.png
│   ├── 2_antibiotic_resistance_distribution.png
│   └── 3_livestock_vs_human_resistance.png
├── requirements.txt                        # Python dependencies
└── README.md                               # This file
```

## Requirements

- Python 3.8+
- pandas
- matplotlib
- seaborn
- scipy
- adjustText
- jupyter

Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Clone this repository:
```bash
git clone https://github.com/[your-username]/antibiotic-resistance-analysis.git
cd antibiotic-resistance-analysis
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open and run the Jupyter notebook:
```bash
jupyter notebook antibiotic_resistance_analysis.ipynb
```

## Methods Summary

This analysis examined relationships between antibiotic consumption and *E. coli* resistance using Pearson correlation analysis. Data preprocessing included filtering resistance records for *E. coli* bloodstream infections and standardizing country names. Antibiotics were categorized into seven classes (penicillins, cephalosporins, fluoroquinolones, folate inhibitors, carbapenems, and polymyxins) for comparative analysis. Statistical significance was set at p < 0.05, with a minimum of 10 country data points required for correlation analysis.

## Visualizations

### 1. Top Antibiotics: Human Consumption vs. Resistance
![Top 2 Antibiotics](outputs/1_top2_antibiotics_with_countries.png)

### 2. Resistance Distribution Across Countries (Color-coded by Class)
![Resistance Distribution](outputs/2_antibiotic_resistance_distribution.png)

### 3. Livestock Use vs. Human Resistance
![Livestock Analysis](outputs/3_livestock_vs_human_resistance.png)

## Citation

If you use this analysis, please cite:

```
Abilekaj, A. (2025). Antibiotic Consumption and E. coli Resistance Analysis. 
MAT2007 Course Project. [GitHub repository URL]
```

## Data Citations

- WHO/ECDC Antimicrobial Consumption Database
- WHO Global Antimicrobial Resistance and Use Surveillance System (GLASS)
- Mulchandani et al. (2023). "Global trends in antimicrobial use in food-producing animals: 2020 to 2030"

## License

This project is available for educational and research purposes.

## Contact

For questions or collaboration: [Your email]

