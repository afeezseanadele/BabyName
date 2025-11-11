# Baby Names Popularity Decline Analysis (2007-2020)

A comprehensive data analysis project that identifies and visualizes US baby names that experienced the most significant decline in popularity between 2007 and 2020.

## 📊 Project Overview

This project analyzes baby naming trends in the United States by identifying names that were highly popular in 2007 (ranked in the top 100) but fell outside the top 100 by 2020. The analysis reveals shifting cultural preferences and naming trends over a 13-year period.

## 🎯 Key Findings

The analysis identifies:
- **Top 10 male names** with the biggest popularity drops
- **Top 10 female names** with the biggest popularity drops
- Names that completely disappeared from rankings vs. those that still exist but declined
- Quantitative metrics showing the magnitude of each decline

## 📁 Dataset

- **Source**: US Social Security Administration Baby Names Database
- **Years Analyzed**: 2007 and 2020
- **Scope**: Top 1000 names for each gender per year
- **Format**: CSV files with columns [Rank, Male name, Female name]

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Data visualization
- **NumPy** - Numerical operations
- **Jupyter Notebook / Google Colab** - Interactive development environment

## 📈 Methodology

### 1. Data Preparation
- Loaded datasets for 2007 and 2020
- Separated male and female names into distinct datasets
- Cleaned data (removed NaN values, stripped whitespace)

### 2. Filtering Criteria
- Focused on names ranked in the **top 100 in 2007**
- Identified names that fell **outside the top 100 in 2020**

### 3. Ranking Algorithm
- Calculated rank drop: `2020_rank - 2007_rank`
- For names not in 2020 top 1000: assigned maximum drop value (999999)
- Sorted by rank drop magnitude (descending)

### 4. Selection Process
- Selected top 10 names for each gender with the largest drops
- Prioritized names that were more popular in 2007 (lower rank numbers)

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas matplotlib numpy
```

### Running the Analysis

1. Clone the repository:
```bash
git clone https://github.com/afeezseanadele/BabyName.git
cd BabyName
```

2. Place your data files in the project directory:
   - `2007.csv`
   - `2020.csv`

3. Run the Jupyter notebook or Python script:
```bash
jupyter notebook baby_names_analysis.ipynb
```

Or if using Google Colab:
- Upload the notebook to Colab
- Upload data files to `/content/` directory
- Run all cells

## 📊 Sample Output

The analysis produces:
- **Detailed tables** showing rank changes for each name
- **Horizontal bar charts** visualizing the magnitude of decline
- **Summary statistics** on overall naming trends
- **Categorization** of names that disappeared vs. remained in top 1000

## 📝 Key Insights

- **Percentage of top 100 names that fell out** by 2020
- **Names that completely vanished** from the top 1000
- **Cultural shifts** in naming preferences over 13 years
- **Gender-specific trends** in name popularity changes

## 🔍 Use Cases

This analysis can be valuable for:
- **Researchers** studying cultural and sociological trends
- **Parents** making informed naming decisions
- **Data scientists** learning time-series analysis techniques
- **Marketers** understanding generational preferences

## 📂 Project Structure
```
BabyName/
│
├── data
│   ├── 2007.csv
│   └── 2020.csv
│
├── notebooks
│   └── BabyName.ipynb
│
├── README.md
└── LICENSE
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Potential Enhancements
- Extend analysis to more years (e.g., 2000-2024)
- Add regional/state-level analysis
- Implement predictive modeling for future trends
- Create interactive dashboards with Plotly or Streamlit
- Analyze factors influencing name popularity (pop culture, events, etc.)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Data provided by the [US Social Security Administration](https://www.ssa.gov/oact/babynames/)
- Inspired by data journalism and cultural trend analysis
- Built as part of a data analysis assessment/portfolio project

---

⭐ If you found this analysis interesting, please consider giving it a star!
```

## requirements.txt
```
pandas>=1.3.0
matplotlib>=3.4.0
numpy>=1.21.0
jupyter>=1.0.0
```

## Additional Files to Include

### .gitignore
```
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
*.egg-info/

# Jupyter Notebook
.ipynb_checkpoints

# Data files (if large)
*.csv
*.xlsx

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/
```

### LICENSE (MIT License)
```
MIT License

Copyright (c) 2024 [Afeez Sean Adele]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
